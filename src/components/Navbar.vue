<template>
    <div class="navbar">
        <nav>
            <div class="navbar_header">
                <p>3D</p>
            </div>
            <ul class="nav-links">
                <li class="navlink"><router-link to="/"><i class="fa fa-home mr-2" aria-hidden="true"></i>Home</router-link></li>
                <li class="navlink"><router-link to="/products"><i class="fa fa-cube mr-2" aria-hidden="true"></i>Products</router-link></li>
                <li class="navlink" v-b-modal.modal-scrollable1><i class="fa fa-envelope mr-2" aria-hidden="true"></i>Contact</li>
            </ul>
            <b-modal id="modal-scrollable1" scrollable size="xl" hide-footer>
                <section class="ftco-section">
                    <div class="container">
                        <div class="row justify-content-center ">
                            <div class="col-lg-10 col-md-12 ">
                                <div class="wrapper">
                                    <div class="row no-gutters  shadow ">
                                        <div class="col-md-7 d-flex align-items-stretch">
                                            <div class="contact-wrap w-100 p-md-5 p-4">
                                                <h3 class="mb-4">Get in touch</h3>
                                                <div id="form-message-warning" class="mb-4"></div>
                                                <div id="form-message-success" class="mb-4">
                                                    Your message was sent, thank you!
                                                </div>
                                                <form method="POST" id="contactForm" name="contactForm">
                                                    <div class="row">
                                                        <div class="col-md-6">
                                                            <div class="form-group">
                                                                <input type="text" class="form-control" name="name" id="name" placeholder="Name" />
                                                            </div>
                                                        </div>
                                                        <div class="col-md-6">
                                                            <div class="form-group">
                                                                <input type="email" class="form-control" name="email" id="email" placeholder="Email" />
                                                            </div>
                                                        </div>
                                                        <div class="col-md-12">
                                                            <div class="form-group">
                                                                <input type="text" class="form-control" name="subject" id="subject" placeholder="Subject" />
                                                            </div>
                                                        </div>
                                                        <div class="col-md-12">
                                                            <div class="form-group">
                                                                <textarea name="message" class="form-control" id="message" cols="30" rows="7" placeholder="Message"></textarea>
                                                            </div>
                                                        </div>
                                                        <div class="col-md-12">
                                                            <div class="form-group">
                                                                <input type="submit" value="Send Message" class="btn btn-primary" />
                                                                <div class="submitting"></div>
                                                            </div>
                                                        </div>
                                                    </div>
                                                </form>
                                            </div>
                                        </div>
                                        <div class="col-md-5 d-flex align-items-stretch ">
                                            <div class="info-wrap bg-primary w-100 p-lg-5 p-4">
                                                <h3 class="mb-4 mt-md-4">Contact us</h3>
                                                <div class="dbox w-100 d-flex align-items-start">
                                                    <div class="icon d-flex align-items-center justify-content-center">
                                                        <span class="fa fa-map-marker"></span>
                                                    </div>
                                                    <div class="text pl-3">
                                                        <p><span>Address:</span> Basni </p>
                                                    </div>
                                                </div>
                                                <div class="dbox w-100 d-flex align-items-center">
                                                    <div class="icon d-flex align-items-center justify-content-center">
                                                        <span class="fa fa-phone"></span>
                                                    </div>
                                                    <div class="text pl-3">
                                                        <p><span>Phone:</span> <a href="tel://1234567920">+ 1235 2355 98</a></p>
                                                    </div>
                                                </div>
                                                <div class="dbox w-100 d-flex align-items-center">
                                                    <div class="icon d-flex align-items-center justify-content-center">
                                                        <span class="fa fa-paper-plane"></span>
                                                    </div>
                                                    <div class="text pl-3">
                                                        <p><span>Email:</span> <a href="mailto:info@yoursite.com">info@yoursite.com</a></p>
                                                    </div>
                                                </div>
                                                <div class="dbox w-100 d-flex align-items-center">
                                                    <div class="icon d-flex align-items-center justify-content-center">
                                                        <span class="fa fa-globe"></span>
                                                    </div>
                                                    <div class="text pl-3">
                                                        <p><span>Website</span> <a href="#">yoursite.com</a></p>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>
            </b-modal>
        </nav>
    </div>
</template>

<style lang="scss" scoped>
@import "bootstrap/bootstrap";
@import "bootstrap/variables";
@import "bootstrap/mixins";
$font-primary: "Poppins", Arial, sans-serif;
$primary: #1089ff;


.bg-primary {
    background: $primary !important;
}

.ftco-section {
    padding: 7em 0;
}

.ftco-no-pt {
    padding-top: 0;
}
.ftco-no-pb {
    padding-bottom: 0;
}
//HEADING SECTION
.heading-section {
    font-size: 28px;
    color: $black;
}

//COVER BG
.img {
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
}

