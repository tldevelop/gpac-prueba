<template>
    <header class="header-container">
        <div class="logo-container">
            <router-link to="/">
                <img src="../assets/img/icon-logo.png" alt="Site Logo" class="site-logo">
            </router-link>        
        </div>
        <div class="nav-container">
            <div class="menu">
                <i class='bx bx-search search-icon'></i>
                <i class='bx bx-menu menu-icon'></i>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    
}
</script>

<style lang="less">
    .half-width {
        width: 50%;
    }
    .header-container {
        display: flex;
        align-items: center;
        padding: 8px 28px;
        position: sticky;
        top: 0;
        background-color: #ffffff;
        .logo-container {
            text-align: left;
            .site-logo {
                width: 64px;
            }
        }
        .logo-container,
        .nav-container {
            .half-width();
            .menu-icon {
                font-size: 48px;
                &:hover {
                    cursor: pointer;
                }
            }
        }
        .menu {
            display: flex;
            align-items: center;
            justify-content: flex-end;
        }
        .search-icon {
            font-size: 38px;
            position: absolute;
            right: 98px;
            &:hover {
                cursor: pointer;
            }
        }
    }
</style>