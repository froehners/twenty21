<template>
  <Layout>
    <div class="container">

      <div class="contact-header">
        <h1 class="contact-title">Get in Touch</h1>
        <p>Hi there! Fill out the form below or connect on <a href="https://www.linkedin.com/in/sfroehner/">LinkedIn</a>.</p>
      </div>

      <form class="contact-form" name="contact">

        <div class="sender-info">
          <div>
            <label for="name" class="label">Name</label>
            <input type="text" name="name" />
          </div>
          <div>
            <label for="email" class="label">Email address</label>
            <input type="email" name="email" />
          </div>
        </div>

        <div class="message">
          <label for="message" class="label">Message</label>
          <textarea name="message"></textarea>
        </div>

        <button class="button">Send it!</button>

      </form>

    </div>
  </Layout>
</template>

<script>
export default {}
</script>

<style scoped>
.contact-header {
  padding: 4rem 0 4rem 0;
}
.contact-title {
  font-family: 'Pirata One', cursive;
  font-weight: 400;
  font-size: 4rem;
  margin: 0 0 4rem 0;
  padding: 0;
}
.sender-info {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 2rem;
}
.sender-info > div {
  flex: 1;
  margin-right: 4rem;
}
.sender-info > div:last-of-type {
  margin: 0;
}
.label{
  font-size: 1.125rem;
}
input:focus,textarea:focus {
  border-color: var(--color-contrast-3);
}
input,textarea {
  background: var(--color-base-1);
  border: 1px solid var(--color-contrast-50);
  outline: none;
  border-radius: 0.3rem;
  padding: 0.8rem 1rem;
  color: inherit;
  font-size: 1rem;
  width: 100%;
}
textarea {
  resize: none;
  height: 140px;
}
.button {
  color: var(--color-contrast-1);
  background: var(--color-base-3);
  outline: none;
  border: 0;
  font-size: 1.5rem;
  padding: 0.8rem 1.6rem;
  border-radius: 0.3rem;
  margin-top: 2rem;
  cursor: pointer;
  transition: opacity 0.25s ease;
  font-weight: 500;
  font-family: 'Cabin', sans-serif;
}
.button:hover {
  opacity: 0.6;
}
.button:focus {
  border: 1px solid var(--color-contrast-2);
}
</style>