.form-control {
    height: 52px;
    background: $white;
    color: $black;
    font-size: 14px;
    border-radius: 2px;
    box-shadow: none !important;
    border: 1px solid rgba(0, 0, 0, 0.1);
    &::-webkit-input-placeholder {
        /* Chrome/Opera/Safari */
        color: rgba(0, 0, 0, 0.7) !important;
    }
    &::-moz-placeholder {
        /* Firefox 19+ */
        color: rgba(0, 0, 0, 0.7) !important;
    }
    &:-ms-input-placeholder {
        /* IE 0+ */
        color: rgba(0, 0, 0, 0.7) !important;
    }
    &:-moz-placeholder {
        /* Firefox 18- */
        color: rgba(0, 0, 0, 0.7) !important;
    }
    &:focus,
    &:active {
        border-color: rgba(0, 0, 0, 0.1);
    }
}
textarea.form-control {
    height: inherit !important;
}

.wrapper {
    width: 100%;
    -webkit-box-shadow: 0px 21px 41px -13px rgba(0, 0, 0, 0.18);
    -moz-box-shadow: 0px 21px 41px -13px rgba(0, 0, 0, 0.18);
    box-shadow: 0px 21px 41px -13px rgba(0, 0, 0, 0.18);
}
.contact-wrap {
    background: $white;
}

.info-wrap {
    h3 {
        color: $white;
    }
    .dbox {
        width: 100%;
        color: rgba(255, 255, 255, 0.8);
        margin-bottom: 25px;
        &:last-child() {
            margin-bottom: 0;
        }
        p {
            margin-bottom: 0;
            span {
                font-weight: 600;
                color: $white;
            }
            a {
                color: $white;
            }
        }
        .icon {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            span {
                font-size: 20px;
                color: $white;
            }
        }
        .text {
            width: calc(100% - 50px);
        }
    }
    @include media-breakpoint-up(lg) {
        margin-top: -20px;
        margin-bottom: -20px;
        border-radius: 5px;
    }
}

.btn {
    padding: 12px 16px;
    cursor: pointer;
    border-width: 1px;
    border-radius: 5px;
    font-size: 14px;
    font-weight: 400;
    -webkit-box-shadow: 0px 10px 20px -6px rgba(0, 0, 0, 0.12);
    -moz-box-shadow: 0px 10px 20px -6px rgba(0, 0, 0, 0.12);
    box-shadow: 0px 10px 20px -6px rgba(0, 0, 0, 0.12);
    position: relative;
    margin-bottom: 20px;
    @include transition(0.3s);
    &:hover,
    &:active,
    &:focus {
        outline: none !important;
        -webkit-box-shadow: 0px 10px 20px -6px rgba(0, 0, 0, 0.22) !important;
        -moz-box-shadow: 0px 10px 20px -6px rgba(0, 0, 0, 0.22) !important;
        box-shadow: 0px 10px 20px -6px rgba(0, 0, 0, 0.22) !important;
    }
    &.btn-primary {
        background: $primary !important;
        border-color: $primary !important;
        color: $white;
        &:hover,
        &:focus {
            border-color: darken($primary, 10%) !important;
            background: darken($primary, 10%) !important;
        }
    }
}

//Forms style
#contactForm {
    .error {
        color: red;
        font-size: 12px;
    }
    .form-control {
        font-size: 16px;
    }
}
#message {
    resize: vertical;
}
#form-message-warning,
#form-message-success {
    display: none;
}
#form-message-warning {
    color: red;
}
#form-message-success {
    color: $success;
    font-size: 18px;
    font-weight: bold;
}
.submitting {
    float: left;
    width: 100%;
    padding: 10px 0;
    display: none;
    font-size: 16px;
    font-weight: bold;
}

.navbar {
    background: #121212;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    margin: 0;
    padding: 0;
    height: max-content;
    z-index: 1;
    transition: all 0.5s ease-in-out;
}

nav {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 100%;
}

.navbar_header {
    margin-left: 2em;
}

.navbar_header p {
    font-size: 2.5em;
    font-weight: 500;
    margin: 0;
    padding: 0;
    color: orange;
}

.nav-links {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    margin: 0;
    padding: 0;
    /* width: 100%; */
}

ul {
    list-style: none;
}

ul.nav-links li {
    margin: auto 3vw;
    color:#fff;
}
ul.nav-links li:hover {
    border-bottom: 2px solid #fff;
}

ul.nav-links li a {
    text-decoration: none;
    color: white;
}

ul li a:hover {
    color: white;
}

ul li button {
    background: none;
    border: none;
    outline: none;
    color: white;
}

@media screen and (max-width: 576px) {
    nav {
        font-size: 80%;
    }
}

@media screen and (max-width: 400px) {
    nav {
        display: block;
        align-items: center;
        justify-content: center;
        text-align: center;
        margin: auto;
        width: 100%;
        padding-bottom:5px;
    }

    .navbar_header {
        margin-left: 0;
    }

    ul.nav-links {
        width: 100%;
        margin: auto;
    }

    ul.nav-links li {
        margin: auto;
        padding: 0;
    }
}
</style>
