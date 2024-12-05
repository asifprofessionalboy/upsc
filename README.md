      <script>
                               const closeBtn = document.querySelector(".close-btn");
                               closeBtn.addEventListener("click", () => {
                                   closeBtn.classList.toggle("open");
                               });
                           </script>


                       <div class="mycontainer">
      <span class="close-btn">
        <i class="fa-solid fa-xmark"></i>
      </span>
      <div class="media-icons">
        <a href="#" style="background: #e60023">
          <i class="fa-brands fa-pinterest"></i>
          <span class="tooltip" style="color: #e60023">Pinterest</span>
        </a>
        <a href="#" style="background: #0e76a8">
          <i class="fa-brands fa-linkedin"></i>
          <span class="tooltip" style="color: #0e76a8">Linkedin</span>
        </a>
        <a href="#" style="background: #ff0000">
          <i class="fa-brands fa-youtube"></i>
          <span class="tooltip" style="color: #ff0000">YouTube</span>
        </a>
        <a href="#" style="background: #ea4689">
          <i class="fa-brands fa-dribbble"></i>
          <span class="tooltip" style="color: #ea4689">Dribbble</span>
        </a>
        <a href="#" style="background: #8e36ff">
          <i class="fa-brands fa-github"></i>
          <span class="tooltip" style="color: #8e36ff">Github</span>
        </a>
        <a href="#" style="background: #4267b2">
          <i class="fa-brands fa-facebook-f"></i>
          <span class="tooltip" style="color: #4267b2">Facebook</span>
        </a>
        <a href="#" style="background: #1da1f2">
          <i class="fa-brands fa-twitter"></i>
          <span class="tooltip" style="color: #1da1f2">Twitter</span>
        </a>
      </div>
    </div>


<style>
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
  transform: translateX(555%);
  transition: all 0.5s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}
.close-btn.open ~ .media-icons {
  transform: translateX(0);
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
    </style>
