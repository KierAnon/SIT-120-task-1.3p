<template>
  <div class="contact">
    <h1>Contact me</h1>
    <form>
      <div class="form-group">
        <label>Your email address</label>
        <input type="email" placeholder="Enter your email">
      </div>
      <div class="form-group">
        <label>Your message</label>
        <textarea placeholder="Write your message here..."></textarea>
      </div>
      <button>Submit</button>
    </form>
  </div>
</template>

<style scoped>
.contact {
  font-family: 'Arial', sans-serif;
  max-width: 600px;
  margin: 40px auto;
  padding: 20px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  background-color: #f7f7f9;
  border-radius: 10px;
}

h1 {
  text-align: center;
  margin-bottom: 30px;
}

.form-group {
  margin-bottom: 20px;
}

label {
  display: block;
  margin-bottom: 10px;
}

input, textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #fff;
  resize: vertical; /* Allows users to resize the textarea vertically */
  transition: border 0.3s ease;

  &:focus {
    border-color: #007bff; /* Blue border on focus */
    outline: none;
  }
}

button {
  display: block;
  width: 100%;
  padding: 10px;
  background-color: #007bff; /* Blue background color */
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;

  &:hover {
    background-color: #0056b3; /* Darker blue on hover */
  }
}
</style>