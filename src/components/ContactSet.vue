<template>
    <div class="contact-set">
        <a :href="contact.link" class="contact-item" v-for="contact in contacts" :key="contact.name" target="_blank">
            <img :src="require('../assets/img/icons/' + contact.img)" width="20" height="20" :alt="contact.name" loading="lazy">
            {{contact.text}}
        </a>
    </div>
</template>

<script>
export default {
    name: 'ContactSet',
    data() {
        return {
            contacts: [
                {
                    name: 'location',
                    text: 'Toronto, Canada',
                    img: 'location.png',
                    link: 'https://www.google.com/maps/place/Toronto,+ON,+Canada/@43.718371,-79.5428638,11z/data=!3m1!4b1!4m6!3m5!1s0x89d4cb90d7c63ba5:0x323555502ab4c477!8m2!3d43.653226!4d-79.3831843!16zL20vMGg3aDY?entry=ttu'
                },
                {
                    name: 'Skype',
                    text: 'Black Cat',
                    img: 'skype.png',
                    link: 'https://join.skype.com/invite/xisLaU16JalB'
                },
                {
                    name: 'email',
                    text: 'Black Cat',
                    img: 'email.png',
                    link: 'mailto:black.cat01312@gmail.com'
                },
                {
                    name: 'telegram',
                    text: 'superBizz3217',
                    img: 'telegram.png',
                    link: 'https://t.me/superBizz3217'
                },
            ]
        }
    }
}
</script>

<style>
.contact-set {
    width: 100%;
}
.contact-item {
	display: flex;
  align-items: center;
  padding: 1.6rem;
  border: 1px solid hsla(0, 0%, 100%, 0.2);
  background-color: var(--main-bg-color);
  backdrop-filter: blur(5px);
  border-radius: var(--box-border-radius);
  border: var(--box-border);
  box-shadow: var(--box-shadow);
  margin-bottom: .3rem;
  transition: all .2s ease
}
.contact-item:hover {
	background-color: var(--contact-item-hover-bg);
  border: var(--box-border);
}
.contact-item img {
	margin-right: 1.5rem;
  height: auto;
  filter: drop-shadow(var(--regular-text-shadow))
}
@media (max-width: 600px) {
  .contact-item {
    padding: 1rem;
    font-size: 0.9rem;
  }
}
@media (max-width: 350px) {
  .contact-item {
    padding: 1.5rem .8rem;
    font-size: 0.9rem;
  }
  .contact-item img {
    margin-right: .5rem;
  }
}
</style>