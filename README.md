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


body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    overflow-x: hidden;
}

.mycontainer {
    position: absolute;
    top: 75%;
    left: 80px;
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
    position: absolute;
    right: 0;
    transform-origin: top right;
    transform: scale(0);
    opacity: 0;
    transition: transform 0.5s ease, opacity 0.5s ease;
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
    transition: all 0.5s ease;
}

.close-btn.open {
    background-color: #de0611;
}

.media-icons.open {
    transform: scale(1);
    opacity: 1;
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

@media screen and (max-width: 768px) {
    .mycontainer {
        top: 60%;
        left: 50px;
        align-items: flex-start;
    }

    .close-btn {
        height: 30px;
        width: 30px;
        font-size: 16px;
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
        top: -3px;
        right: -3px;
    }
}

const closeBtn = document.querySelector(".close-btn");
const mediaIcons = document.querySelector(".media-icons");

closeBtn.addEventListener("click", () => {
    closeBtn.classList.toggle("open");
    mediaIcons.classList.toggle("open");
});
