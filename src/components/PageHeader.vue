<script>
export default {
    name: "PageHeader",
    data() {
        return {
            navbarItems: [
                {
                    title: "Home",
                    arrow: true
                },
                {
                    title: "Courses",
                    arrow: true
                },
                {
                    title: "About Us",
                    arrow: false
                },
                {
                    title: "News",
                    arrow: true
                },
                {
                    title: "Pages",
                    arrow: true
                },
                {
                    title: "Contact",
                    arrow: false
                },
                {
                    title: "Purchase",
                    arrow: false
                }
            ]
        }
    }
}
</script>

<template>
    <header>
        <div id="menu">
            <div>
                <img src="../assets/img/theme_eduprime_logo.png" alt="Logo Eduprime">
            </div>
            <div>
                <nav>
                    <ul>
                        <li v-for="navbarItem in navbarItems">
                            <strong>
                                {{ navbarItem.title }}
                                <font-awesome-icon class="marLef0_5rem" icon="fa-solid fa-caret-down"
                                    v-if="navbarItem.arrow == true" />
                            </strong>
                        </li>
                    </ul>
                </nav>
            </div>
            <div>
                <button>
                    <strong>VIEW COURSES</strong>
                </button>
            </div>
        </div>
    </header>
</template>

<style scoped>
header {
    height: 1000px;
    background-color: red;
    padding: 3rem 3rem 0;
}

#menu {
    display: flex;
}

#menu>div:first-child,
#menu>div:last-child {
    width: 25%;
}

#menu>div:nth-child(2) {
    width: 50%;
    display: flex;
    align-items: center;
}

#menu>div:first-child>img {
    width: 100%;
}

#menu>div:first-child {
    padding-right: 1.5rem;
    display: flex;
    align-items: center;
}

#menu>div:nth-child(2)>nav>ul {
    list-style-type: none;
    display: flex;
    justify-content: space-between;
}

#menu>div:nth-child(2)>nav>ul>li:first-child {
    color: rgba(232, 210, 89, 255);
}

#menu>div:nth-child(2)>nav {
    width: 100%;
}

#menu>div:nth-child(2)>nav>ul>li {
    color: white;
}

#menu>div:last-child {
    display: flex;
    align-items: center;
    padding-left: 1.5rem;
    justify-content: flex-end;
}

#menu>div:last-child>button {
    padding: 1.5rem 3rem;
    border: none;
    border-radius: 2rem;
    color: white;
    background-color: rgba(232, 210, 89, 255);
}
</style>