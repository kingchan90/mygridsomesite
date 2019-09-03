<template>
  <header id="header">
    <div class="nav-wrapper">
      <div class="container">
        <div class="row">
          <nav class="navbar navbar-expand-lg col-12">
            <a class="navbar-brand" href="/en_UK" title="Home">
              <g-image class="img-fluid" src="~/img/upload/main-logo.png" alt="Bright Beauty" />
            </a>
            <button
              class="navbar-toggler"
              type="button"
              data-target="#navbarSupportedContent"
              aria-controls="navbarSupportedContent"
              aria-expanded="false"
              aria-label="Toggle navigation"
            >
              <span></span>
              <span></span>
              <span></span>
            </button>
            <div class="navbar-collapse" id="navbarSupportedContent">
              <ul class="navbar-nav mr-lg-0 ml-lg-auto align-items-center">
                <li class="nav-item">
                  <a class="nav-link" href="/en_UK/technology.html" title="Our Technology">
                    <span>Our Technology</span>
                  </a>
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="/en_UK/products.html" title="Our Products">
                    <span>Our Products</span>
                  </a>
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="/en_UK/career.html" title="Your Career">
                    <span>Your Career</span>
                  </a>
                </li>
                <li class="nav-item">
                  <a
                    class="nav-link text-center"
                    href="/en_UK/partnership.html"
                    title="Partnership &lt;br&gt;Opportunities"
                  >
                    <span>
                      Partnership
                      <br />Opportunities
                    </span>
                  </a>
                </li>
                <li class="nav-item">
                  <a
                    class="nav-link text-center"
                    href="/en_UK/contact.html"
                    title="Curious?&lt;br&gt; Contact Us"
                  >
                    <span>
                      Curious?
                      <br />Contact Us
                    </span>
                  </a>
                </li>
              </ul>
              <div class="dropdown dropdown-lang">
                <a
                  class="dropdown-toggle"
                  href="#"
                  role="button"
                  data-toggle="dropdown"
                  aria-haspopup="true"
                  aria-expanded="false"
                  id="navbarDropdown"
                >
                  <span class="en dropdown-item d-inline-block w-auto">English</span>
                </a>
                <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                  <a class="cn dropdown-item" href="/zh_CN/" title="中文">
                    <span>中文</span>
                  </a>
                </div>
              </div>
            </div>
          </nav>
        </div>
      </div>
    </div>
  </header>
</template>
<script>
export default {};
</script>