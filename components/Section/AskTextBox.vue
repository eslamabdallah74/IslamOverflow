<template>
    <div class="text-editor-holder">
        <div class="text-editor" v-if="editor">
            <button type="button" @click="editor.chain().focus().toggleBold().run()"
                :disabled="!editor.can().chain().focus().toggleBold().run()"
                :class="{ 'is-active': editor.isActive('bold') }">
                <b>B</b>
            </button>
            <button type="button" @click="editor.chain().focus().toggleItalic().run()"
                :disabled="!editor.can().chain().focus().toggleItalic().run()"
                :class="{ 'is-active': editor.isActive('italic') }">
                <i>
                    <IconItalic />
                </i>
            </button>
            <button type="button" @click="editor.chain().focus().toggleStrike().run()"
                :disabled="!editor.can().chain().focus().toggleStrike().run()"
                :class="{ 'is-active': editor.isActive('strike') }">
                <IconDash />
            </button>
            <button type="button" @click="editor.chain().focus().toggleCode().run()"
                :disabled="!editor.can().chain().focus().toggleCode().run()"
                :class="{ 'is-active': editor.isActive('code') }">
                <span class="code"> C </span>
            </button>
            <button type="button" @click="editor.chain().focus().unsetAllMarks().run()">
                حذف الاستايل
            </button>

            <button type="button" @click="editor.chain().focus().setParagraph().run()"
                :class="{ 'is-active': editor.isActive('paragraph') }">
                براجراف
            </button>
            <!-- Heading -->
            <nav style="display: inline;" class="menu-bar ml-auto pr-2">
                <ul style="display: inline;">
                    <li>
                        <button type="button">
                            <IconDownArrow /> الخط
                        </button>
                        <ul class="dropdown-menu-item font">

                            <li>
                                <button type="button" @click="editor.chain().focus().toggleHeading({ level: 6 }).run()"
                                    :class="{ 'is-active': editor.isActive('heading', { level: 6 }) }">
                                    <h6>ABC</h6>
                                </button>
                            </li>
                            <li>
                                <button type="button" @click="editor.chain().focus().toggleHeading({ level: 5 }).run()"
                                    :class="{ 'is-active': editor.isActive('heading', { level: 5 }) }">
                                    <h5>ABC</h5>
                                </button>
                            </li>
                            <li>
                                <button type="button" @click="editor.chain().focus().toggleHeading({ level: 4 }).run()"
                                    :class="{ 'is-active': editor.isActive('heading', { level: 4 }) }">
                                    <h4>ABC</h4>
                                </button>
                            </li>
                            <li>
                                <button type="button" @click="editor.chain().focus().toggleHeading({ level: 3 }).run()"
                                    :class="{ 'is-active': editor.isActive('heading', { level: 3 }) }">
                                    <h3>ABC</h3>
                                </button>
                            </li>
                            <li>
                                <button type="button" @click="editor.chain().focus().toggleHeading({ level: 2 }).run()"
                                    :class="{ 'is-active': editor.isActive('heading', { level: 2 }) }">
                                    <h2>ABC</h2>
                                </button>
                            </li>
                            <li>
                                <button type="button" @click="editor.chain().focus().toggleHeading({ level: 1 }).run()"
                                    :class="{ 'is-active': editor.isActive('heading', { level: 1 }) }">
                                    <h1>ABC</h1>
                                </button>
                            </li>
                        </ul>
                    </li>
                </ul>
            </nav>
            <button type="button" @click="setLink" :class="{ 'is-active': editor.isActive('link') }">
                <IconLink />
            </button>
            <button type="button" @click="editor.chain().focus().unsetLink().run()"
                :disabled="!editor.isActive('link')">
                <IconRemoveLink />
            </button>
            <button type="button" @click="editor.chain().focus().toggleBulletList().run()"
                :class="{ 'is-active': editor.isActive('bulletList') }">
                <IconUlist />
            </button>
            <button type="button" @click="editor.chain().focus().toggleOrderedList().run()"
                :class="{ 'is-active': editor.isActive('orderedList') }">
                <IconOlist />
            </button>
            <button type="button" @click="editor.chain().focus().clearNodes().run()">
                حذف نمط القائمة
            </button>
            <button type="button" @click="editor.chain().focus().setHorizontalRule().run()">
                خط أفقي
            </button>
            <button type="button" @click="editor.chain().focus().undo().run()"
                :disabled="!editor.can().chain().focus().undo().run()">
                الغاء
            </button>
            <button type="button" @click="editor.chain().focus().redo().run()"
                :disabled="!editor.can().chain().focus().redo().run()">
                إعادة
            </button>
        </div>
        <div class="text-area-holder">
            <editor-content :editor="editor" />
        </div>
    </div>

</template>

<script>
import StarterKit from '@tiptap/starter-kit'
import Link from '@tiptap/extension-link'
import { Editor, EditorContent } from '@tiptap/vue-2'

export default {
    components: {
        EditorContent,
    },

    data() {
        return {
            editor: null,
        }
    },

    mounted() {
        this.editor = new Editor({
            extensions: [
                StarterKit,
                Link.configure({
                    openOnClick: true,
                }),
            ],
            content: "",
        });
    },
    // Link
    methods: {
        setLink() {
            const previousUrl = this.editor.getAttributes('link').href
            const url = window.prompt('URL', previousUrl)

            // cancelled
            if (url === null) {
                return
            }

            // empty
            if (url === '') {
                this.editor
                    .chain()
                    .focus()
                    .extendMarkRange('link')
                    .unsetLink()
                    .run()

                return
            }

            // update link
            this.editor
                .chain()
                .focus()
                .extendMarkRange('link')
                .setLink({ href: url })
                .run()
        },
    },

    beforeUnmount() {
        this.editor.destroy()
    },
}
</script>
