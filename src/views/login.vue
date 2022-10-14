<template>
    <div class="login">
        <el-card class="box-card">
            <el-form ref="loginForm" :model="loginForm" :rules="rules">
                <el-form-item prop="username">
                    <el-input placeholder="请输入账号" v-model="loginForm.username" clearable></el-input>
                </el-form-item>
                <el-form-item prop="password">
                    <el-input placeholder="请输入密码" v-model="loginForm.password" show-password></el-input>
                </el-form-item>
                <el-form-item>
                    <el-button type="primary">登陆</el-button>
                </el-form-item>
            </el-form>
        </el-card>
    </div>
</template>

<script>
export default {
    data() {
        return {
            loginForm: {
                username: '',
                password: ''
            },
            rules: {
                username: [
                    {require: true, message: '请输入账号', trigger: 'blur'}
                ],
                password: [
                    {require: true, message: '请输入密码', trigger: 'blur'}
                ]
            }
        }
    },
    mounted() {

    },
    methods: {

    }
}
</script>

<style lang="scss" socped>
.login {
    position: absolute;
    width: 100%;
    height: 100%;
    background-color: rgb(203, 197, 197);
}
.box-card {
    width: 400px;
    // margin: 0 auto;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    .el-input {
        margin-bottom: 10px;
    }
    .el-button {
        width: 100%;
    }
}
</style>