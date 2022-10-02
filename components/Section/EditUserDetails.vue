<template>
    <section class="user-details-area pt-40px pb-40px">
        <div class="tab-content mb-50px" id="myTabContent">
            <div class="tab-pane fade show active" id="edit-profile" role="tabpanel" aria-labelledby="edit-profile-tab">
                <div class="user-panel-main-bar">
                    <div class="user-panel">
                        <div class="bg-gray p-3 rounded-rounded">
                            <h3 class="fs-17">Edit your profile</h3>
                        </div>
                        <form method="post" class="pt-35px">
                            <div class="settings-item mb-10px">
                                <h4 class="fs-14 pb-2 text-gray text-uppercase">Public information</h4>
                                <div class="divider"><span></span></div>
                                <div class="row pt-4 align-items-center">
                                    <div class="col-lg-6">
                                        <div class="edit-profile-photo d-flex flex-wrap align-items-center">
                                            <img src="images/team.jpg" alt="user avatar" class="profile-img mr-4">
                                            <div>
                                                <div class="file-upload-wrap file--upload-wrap">
                                                    <input type="file" name="files[]" class="multi file-upload-input"
                                                        multiple>
                                                    <span class="file-upload-text"><i
                                                            class="la la-photo mr-2"></i>Upload Photo</span>
                                                </div>
                                                <p class="fs-14">Maximum file size: 10 MB.</p>
                                            </div>
                                        </div>
                                    </div><!-- end col-lg-6 -->
                                    <div class="col-lg-6">
                                        <div class="input-box">
                                            <label class="fs-13 text-black lh-20 fw-medium">Display name</label>
                                            <div class="form-group">
                                                <input class="form-control form--control" type="text" name="text"
                                                    value="Arden Smith">
                                            </div>
                                        </div>
                                        <div class="input-box">
                                            <label class="fs-13 text-black lh-20 fw-medium">Location</label>
                                            <div class="form-group">
                                                <input class="form-control form--control" type="text" name="text"
                                                    value="United States">
                                            </div>
                                        </div>
                                    </div><!-- end col-lg-6 -->
                                    <div class="col-lg-12">
                                        <div class="input-box">
                                            <label class="fs-15 text-black lh-20 fw-medium">About me</label>
                                            <div class="form-group">
                                                <textarea class="form-control form--control user-text-editor" rows="10"
                                                    cols="40"></textarea>
                                            </div>
                                        </div>
                                    </div><!-- end col-lg-12 -->
                                </div><!-- end row -->
                            </div><!-- end settings-item -->
                            <div class="settings-item">
                                <h4 class="fs-14 pb-2 text-gray text-uppercase">Web presence</h4>
                                <div class="divider"><span></span></div>
                                <div class="row pt-4">
                                    <div class="col-lg-6">
                                        <div class="input-box">
                                            <label class="fs-13 text-black lh-20 fw-medium">Website link</label>
                                            <div class="form-group">
                                                <input class="form-control form--control pl-40px" type="text"
                                                    name="text">
                                                <span class="la la-link input-icon"></span>
                                            </div>
                                        </div>
                                    </div><!-- end col-lg-6 -->
                                    <div class="col-lg-6">
                                        <div class="input-box">
                                            <label class="fs-13 text-black lh-20 fw-medium">Twitter link</label>
                                            <div class="form-group">
                                                <input class="form-control form--control pl-40px" type="text"
                                                    name="text">
                                                <span class="la la-twitter input-icon"></span>
                                            </div>
                                        </div>
                                    </div><!-- end col-lg-6 -->
                                    <div class="col-lg-6">
                                        <div class="input-box">
                                            <label class="fs-13 text-black lh-20 fw-medium">Facebook link</label>
                                            <div class="form-group">
                                                <input class="form-control form--control pl-40px" type="text"
                                                    name="text">
                                                <span class="la la-facebook input-icon"></span>
                                            </div>
                                        </div>
                                    </div><!-- end col-lg-6 -->
                                    <div class="col-lg-6">
                                        <div class="input-box">
                                            <label class="fs-13 text-black lh-20 fw-medium">Instagram link</label>
                                            <div class="form-group">
                                                <input class="form-control form--control pl-40px" type="text"
                                                    name="text">
                                                <span class="la la-instagram input-icon"></span>
                                            </div>
                                        </div>
                                    </div><!-- end col-lg-6 -->
                                    <div class="col-lg-6">
                                        <div class="input-box">
                                            <label class="fs-13 text-black lh-20 fw-medium">Youtube link</label>
                                            <div class="form-group">
                                                <input class="form-control form--control pl-40px" type="text"
                                                    name="text">
                                                <span class="la la-youtube input-icon"></span>
                                            </div>
                                        </div>
                                    </div><!-- end col-lg-6 -->
                                    <div class="col-lg-6">
                                        <div class="input-box">
                                            <label class="fs-13 text-black lh-20 fw-medium">Vimeo link</label>
                                            <div class="form-group">
                                                <input class="form-control form--control pl-40px" type="text"
                                                    name="text">
                                                <span class="la la-vimeo input-icon"></span>
                                            </div>
                                        </div>
                                    </div><!-- end col-lg-6 -->
                                    <div class="col-lg-12">
                                        <div class="input-box">
                                            <label class="fs-13 text-black lh-20 fw-medium">GitHub link</label>
                                            <div class="form-group">
                                                <input class="form-control form--control pl-40px" type="text"
                                                    name="text">
                                                <span class="la la-github input-icon"></span>
                                            </div>
                                        </div>
                                    </div><!-- end col-lg-12 -->
                                    <div class="col-lg-12">
                                        <div class="submit-btn-box pt-3">
                                            <button class="btn theme-btn" type="button">Save changes</button>
                                        </div>
                                    </div><!-- end col-lg-12 -->
                                </div><!-- end row -->
                            </div><!-- end settings-item -->
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
                                <button type="button" class="btn btn-danger fw-medium" data-toggle="modal"
                                    data-target="#deleteModal" id="delete-button" disabled><i
                                        class="la la-trash mr-1"></i> Delete your account</button>
                            </div>
                        </div>
                    </div><!-- end user-panel -->
                </div><!-- end user-panel-main-bar -->
            </div><!-- end tab-pane -->
        </div>
    </section>
</template>