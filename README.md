<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Icons with Badges</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    /* General Styles */
    body {
      margin: 0;
      padding: 0;
      overflow-x: hidden; /* Prevent horizontal scrolling */
      font-family: Arial, sans-serif;
    }

    .mycontainer {
      position: absolute;
      top: 50%;
      left: 0;
      transform: translateY(-50%);
      display: flex;
      flex-direction: column-reverse;
      align-items: center;
    }

    .media-icons {
      display: flex;
      align-items: flex-start;
      flex-direction: column;
      justify-content: center;
      background-color: #fff;
      padding: 6px;
      border-radius: 6px;
      box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
      transform: translateX(555%); /* Hide off-screen */
      transition: all 0.5s cubic-bezier(0.68, -0.55, 0.265, 1.55);
      position: absolute;
      right: -100%;
    }

    .close-btn.open ~ .media-icons {
      transform: translateX(0); /* Bring it back into view */
      right: 0;
    }

    .media-icons a {
      text-decoration: none;
      position: relative;
      height: 35px;
      width: 35px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 6px;
      margin: 6px;
    }

    .media-icons a i {
      color: #fff;
    }

    .media-icons a .tooltip {
      position: absolute;
      left: 55px;
      font-size: 14px;
      font-weight: 400;
      pointer-events: none;
      background-color: #fff;
      padding: 4px 8px;
      border-radius: 4px;
      transform: translateY(-25px);
      opacity: 0;
      transition: all 0.2s linear;
      box-shadow: 0 5px 10px rgba(0, 0, 0, 0.05);
    }

    a:hover .tooltip {
      opacity: 1;
      transform: translateY(0);
    }

    a .tooltip::before {
      content: "";
      position: absolute;
      height: 10px;
      width: 10px;
      top: 50%;
      left: -5px;
      transform: translateY(-50%) rotate(45deg);
      background-color: #fff;
    }

    .close-btn {
      display: flex;
      align-items: center;
      justify-content: center;
      height: 35px;
      width: 35px;
      border-radius: 50%;
      color: #fff;
      font-size: 18px;
      margin-top: 20px;
      background-color: #8e36ff;
      box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
      cursor: pointer;
      transform: rotate(45deg);
      transition: all 0.5s cubic-bezier(0.68, -0.55, 0.265, 1.55);
    }

    .close-btn.open {
      transform: rotate(90deg);
      background-color: #de0611;
    }

    /* Badge styling */
    .badge {
      position: absolute;
      top: -5px;
      right: -5px;
      background-color: #ff0000;
      color: #fff;
      font-size: 12px;
      font-weight: bold;
      padding: 2px 6px;
      border-radius: 50%;
      z-index: 1;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    }

    /* Ensure the badge stays on top of icons */
    .media-icons a {
      position: relative; /* Makes the badge positioning relative to the icon */
    }

    /* Responsive Design for Mobile */
    @media screen and (max-width: 768px) {
      .mycontainer {
        top: 10%;
        left: 10px;
        transform: translateY(0);
        align-items: flex-start;
      }

      .media-icons {
        transform: translateX(150%);
        padding: 4px;
        right: -150%;
      }

      .close-btn.open ~ .media-icons {
        transform: translateX(0);
        right: 10px;
      }

      .media-icons a {
        height: 30px;
        width: 30px;
        margin: 4px;
      }

      .media-icons a .tooltip {
        font-size: 12px;
        left: 45px;
        padding: 3px 6px;
      }

      .close-btn {
        height: 30px;
        width: 30px;
        font-size: 16px;
      }

      .badge {
        font-size: 10px;
        padding: 1px 4px;
        top: -3px;
        right: -3px;
      }
    }
  </style>
</head>
<body>
  <div class="mycontainer">
    <span class="close-btn">
      <i class="fa-solid fa-xmark"></i>
    </span>
    <div class="media-icons">
      <a href="#" style="background: #e60023">
        <i class="fa-brands fa-pinterest"></i>
        <span class="badge">5</span>
        <span class="tooltip" style="color: #e60023">Pinterest</span>
      </a>
      <a href="#" style="background: #0e76a8">
        <i class="fa-brands fa-linkedin"></i>
        <span class="badge">3</span>
        <span class="tooltip" style="color: #0e76a8">Linkedin</span>
      </a>
      <a href="#" style="background: #ff0000">
        <i class="fa-brands fa-youtube"></i>
        <span class="badge">7</span>
        <span class="tooltip" style="color: #ff0000">YouTube</span>
      </a>
      <a href="#" style="background: #ea4689">
        <i class="fa-brands fa-dribbble"></i>
        <span class="badge">2</span>
        <span class="tooltip" style="color: #ea4689">Dribbble</span>
      </a>
    </div>
  </div>
  <script>
    const closeBtn = document.querySelector(".close-btn");
    closeBtn.addEventListener("click", () => {
      closeBtn.classList.toggle("open");
    });
  </script>
</body>
</html>
