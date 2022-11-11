<template>
    <aside :style="{ display: isActive }">
        <div class="top">
            <div class="logo">
                <img src="../assets/logo.png" alt="" />
                <h2>Kha <span class="danger">Wal</span></h2>
            </div>
            <div class="close" id="close-btn" @click="active">
                <i class="uil uil-multiply"></i>
            </div>
        </div>
        <div class="side-bar">
            <a href="#" class="active" @click="active">
                <i class="uil uil-th"></i>
                <h3>Dashboard</h3>
            </a>
            <a href="#">
                <i class="uil uil-user"></i>
                <h3>Customers</h3>
            </a>
            <a href="#">
                <i class="uil uil-file-copy-alt"></i>
                <h3>Orders</h3>
            </a>
            <a href="#">
                <i class="uil uil-analysis"></i>
                <h3>Analytics</h3>
            </a>
            <a href="#">
                <i class="uil uil-envelope-alt"></i>
                <h3>Messages</h3>
                <span class="message-count">12</span>
            </a>
            <a href="#">
                <i class="uil uil-file-check-alt"></i>
                <h3>Products</h3>
            </a>
            <a href="#">
                <i class="uil uil-exclamation-octagon"></i>
                <h3>Reports</h3>
            </a>
            <a href="#">
                <i class="uil uil-setting"></i>
                <h3>Settings</h3>
            </a>
            <a href="#">
                <i class="uil uil-plus"></i>
                <h3>Add Products</h3>
            </a>
            <a href="#">
                <i class="uil uil-sign-out-alt"></i>
                <h3>Logout</h3>
            </a>
        </div>
    </aside>
</template>
<script>
export default {
    data() {
        return {
            isActive: null,
        }
    },
    methods: {
        active() {
            if (this.isActive == 'block') {
                this.isActive = 'none'
            } else {
                this.isActive = 'block'
            }
        }
    }
}</script>