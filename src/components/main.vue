<template>
    <main>
        <h1>Dashboard</h1>
        <div class="date">
            <input type="date" name="" id="" />
        </div>
        <div class="insights ">
            <div class="sales ">
                <i class="uil uil-analytics "></i>
                <div class="middle">
                    <div class="left">
                        <h3>Total Sales</h3>
                        <h1>$19,999</h1>
                    </div>
                    <div class="progress">
                        <svg>
                            <circle cx="38" cy="38" r="36"></circle>
                        </svg>
                        <div class="number">
                            <p>79%</p>
                        </div>
                    </div>
                </div>
                <small class="text-muted">Last 24 Hours</small>
            </div>
            <!-- end sales -->
            <div class="sales-1 ">
                <i class="uil uil-analytics "></i>
                <div class="middle">
                    <div class="left">
                        <h3>Total Sales</h3>
                        <h1>$19,999</h1>
                    </div>
                    <div class="progress">
                        <svg>
                            <circle cx="38" cy="38" r="36"></circle>
                        </svg>
                        <div class="number">
                            <p>79%</p>
                        </div>
                    </div>
                </div>
                <small class="text-muted">Last 24 Hours</small>
            </div>
            <!-- end sales -->
            <div class="sales-2">
                <i class="uil uil-analytics"></i>
                <div class="middle">
                    <div class="left">
                        <h3>Total Sales</h3>
                        <h1>$19,999</h1>
                    </div>
                    <div class="progress">
                        <svg>
                            <circle cx="38" cy="38" r="36"></circle>
                        </svg>
                        <div class="number">
                            <p>79%</p>
                        </div>
                    </div>
                </div>
                <small class="text-muted">Last 24 Hours</small>
            </div>
            <!-- end sales -->
        </div>
        <div class="recent-orders">
            <orders></orders>
        </div>
        <!-- end orders -->
    </main>
</template>
<script>
import orders from '../components/orders.vue'
export default {
    components: {
        orders: orders,
    },
    data() {
        return {

        }
    },
}
</script>