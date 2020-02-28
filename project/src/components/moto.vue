<template>
    <div class="main">

        <img src="../assets/rouge.png" alt="image mac" width="50%" v-if="colorSelected === 'rouge'">
        <img src="../assets/jaune.png" alt="image mac" width="50%" v-if="colorSelected === 'jaune'">


        <div class="toggle-radio">
            <input type="radio" name="rdo" id="yes" checked value="rouge" v-model="colorSelected">
            <input type="radio" name="rdo" id="no" value="jaune" v-model="colorSelected">
            <div class="switch">
                <label for="yes">Rouge</label>
                <label for="no">Jaune</label>
                <span></span>
            </div>
        </div>





    </div>
</template>

<script>
    export default {
        name: 'moto',

        data() {
            return{
                colorSelected: 'rouge'
            }
        }


    }

</script>

<style>



  .main{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    li{
        list-style: none;
    }
    body {
        font-family: sans-serif;
        font-weight: 800;
        background: #eee;
    }
    .switch {
        position: absolute;
        top: 50%;
        left: 50%;
        width: 300px;
        height: 50px;
        text-align: center;
        margin: -10px 0 0 -145px;
        background: red;
        transition: all 0.2s ease;
        border-radius: 25px;
    }

    input[type=radio] {
        display: none;
    }
    .switch label {
        cursor: pointer;
        color: rgba(0,0,0,0.2);
        width: 180px;
        line-height: 50px;
        transition: all 0.2s ease;
    }
    label[for=yes] {
        position: absolute;
        left: 0px;
        height: 20px;
    }
    label[for=no] {
        position: absolute;
        right: 0px;
    }
    #no:checked ~ .switch {
        background: yellow;
    }
    #no:checked ~ .switch span {
        background: #fff;
        margin-left: -8px;
    }
    #no:checked ~ .switch span:after {
        background: #fff;
        height: 20px;
        margin-top: -8px;
        margin-left: 8px;
    }
    #yes:checked ~ .switch label[for=yes] {
        color: #fff;
    }
    #no:checked ~ .switch label[for=no] {
        color: #fff;
    }

</style>