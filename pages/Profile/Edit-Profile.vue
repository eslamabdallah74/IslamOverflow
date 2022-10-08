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
          <!-- Edit User Details -->
          <section-edit-user-details />
        </div>
        <div class="col-sm-12 col-md-4">
          <SectionProfileRecords />
        </div>
      </div>
    </div>
  </div>
</template>

