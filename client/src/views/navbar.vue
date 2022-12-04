<template>
    <nav class="navbar navbar-expand-lg">
        <div class="container">
            <a class="navbar-brand" href="#">LetsGoo</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav me-auto">
                    <li class="nav-item">
                        <router-link class="nav-link" to="/">Home</router-link>
                    </li>
                    <!-- <li class="nav-item">
                        <router-link class="nav-link" to="/about">About</router-link>
                    </li> -->
                </ul>

                <ul class="navbar-nav d-flex">
                    <li class="nav-item">
                        <router-link class="nav-link" to="/keranjang">Keranjang <i class="bi bi-bag"></i><span class="badge text-bg-success mr-2">0</span></router-link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>

export default {
    
}
</script>