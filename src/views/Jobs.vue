<template>
    <MainHeader></MainHeader>
    <div class="jobs">
        <div class="sb-container">
            <h1 class="title">FIND <span class="red-text">JOBS</span></h1>
        </div>
        <div class="form-container">
            <form action="" id="job-form" class="job-search">
                <input type="text" class="jobs-fields" placeholder="Job Title">
                <input type="text" class="jobs-fields space-up" placeholder="City or Zip Code">
                <input type="submit" value="Search" class="red-bg submit-button space-up">
            </form>
        </div>
        <div class="go-table">
            <p class="main-font">OR</p>
            <a href="https://gogpac.jobs.net/en-US" target="blank" rel="nofollow" class="go-button">
                VISIT OUR JOB BOARD
                <i class='bx bx-right-arrow-alt'></i>
            </a>
        </div>
        <a href="#member"><i class='bx bx-chevron-down'></i></a>       
    </div>
    <div class="member-container" id="member">
        <div class="member-image">
            <img src="../assets/img/abby.png" alt="Abby" class="member-picture">
            <p class="member-name main-font"><strong class="red-text">ABBY DENEUI</strong>, COACH</p>
        </div>
        <div class="member-content">
            <div class="card">
                <h2 class="main-font member-title">WE MATCH YOU WITH THE OPPORTUNITIES <span class="red-text">THAT BEST FIT YOUR CAREER GOALS</span></h2>
                <a href="" class="watch-video main-font red-bg">
                    WATCH VIDEO
                    <i class='bx bx-play-circle' ></i>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
import MainHeader from '@/components/MainHeader.vue'

export default {
    name: 'Home',
    components: {
        MainHeader
    }
}
</script>

<style lang="less">
    .main-font {
        font-family: 'Kanit', Sans-Serif;
    }
    .jobs {
        display: flex;
        flex-direction: column;
        min-height: 88vh;
        align-items: center;
        justify-content: center;
        background-image: url(../assets/img/job-search.png);
        background-position: center center;
        background-size: cover;
    }
    .red-text {
        color: #D52028;
    }
    .title {
        .main-font();
        color: #333;
        font-weight: 700;
        font-size: 68px;
    }
    .form-container {
        width: 100%;
        display: flex;
        justify-content: center;
        form {
            display: flex;
            width: 50%;
            align-items: center;
            justify-content: space-around;
        }
    }
    .jobs-fields {
        .main-font();
        font-weight: 500;
        font-size: 18px;
        border: none;
        background-color: #ececec;
        padding: 16px 42px;
        border-radius: 48px;
        transition: all .4s ease-in-out;
        &:focus {
            border: none;
            box-shadow: 1px 1px 5px 0px rgba(0,0,0,0.45)
        }
        &:focus-visible {
            outline: none;
        }
    }
    .submit-button {
        border: none;
        padding: 16px 42px;
        border-radius: 48px;
        color: #ffffff;
        .main-font();
        font-weight: 600;
        font-size: 18px;
        transition: all .4s ease-in-out;
        &:hover {
            cursor: pointer;
            background-color: #ffffff00;
            border: 2px solid #D52028;
            color: #D52028;
        }
    }
    .go-table {
        p {
            color: #333;
            font-weight: 600;
            font-size: 40px;
        }
    }
    .go-button {
        .main-font();
        .red-text();
        text-decoration: none;
        font-weight: 500;
        border: 2px solid #D52028;
        padding: 8px 16px;
        border-radius: 48px;
        i {
            margin-left: -24px;
            opacity: 0;
            transition: all .4s ease-in-out;
        }
        &:hover i {
            margin: 0;
            opacity: 1;
        }
    }
    .bx-chevron-down {
        color: #333;
        font-size: 48px;
        margin-top: 24px;
    }
    .member-container {
        display: flex;
        width: 100%;
        min-height: 88vh;
        align-items: center;
        justify-content: center;
        .member-image, .member-content {
            width: 50%;
        }
        .member-picture {
            width: 50%;
        }
    }
    .member-name {
        font-weight: 500;
        font-size: 24px;
    }
    .card {
        padding: 48px;
        background-color: #ececec;
        border-radius: 48px; 
    }
    .member-content {
        padding: 48px;
        .member-title {
            font-weight: 600;
            font-size: 48px;
        }
    }
    .watch-video {
        text-decoration: none;
        padding: 8px 16px;
        color: #ffffff;
        font-weight: 600;
        font-size: 24px;
        border-radius: 48px;
        transition: all .4s ease-in-out;
        i {
            .red-text();
            margin-left: -24px;
            opacity: 0;
            transition: all .4s ease-in-out;
        }
        &:hover {
            background-color: #ffffff00;
            border: 2px solid #D52028;
            .red-text();
            i {
                margin: 0;
                opacity: 1;
            }
        }
    }
    
    @media (max-width: 768px) {
        .space-up {
            margin-top: 24px;
        }
        .jobs {
            background-image: url(../assets/img/job-search-mobile.png);
            padding: 0 24px;
        }
        .form-container {
            form {
                flex-direction: column;
                width: 100%;
            }
        }
        .jobs-fields {
            width: 100%;
        }
        input[type="submit"] {
            width: 100%;
        }
        .member-container {
            flex-direction: column;
        }
        .member-image, .member-content {
            width: 100%;
        }
        .member-picture {
            width: 100% !important;
        }
        .member-name {
            font-size: 18px;
        }
        .member-title {
            font-size: 24px !important;
        }
        .member-content {
            width: 100% !important;
            padding: 0 12px;
        }
    }
</style>