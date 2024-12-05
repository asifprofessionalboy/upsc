<style>
        body{
            overflow-x:hidden;
        }
          .mycontainer {
      position: absolute;
      top: 75%;
      left: 80px;
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
      padding: 10px 5px;
      border-radius: 6px;
      box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
      transform: translateX(555%); /* Hide off-screen */
      transition: all 0.5s cubic-bezier(0.68, -0.55, 0.265, 1.55);
      position: absolute;
      right: -100%;
    }

    .close-btn.open ~ .media-icons {
      transform: translateX(0); /* Bring it back into view */
      right: -10px;
             margin-bottom:50px
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
      background-color: #0c4aaf;
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
      top: -10px;
      right: -10px;
      background-color: #f9232e;
      color: #fff;
      font-size: 12px;
      font-weight: 500;
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

        body{
            overflow-x:hidden;
        }

      .mycontainer {
        top: 60%;
        left: 150px;
        transform: translateY(0);
        align-items: flex-start;
      }

      .media-icons {
        transform: translateX(515%);
        padding: 4px;
        right: -150%;
        margin-bottom:50px;
      }

      .close-btn.open ~ .media-icons {
        transform: translateX(0);
        right: -6px;
 
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


<div class="mycontainer">
    <span class="close-btn">
      <i class="fa-solid fa-xmark"></i>
    </span>
    <div class="media-icons">
      <a href="#" style="background: #bfb434">
<i class="fa-solid fa-ban"></i>
        <span class="badge">5</span>
        <span class="tooltip" style="color: #bfb434">Blocked/UnBlocked</span>
      </a>
      <a href="#" style="background: #0e76a8">
    <i class="fa-solid fa-circle-exclamation"></i>
        <span class="badge">3</span>
        <span class="tooltip" style="color: #0e76a8">Grievance</span>
      </a>
      <a href="#" style="background: #23b6cd">
  <i class="fa-solid fa-building-columns"></i>
        <span class="badge">7</span>
        <span class="tooltip" style="color: #23b6cd">Government</span>
      </a>
 
    </div>


                   </div>


  <script>
                               const closeBtn = document.querySelector(".close-btn");
                               closeBtn.addEventListener("click", () => {
                                   closeBtn.classList.toggle("open");
                               });
                           </script>
