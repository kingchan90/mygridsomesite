<template>
  <footer id="footer">
    <div class="footer-top">
      <div class="container">
        <div class="row">
          <div class="col">
            <ul class="footer-links">
              <li>
                <a
                  class="footer-link text-white"
                  href="/en_UK/technology.html"
                  title="Our Technology"
                >
                  <span>Our Technology</span>
                </a>
              </li>
              <li>
                <a class="footer-link text-white" href="/en_UK/products.html" title="Our Products">
                  <span>Our Products</span>
                </a>
              </li>
              <li>
                <a class="footer-link text-white" href="/en_UK/career.html" title="Your Career">
                  <span>Your Career</span>
                </a>
              </li>
              <li>
                <a
                  class="footer-link text-white"
                  href="/en_UK/partnership.html"
                  title="Partnership Opportunities"
                >
                  <span>Partnership Opportunities</span>
                </a>
              </li>
              <li>
                <a
                  class="footer-link text-white"
                  href="/en_UK/contact.html"
                  title="Curious? Contact Us"
                >
                  <span>Curious? Contact Us</span>
                </a>
              </li>
            </ul>
            <div class="footer-social">
              <p class="text-mute pb-2">Learn More On Our Social Media</p>
              <a
                class="footer-social-link mr-4 float-left"
                href="#"
                title
                data-toggle="modal"
                data-target="#wechat"
              >
                <g-image src="~/img/wechat-icon.svg" />
              </a>
              <a
                class="footer-social-link mr-4 float-left"
                href="#"
                title
                data-toggle="modal"
                data-target="#miniprogram"
              >
                <g-image src="~/img/progam-icon.svg" />
              </a>
              <a
                class="footer-social-link mr-4 float-left"
                href="https://weibo.com/u/6798033349"
                title
                target="_blank"
              >
                <g-image src="~/img/weibo-icon.svg" />
              </a>
              <a
                class="footer-social-link mr-4 float-left"
                href=" https://www.linkedin.com/company/brighterbeauty/"
                title
                target="_blank"
              >
                <g-image src="~/img/linkedin-icon.svg" />
              </a>
            </div>
          </div>
          <div class="col-sm-auto text-sm-right">
            <div class="footer-qr d-inline-block">
              <g-image class="img-fluid" src="~/img/upload/qr-code.jpg" alt />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="container">
        <div class="row">
          <div class="col-md-auto">
            <div class="row align-items-center h-100">
              <div
                class="copyright mr-0 col-md-auto col-12 d-block"
              >Copyright © 2017-2019 BrighterBeauty™</div>
              <a
                class="col-12 col-md-auto d-block"
                href="http://www.beian.miit.gov.cn/"
                title="沪ICP备18043705号-1"
                target="_blank"
              >
                <span>沪ICP备18043705号-1</span>
              </a>
              <a
                class="col-12 mt-3 mt-md-0 col-md-auto d-block"
                href="/zh_CN/term-and-condition.html"
                title="Terms and Conditions"
              >
                <span>Terms and Conditions</span>
              </a>
              <a
                class="mt-3 mt-md-0 col-md-auto col-12 d-block"
                href="/zh_CN/policy.html"
                title="Privacy Policy"
              >
                <span>Privacy Policy</span>
              </a>
            </div>
          </div>
          <div class="col mr-0 ml-auto">
            <div class="dropdown dropdown-lang">
              <a
                class="dropdown-toggle"
                href="#"
                role="button"
                data-toggle="dropdown"
                aria-haspopup="true"
                aria-expanded="false"
                id="footerDropdown"
              >
                <span class="en dropdown-item d-inline-block w-auto">English</span>
              </a>
              <div class="dropdown-menu" aria-labelledby="footerDropdown">
                <a class="cn dropdown-item" href="/zh_CN/" title="中文">
                  <span>中文</span>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div
      class="qr-code-modal modal fade"
      tabindex="-1"
      role="dialog"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
      id="miniprogram"
    >
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <button class="close" type="button" data-dismiss="modal" aria-label="Close">
              <span class="text-violet" aria-hidden="true"></span>
            </button>
          </div>
          <div class="modal-body">
            <g-image class="d-block ml-auto mr-auto" src="~/img/upload/qr-code.jpg" alt />
          </div>
        </div>
      </div>
    </div>
    <div
      class="qr-code-modal modal fade"
      tabindex="-1"
      role="dialog"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
      id="wechat"
    >
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <button class="close" type="button" data-dismiss="modal" aria-label="Close">
              <span class="text-violet" aria-hidden="true"></span>
            </button>
          </div>
          <div class="modal-body">
            <g-image class="d-block ml-auto mr-auto" src="~/img/upload/qr-code-wechat.jpg" alt />
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
<script>
export default {};
</script>
<style lang="scss">
#footer {
  background: $blue;
  font-family: $font-family-primary;
  color: $white;
  .dropdown.dropdown-lang {
    padding: 0;
    max-width: 13rem;
    > a {
      padding: 1rem 1.5rem 12px;
      display: block;
    }
    &.show > a {
      background: $grey-light;
    }
    &:before {
      content: none;
    }
  }
  .dropdown-menu {
    transform: none !important; //overide js styles
    bottom: 100%;
    top: auto !important; //overide js styles
  }
}
.footer {
  &-links {
    padding-top: 1rem;
    .active {
      text-decoration: underline;
    }
    > li {
      display: inline-block;
      margin-right: 3.9rem;
    }
  }
  &-qr {
    max-width: 14rem;
  }
  &-social {
    margin-top: 2.9rem;
    &-link {
      @include round(3.5rem);
      background: $white;
    }
  }
  &-top {
    padding: 5rem 0;
  }
  &-bottom {
    padding: 1.7rem 0;
    background: $blue-dark;
    font-family: $font-family-primary;
    font-size: $font-size-xxs;
    .dropdown-lang {
      margin-left: 0;
    }
    .dropdown-toggle:hover {
      color: inherit;
    }
    .copyright {
      float: left;
      margin-right: 3rem;
    }
  }
}
@media #{$tablet} {
  .footer {
    &-links {
      > li {
        display: block;
        + li {
          margin-left: 0;
          margin-top: 1.5rem;
        }
      }
    }
  }
}
@media #{$mobile-small} {
  .footer {
    &-qr {
      margin-top: 2.5rem;
    }
    &-bottom {
      .copyright {
        float: none;
        margin-bottom: 2rem;
        margin-right: 0;
      }
      .dropdown {
        margin-top: 2rem;
        max-width: 150px;
        margin-left: -1.5rem;
      }
    }
  }
}
</style>