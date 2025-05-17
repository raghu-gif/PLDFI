document.getElementById('contactForm').addEventListener('submit', function (event) {
  event.preventDefault();

  const name = this.name.value.trim();
  const email = this.email.value.trim();
  const message = this.message.value.trim();
  const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

  if (!name || !email || !message) {
    alert('Please fill in all required fields.');
    return;
  }

  if (!emailPattern.test(email)) {
    alert('Please enter a valid email address.');
    return;
  }

  alert(`Thank you for reaching out, ${name}. We will get back to you soon!`);
  this.reset();
});
