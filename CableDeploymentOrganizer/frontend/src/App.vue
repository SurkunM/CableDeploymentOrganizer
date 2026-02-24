<template>
    <div class="d-flex flex-column min-vh-100 bg-dark text-white">
        <header class="py-4">
            <div class="container text-center">
                <h1 class="h4 mb-4 text-white">Очередь монтажных работ</h1>
                <ul class="nav nav-pills nav-fill justify-content-center">
                    <li class="nav-item me-2">
                        <router-link to="/LAN"
                                     class="nav-link text-white border border-primary"
                                     :class="{ active: $route.path === '/LAN' }">
                            Локальная сеть
                        </router-link>
                    </li>

                    <li class="nav-item me-2">
                        <router-link to="/Video"
                                     class="nav-link text-white border border-primary"
                                     :class="{ active: $route.path === '/Video' }">
                            Видеонаблюдения
                        </router-link>
                    </li>

                    <li class="nav-item">
                        <router-link to="/Create"
                                     class="nav-link text-white border border-primary"
                                     :class="{ active: $route.path === '/Create' }">
                            Создать заявку
                        </router-link>
                    </li>
                </ul>
            </div>
        </header>

        <main class="flex-grow-1 overflow-hidden">
            <div class="container-fluid p-0 h-100 bg-light text-dark">
                <div class="p-3 h-100">
                    <router-view />
                </div>
            </div>
        </main>
    </div>
</template>

<script >
</script>