const toggleBtn = document.querySelector(".toggle-btn");
const mediaIcons = document.querySelector(".media-icons");

// Add click event for toggle functionality
toggleBtn.addEventListener("click", () => {
    toggleBtn.classList.toggle("open"); // Animate plus-to-X
    mediaIcons.classList.toggle("open"); // Show/hide media icons
});


/* Body style to prevent scrolling issues */
body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    overflow-x: hidden;
}

/* Main container positioning */
.mycontainer {
    position: absolute;
    top: 50%;
    left: 20px;
    transform: translateY(-50%);
    display: flex;
    flex-direction: column-reverse;
    align-items: center;
}

/* Button (toggle) styling */
.toggle-btn {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 50px;
    width: 50px;
    border-radius: 50%;
    background-color: #0c4aaf;
    color: #fff;
    font-size: 24px;
    cursor: pointer;
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
    transition: all 0.4s ease-in-out;
}

/* Plus-to-X animation */
.toggle-btn.open {
    transform: rotate(45deg);
    background-color: #de0611;
    transition: all 0.4s ease-in-out;
}

/* Media icons container */
.media-icons {
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    justify-content: center;
    background-color: #fff;
    padding: 10px 5px;
    border-radius: 6px;
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
    position: absolute;
    transform-origin: top left;
    transform: scale(0);
    opacity: 0;
    transition: transform 0.5s ease, opacity 0.5s ease;
}

/* Open state of media icons */
.media-icons.open {
    transform: scale(1);
    opacity: 1;
}

/* Individual media icons styling */
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

/* Tooltip styling */
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

/* Responsive design for mobile */
@media screen and (max-width: 768px) {
    .toggle-btn {
        height: 40px;
        width: 40px;
        font-size: 20px;
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

    .badge {
        font-size: 10px;
        padding: 1px 4px;
        top: -5px;
        right: -5px;
    }
}


<div class="mycontainer">
    <span class="toggle-btn">
        <i class="fa-solid fa-plus"></i>
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
