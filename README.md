# 🎬 Cinematixx - Movie Ticket Booking Website

Cinematixx is a simple yet interactive front-end website project that simulates a movie ticket booking system. Built using HTML, CSS, and vanilla JavaScript, the platform allows users to browse movie selections, view trailers, and make ticket bookings through a dynamic booking form. This project demonstrates core front-end development practices and JavaScript logic implementation in a real-world use case: cinema ticketing.

---

## 🌟 Features

- 🎥 **Movie Thumbnails**: Movies are showcased using a combination of Bootstrap jumbotron and container components, giving a clean and modern look.
- ▶️ **Watch Trailers**: Embedded YouTube trailers are displayed using `<iframe>` to allow users to preview movies directly from the website.
- 📝 **Booking System**: A booking page where users can:
  - Choose ticket packages
  - Input number of attendees
  - View total payment instantly
  - Trigger a thank-you message and redirect after booking

Example JavaScript logic used:
```javascript
function goToBooking(){
    window.location.assign("bookingform.html");
}
function process(){
    var package = document.getElementById('package').value;
    var num_of_people = document.getElementById('num-of-people').value;
    var totalPayment = package * num_of_people;
    document.getElementById('total').innerHTML = totalPayment;
    setTimeout(() => {
        alert('Thank you for purchasing!');
        window.location.assign('about.html');
    }, 1000);
}
