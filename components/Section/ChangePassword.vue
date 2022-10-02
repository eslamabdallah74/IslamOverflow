<template>
    <section class="user-details-area pt-40px pb-40px">

        <div class="tab-pane" id="change-password" role="tabpanel" aria-labelledby="change-password-tab">
            <div class="user-panel-main-bar">
                <div class="user-panel">
                    <div class="bg-gray p-3 rounded-rounded">
                        <h3 class="fs-17">Change password</h3>
                    </div>
                    <form method="post" class="pt-20px">
                        <div class="settings-item mb-30px">
                            <div class="form-group">
                                <label class="fs-13 text-black lh-20 fw-medium">Current Password</label>
                                <input class="form-control form--control password-field" type="password" name="password"
                                    placeholder="Current password">
                            </div>
                            <div class="form-group">
                                <label class="fs-13 text-black lh-20 fw-medium">New Password</label>
                                <input class="form-control form--control password-field" type="password" name="password"
                                    placeholder="New password">
                            </div>
                            <div class="form-group">
                                <label class="fs-13 text-black lh-20 fw-medium">New Password (again)</label>
                                <input class="form-control form--control password-field" type="password" name="password"
                                    placeholder="New password again">
                                <p class="fs-14 lh-18 py-2">Passwords must contain at least eight characters, including
                                    at
                                    least 1 letter and 1 number.</p>
                                <button class="btn theme-btn-outline theme-btn-outline-gray toggle-password"
                                    type="button" data-toggle="tooltip" data-placement="right"
                                    title="Show/hide password">
                                    <svg class="eye-on" xmlns="http://www.w3.org/2000/svg" height="22px"
                                        viewBox="0 0 24 24" width="22px" fill="#7f8897">
                                        <path d="M0 0h24v24H0V0z" fill="none" />
                                        <path
                                            d="M12 6c3.79 0 7.17 2.13 8.82 5.5C19.17 14.87 15.79 17 12 17s-7.17-2.13-8.82-5.5C4.83 8.13 8.21 6 12 6m0-2C7 4 2.73 7.11 1 11.5 2.73 15.89 7 19 12 19s9.27-3.11 11-7.5C21.27 7.11 17 4 12 4zm0 5c1.38 0 2.5 1.12 2.5 2.5S13.38 14 12 14s-2.5-1.12-2.5-2.5S10.62 9 12 9m0-2c-2.48 0-4.5 2.02-4.5 4.5S9.52 16 12 16s4.5-2.02 4.5-4.5S14.48 7 12 7z" />
                                    </svg>
                                    <svg class="eye-off" xmlns="http://www.w3.org/2000/svg" height="22px"
                                        viewBox="0 0 24 24" width="22px" fill="#7f8897">
                                        <path d="M0 0h24v24H0V0zm0 0h24v24H0V0zm0 0h24v24H0V0zm0 0h24v24H0V0z"
                                            fill="none" />
                                        <path
                                            d="M12 6c3.79 0 7.17 2.13 8.82 5.5-.59 1.22-1.42 2.27-2.41 3.12l1.41 1.41c1.39-1.23 2.49-2.77 3.18-4.53C21.27 7.11 17 4 12 4c-1.27 0-2.49.2-3.64.57l1.65 1.65C10.66 6.09 11.32 6 12 6zm-1.07 1.14L13 9.21c.57.25 1.03.71 1.28 1.28l2.07 2.07c.08-.34.14-.7.14-1.07C16.5 9.01 14.48 7 12 7c-.37 0-.72.05-1.07.14zM2.01 3.87l2.68 2.68C3.06 7.83 1.77 9.53 1 11.5 2.73 15.89 7 19 12 19c1.52 0 2.98-.29 4.32-.82l3.42 3.42 1.41-1.41L3.42 2.45 2.01 3.87zm7.5 7.5l2.61 2.61c-.04.01-.08.02-.12.02-1.38 0-2.5-1.12-2.5-2.5 0-.05.01-.08.01-.13zm-3.4-3.4l1.75 1.75c-.23.55-.36 1.15-.36 1.78 0 2.48 2.02 4.5 4.5 4.5.63 0 1.23-.13 1.77-.36l.98.98c-.88.24-1.8.38-2.75.38-3.79 0-7.17-2.13-8.82-5.5.7-1.43 1.72-2.61 2.93-3.53z" />
                                    </svg>
                                </button>
                            </div>
                            <div class="submit-btn-box pt-3">
                                <button class="btn theme-btn" type="button">Change Password</button>
                            </div>
                        </div>
                        <div class="border border-gray p-4">
                            <h4 class="fs-18 mb-2">Forgot your password</h4>
                            <p class="pb-3">Don't worry it's happen with everyone. We'll help you to get back your
                                password
                            </p>
                            <a href="recover-password.html" class="btn theme-btn theme-btn-sm theme-btn-white">Recover
                                Password <i class="la la-arrow-right ml-1"></i></a>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </section>
</template>