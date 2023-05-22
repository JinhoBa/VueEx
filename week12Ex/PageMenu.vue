<template>
    <aside class="sidebar">
        <nav>
            <a class="closebtn" onclick="closeMenu()">×</a>
            <ul>
                <li><router-link to="/about">about</router-link></li>
                <li><router-link to="/test">test</router-link></li>
                <li><router-link to="/set">setting</router-link></li>
            </ul>
        </nav>
    </aside>
</template>
<script>
export default {

}
</script>
<style>
    .sidebar {
            height: 100%;
            width: 20%;
            position: fixed;
            z-index: 1;
            top: 0;
            left: 0;
            background-color: #111;
            transition: 0.3s;/*펼침속도*/
            padding-top: 60px;
            }
    .sidebar ul {
            padding: 8px 8px 8px 32px;
            text-decoration: none;
            font-size: 20px;
            color: #818181;
            display: block;
            transition: 0.3s;
            }
</style>
