<script>
export default {

  // Middleware
  middleware: ['auth']
}
</script>

<template>
  <div>
    <!-- Head -->
    <SectionEditProfileHead />
    <div class="container">
      <div class="row">
        <div class="col-sm-12 col-md-8">
          <!-- Edit User Password -->
          <section-change-password />
        </div>
        <div class="col-sm-12 col-md-4">
          <SectionProfileRecords />
        </div>
      </div>
    </div>
  </div>
</template>

