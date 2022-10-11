<script>
import Vue from 'vue'
import vueCountryRegionSelect from 'vue-country-region-select'
Vue.use(vueCountryRegionSelect)

export default {
  mounted() {
    setTimeout(() => {
      this.name = this.$auth.user.name;
      this.title = this.$auth.user.title;
      this.about = this.$auth.user.about;
      this.website = this.$auth.user.website;
      this.country = this.$auth.user.location;
      this.image = this.$auth.user.profile_img_url;
    }, 500);
  },
  data() {
    return {
      name: "",
      title: "",
      about: "",
      website: "",
      location: "",
      country: this.$auth.user.location ? this.$auth.user.location : '',
      image: '',
    }
  },
  methods: {
    update() {
      try {
        console.log(this.name)
        console.log(this.title)
        console.log(this.about)
        console.log(this.website)
        console.log(this.country)
        // $axios.post('/user-update', {
        //   name: user.name,
        //   about: user.about,
        //   title: user.title,
        //   website: user.website,
        //   image: this.image,
        // });
      } catch (error) {
        console.log(error)

      }
    }
  },

}
</script>

<template>
  <section class="user-details-area pt-40px pb-40px">
    <div class="tab-content mb-50px" id="myTabContent">
      <div class="tab-pane fade show active" id="edit-profile" role="tabpanel" aria-labelledby="edit-profile-tab">
        <div class="user-panel-main-bar">
          <div class="user-panel">
            <div class="bg-gray p-3 rounded-rounded">
              <h3 class="fs-17">Edit your profile </h3>
            </div>
            <form method="post" class="pt-35px">
              <div class="settings-item mb-10px">
                <h4 class="fs-14 pb-2 text-gray text-uppercase">Public information</h4>
                <div class="divider"><span></span></div>
                <div class="row pt-4 align-items-center">
                  <!-- Image -->
                  <div class="col-lg-12 col-md-12 mb-4">
                    <div class="edit-profile-photo d-flex flex-wrap align-items-center">
                      <img :src="image" alt="user avatar" class="profile-img mr-4">
                      <div>
                        <div class="file-upload-wrap file--upload-wrap">
                          <input type="file" class="multi file-upload-input" multiple>
                          <span class="file-upload-text"><i class="la la-photo mr-2"></i>Upload Photo</span>
                        </div>
                        <p class="fs-14">Maximum file size: 10 MB.</p>
                      </div>
                    </div>
                  </div><!-- end col-lg-6 -->
                  <div class="col-lg-6">
                    <div class="input-box">
                      <label class="fs-13 text-black lh-20 fw-medium">Display name</label>
                      <div class="form-group">
                        <input v-model="name" class="form-control form--control" type="text" name="text">
                      </div>
                    </div>
                  </div><!-- end col-lg-6 -->
                  <div class="col-lg-6 col-md-6">
                    <div class="input-box">
                      <label class="fs-13 text-black lh-20 fw-medium">title </label>
                      <div class="form-group">
                        <input v-model="title" class="form-control form--control" type="text" name="text">
                      </div>
                    </div>
                  </div>
                  <div class="col-lg-6 col-md-6">
                    <div class="input-box">
                      <label class="fs-13 text-black lh-20 fw-medium">Location</label>
                      <div class="form-group">
                        <country-select class="form-control form--control" v-model="country" :country="country"
                          topCountry="EG" />
                      </div>
                    </div>
                  </div>
                  <div class="col-lg-6 col-md-6">
                    <div class="input-box">
                      <label class="fs-15 text-black lh-20 fw-medium">موقعك </label>
                      <div class="form-group">
                        <input v-model="website" class="form-control form--control" type="text" name="text"
                          placeholder="www.googl.com">
                      </div>
                    </div>
                  </div>
                  <div class="col-lg-12">
                    <div class="input-box">
                      <label class="fs-15 text-black lh-20 fw-medium">About me</label>
                      <div class="form-group">
                        <textarea v-model="about" placeholder="اكنب نبذه عنك"
                          class="form-control form--control user-text-editor" rows="10" cols="40"></textarea>
                      </div>
                    </div>
                  </div>
                </div><!-- end row -->
              </div><!-- end settings-item -->
              <div class="col-lg-12">
                <div class="submit-btn-box pt-3">
                  <button class="btn theme-btn" @click.prevent="update" type="button">Save changes</button>
                </div>
              </div><!-- end col-lg-12 -->
            </form>
          </div><!-- end user-panel -->
        </div><!-- end user-panel-main-bar -->
      </div><!-- end tab-pane -->

      <div class="tab-pane fade" id="delete-account" role="tabpanel" aria-labelledby="delete-account-tab">
        <div class="user-panel-main-bar">
          <div class="user-panel">
            <div class="delete-account-info card card-item border border-danger">
              <div class="card-body">
                <h3 class="fs-22 text-danger fw-bold">Delete Account</h3>
                <p class="pb-3 pt-2 lh-22 fs-15">Before confirming that you would like your profile
                  deleted, we'd like to take a moment to explain the implications of deletion:</p>
                <ul class="generic-list-item generic-list-item-bullet fs-15">
                  <li>Deletion is irreversible, and you will have no way to regain any of your
                    original content, should this deletion be carried out and you change your mind
                    later on.</li>
                  <li>Your questions and answers will remain on the site, but will be disassociated
                    and anonymized (the author will be listed as "user15319675") and will not
                    indicate your authorship even if you later return to the site.</li>
                </ul>
                <p class="pb-3 pt-2 lh-22 fs-15">Once you delete your account, there is no going back.
                  Please be certain.</p>
                <div class="custom-control custom-checkbox fs-15 mb-4">
                  <input type="checkbox" class="custom-control-input" id="delete-terms">
                  <label class="custom-control-label custom--control-label lh-22" for="delete-terms">I
                    have read the information stated above and understand the implications of having
                    my profile deleted. I wish to proceed with the deletion of my profile.</label>
                </div>
                <button type="button" class="btn btn-danger fw-medium" data-toggle="modal" data-target="#deleteModal"
                  id="delete-button" disabled><i class="la la-trash mr-1"></i> Delete your account</button>
              </div>
            </div>
          </div><!-- end user-panel -->
        </div><!-- end user-panel-main-bar -->
      </div><!-- end tab-pane -->
    </div>
  </section>
</template>
