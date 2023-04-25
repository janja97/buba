<template>
    <div class="nav-wrapper">
        <div class="logo-container mv">
            <router-link class="mx-3 header-logo" to="/">BF</router-link>
        </div>
        <nav>
            <input class="hidden" type="checkbox" id="menuToggle">
            <label class="menu-btn" for="menuToggle">
                <div class="menu"></div>
                <div class="menu"></div>
                <div class="menu"></div>
            </label>
            <div class="nav-container">
                <ul class="nav-tabs">
                    <div class="heder-tabs mv">
                        <router-link class="header-logo" to="/">BF</router-link>
                    </div>
					<li class="nav-ta"><router-link class="mx-3 link" to="/">Portfolio</router-link></li>
                    <li class="nav-ta"><router-link class="mx-3 link" to="/client">Client</router-link></li>
                    <li class="nav-ta"><router-link class="mx-3 link logo" to="/">BF</router-link></li>
                    <li class="nav-ta"><router-link class="mx-3 link" to="/about">About</router-link></li>
                    <li class="nav-ta"><router-link class="mx-3 link" to="/contact">Contact</router-link></li>
                    <div class="justify-content-center mv">
						<a href="https://instagram.com/bubaaphotography?igshid=YmMyMTA2M2Y="><img src="/image/icons/instagram-black.png" alt="instagram" class="icons"></a>
						<a href="https://www.facebook.com/profile.php?id=100090263107531"><img src="/image/icons/facebook-black.png" alt="facebook" class="icons"></a>
						<a href="https://wa.me/00447931588770"><img src="/image/icons/whatsapp-black.png" alt="whatsApp" class="icons"></a>
						<a href="mailto:photographybuba@gmail.com"> <img src="/image/icons/email-black.png" alt="mail" class="icons"></a>

                    </div>
                </ul>
            </div>
        </nav>
    </div>

</template>

<script>
export default {
    name: "AppNavbarBlack",
};
</script>

<style setup>
.header-logo {
	color: black;
}

.center {
	text-align: center;
}
.mv {
    display: none;
}
@media screen and (max-width: 800px) {
    .mv {
        display: block;
    }
}

.nav-wrapper {
    width: 100%;
	display: flex;
	position: absolute;
	top: 0px;
	flex-direction: row;
	flex-wrap: nowrap;
	align-items: center;
	justify-content: center;
	margin: auto;
	height: 80px;
	padding: 0 25px;
	z-index: 2;

}

/* .logo-container {
	display: flex;
	justify-content: center;
	align-items: center;
} */

/* .logo {
	height: 60px;
} */

.nav-tabs {
	display: flex;
	/* font-weight: 600;
	font-size: 1px; */
	list-style: none;
    border: none;
	align-items: center;

}

.nav-ta .link {
    color: black ;
	letter-spacing: 1.5px;
	font-weight: 700;
}
.nav-ta .logo {
	font-size: 25px;
}

/* .nav-tab:not(:last-child) {
	padding: 10px 25px;
	margin: 0;
	border-right: 1px solid #eee;
} */

/* .nav-tab:last-child {
	padding: 10px 0 0 25px;
} */

.nav-ta,
.menu-btn {
	cursor: pointer;
}

.hidden {
	display: none;
}

@media screen and (max-width: 800px) {
    .nav-wrapper {
        justify-content: space-between;
    }
    .nav-ta .link {
        color: black  !important;
    }
	.nav-container {
		position: fixed;
		display: none;
		z-index: 99;
		top: 0;
		right: 0;
		width: 100%;
		height: 100%;
		background: #fff;
        color: black;
	}
   
    
	.nav-tabs {
		flex-direction: column;
		align-items: center;
		margin: 30px 30px 0 30px;
        padding: 0;
        width: 100%;
        z-index: 9999999;
	}
    .heder-tabs {
        justify-content: space-between;
        width: 100%;
        margin-bottom: 150px;
    }

	/* .nav-tab:not(:last-child) {
		margin: 0;
		border-right: unset;
	}

	.nav-tab:last-child {
		padding: 15px 25px;
	} */

	.menu-btn {
		position: relative;
		display: block;
		margin: 0;
		width: 20px;
		cursor: pointer;
		z-index: 99999999999999;
		padding: 10px;
		border-radius: 10px;
	}

	.menu-btn .menu {
		display: block;
		width: 20px;
		height: 2px;
		border-radius: 2px;
		background: black;
	}

	.menu-btn .menu:nth-child(2) {
		margin-top: 4px;
		opacity: 1;
	}

	.menu-btn .menu:nth-child(3) {
		margin-top: 4px;
	}

	#menuToggle:checked + .menu-btn .menu {
		transition: transform 0.2s ease;
	}

	#menuToggle:checked + .menu-btn .menu:nth-child(1) {
		transform: translate3d(0, 6px, 0) rotate(45deg);
        background-color: black;
	}

	#menuToggle:checked + .menu-btn .menu:nth-child(2) {
		transform: rotate(-45deg) translate3d(-5.71429px, -6px, 0);
		opacity: 0;
        background-color: black;

	}

	#menuToggle:checked + .menu-btn .menu:nth-child(3) {
		transform: translate3d(0, -6px, 0) rotate(-45deg);
        background-color: black;

	}

	#menuToggle:checked ~ .nav-container {
		z-index: 1;
		display: flex;
		animation: menu-slide-left 0.3s ease;
	}
	@keyframes menu-slide-left {
		0% {
			transform: translateX(200px);
		}
		to {
			transform: translateX(0);
		}
	}
}




</style>
  