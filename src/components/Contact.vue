<template>
  <div id="contact">
    <h2>{{ Contact.title }}</h2>
    <div class="Contact__Content">
      <!-- Content -->
      <div class="Contact__Info">
        <p>{{ Contact.description }}</p>
        <ul class="Contact__SocialMedia__Icons">
          <li v-for="item in SocialMedia.items" :key="item.name">
            <a :href="item.link">
              <g-image immediate="true" :alt="item.name" :src="'/images/' + item.name + '.svg'" />
            </a>
          </li>
        </ul>
      </div>
      <!-- Form -->
      <div class="Contact__Form">
        <form
          action="/success"
          name="contact"
          motheod="post"
          data-netlify="true"
          data-netlify-honeypot="bot-field"
        >
          <input type="hidden" name="form-name" value="contact" />
          <p hidden>
            <label>
              Don’t fill this out:
              <input name="bot-field" />
            </label>
          </p>
          <label for="name">Name</label>
          <input type="name" placeholder="Incognito" v-model="formData.name" />

          <label for="email">Email</label>
          <input type="email" placeholder="incognito@email.com" v-model="formData.email" />

          <label for="message">Message</label>
          <textarea type="message" placeholder="Your message..." v-model="formData.message" />
          <button type="submit">Submit</button>
        </form>
        {{this.formData }}
      </div>
    </div>
  </div>
</template>

<script>
import Contact from "~/data/Contact.yml";
import SocialMedia from "~/data/SocialMedia.yml";

export default {
  data() {
    return {
      formData: {}
    };
  },
  computed: {
    Contact() {
      return Contact;
    },
    SocialMedia() {
      return SocialMedia;
    }
  },
  methods: {
    encode(data) {
      return Object.keys(data)
        .map(
          key => encodeURIComponent(key) + "=" + encodeURIComponent(data[key])
        )
        .join("&");
    },
    handleSubmit(e) {
      fetch("/", {
        method: "POST",
        headers: {
          "Content-Type": "application/x-www-form-urlencoded",
          "Access-Control-Allow-Origin": "*"
        },
        mode: "no-cors",
        body: this.encode({
          "form-name": e.target.getAttribute("name"),
          ...this.formData
        })
      })
        .then(() => this.$router.push("/success"))
        .catch(error => alert(error));
    }
  }
};
</script>

<style lang="sass" scoped>
	#contact
		padding: 30px 0

		h2
			margin-bottom: 15px

		.Contact__Info
			margin-right: 2rem
			margin-bottom: 2rem

		.Contact__Form

			form
				flex-direction: column
				display: flex

				*
					font:
						family: 'Nunito', sans-serif
						size: 16px

				label
					font:
						size: 12px
						weight: 700
					margin-bottom: 20px
					text-transform: uppercase

				input
					margin-bottom: 20px

				input, textarea
					border: none
					border-bottom: 1px solid #CFCFCF
					outline: none
					padding-bottom: 10px
					color: #CFCFCF

				textarea
					height: 60px
					resize: none

				button
					margin-top: 30px
					padding: 15px
					width: 100%
					border: none
					border-radius: 50px
					cursour: pointer
					font-size: 16px
					font-weight: 700
					text-transform: uppercase
					background-color: #CFCFCF
					color: white
					transition: 0.2s

					&:hover
						background-color: #4DBA87
					
	.Contact__SocialMedia__Icons
		display: flex
		flex-direction: row
		margin-top: 20px

		li
			padding-right: 15px

			img
				width: 15px
				height: 15px

	@media (min-width: 576px)
		.Contact__Content
			display: flex
			flex-direction: row

		.Contact__Info
			width: 25%

		.Contact__Form
			width: 70%
</style>

