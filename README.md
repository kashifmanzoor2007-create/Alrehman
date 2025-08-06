# Alrehman
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Online Classes</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background-color: #f4f4f4;
    }

    header {
      background-color: #333;
      color: white;
      padding: 20px 0;
      text-align: center;
    }

    .container {
      padding: 40px;
      text-align: center;
    }

    .btn {
      background-color: #007BFF;
      border: none;
      color: white;
      padding: 14px 28px;
      font-size: 16px;
      cursor: pointer;
      border-radius: 5px;
    }

    .btn:hover {
      background-color: #0056b3;
    }

    /* Modal Styling */
    .modal {
      display: none;
      position: fixed;
      z-index: 999;
      padding-top: 100px;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      overflow: auto;
      background-color: rgba(0,0,0,0.6);
    }

    .modal-content {
      background-color: #fff;
      margin: auto;
      padding: 30px;
      border: 1px solid #888;
      width: 90%;
      max-width: 500px;
      border-radius: 10px;
    }

    .close {
      color: #aaa;
      float: right;
      font-size: 24px;
      font-weight: bold;
    }

    .close:hover,
    .close:focus {
      color: black;
      text-decoration: none;
      cursor: pointer;
    }

    input[type="text"],
    input[type="email"],
    input[type="tel"],
    input[type="date"],
    select {
      width: 100%;
      padding: 10px;
      margin: 10px 0 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    .form-group {
      text-align: left;
    }

    .form-group label {
      display: block;
      margin-bottom: 5px;
    }

    .checkbox-group, .radio-group {
      margin-bottom: 15px;
    }

    .checkbox-group label, .radio-group label {
      margin-right: 10px;
    }

    .submit-btn {
      background-color: #28a745;
    }

    .submit-btn:hover {
      background-color: #218838;
    }
  </style>
</head>
<body>

<header>
  <h1>Welcome to Online Learning</h1>
  <p>Learn Skills to Boost Your Career</p>
</header>

<div class="container">
  <h2>Join Our Popular Courses</h2>
  <p>Enroll in AI, Web Development, Social Media, and more.</p>
  <button class="btn" id="openModalBtn">Register Now</button>
</div>

<!-- Modal -->
<div id="registrationModal" class="modal">
  <div class="modal-content">
    <span class="close" id="closeModalBtn">&times;</span>
    <h2>Registration Form</h2>
    <form>
      <div class="form-group">
        <label for="name">Full Name:</label>
        <input type="text" id="name" name="name" required>
      </div>

      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
      </div>

      <div class="form-group">
        <label for="phone">Phone:</label>
        <input type="tel" id="phone" name="phone" required>
      </div>

      <div class="form-group">
        <label for="dob">Date of Birth:</label>
        <input type="date" id="dob" name="dob" required>
      </div>

      <div class="form-group radio-group">
        <label>Gender:</label>
        <label><input type="radio" name="gender" value="male" required> Male</label>
        <label><input type="radio" name="gender" value="female"> Female</label>
        <label><input type="radio" name="gender" value="other"> Other</label>
      </div>

      <div class="form-group checkbox-group">
        <label>Select Courses:</label>
        <label><input type="checkbox" name="course" value="basic-computer"> Basic Computer</label><br>
        <label><input type="checkbox" name="course" value="ai"> AI</label><br>
        <label><input type="checkbox" name="course" value="shopify"> Shopify</label><br>
        <label><input type="checkbox" name="course" value="wordpress"> WordPress</label><br>
        <label><input type="checkbox" name="course" value="smm"> Social Media Management</label>
      </div>

      <button type="submit" class="btn submit-btn">Submit</button>
    </form>
  </div>
</div>

<script>
  // Modal open/close functionality
  const modal = document.getElementById("registrationModal");
  const openBtn = document.getElementById("openModalBtn");
  const closeBtn = document.getElementById("closeModalBtn");

  openBtn.onclick = () => modal.style.display = "block";
  closeBtn.onclick = () => modal.style.display = "none";
  window.onclick = (event) => {
    if (event.target === modal) {
      modal.style.display = "none";
    }
  }
</script>

</body>
</html>
