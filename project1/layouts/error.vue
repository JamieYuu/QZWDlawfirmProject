<template>
    <div id="wholePage">
        <script src="https://use.fontawesome.com/c17a47c7ea.js"></script>
        <p id="theText"><i class="fa fa-exclamation-circle" aria-hidden="true"></i> 页面被吃掉了!</p>
        <p id="theButton"><router-link to="/"><b-btn variant="outline-primary">返回首页</b-btn></router-link></p>
    </div>
</template>

<script>

</script>

<style>
body {
    background-color: rgb(245, 245, 245)
}

#theButton{
    position: relative;
    top: 200px;
    text-align: center;
}

#theText {
    position: relative;
    top: 200px;
    text-align: center;
    font-size: 30px;
}
</style>

