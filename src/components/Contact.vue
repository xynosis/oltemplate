<template lang="pug">
v-container(text-xs-center fill-height justify-center)
        v-flex(xs10)
            h1 Where is Open Lab?
            iframe(src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1096.4210352383202!2d-1.6268650601997814!3d54.97436920021209!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487e70cc04d6ac0f%3A0x144aed291839c569!2sOpen+Lab!5e0!3m2!1sen!2suk!4v1530783807050" width="600" height="450" frameborder="0" style="border:0" allowfullscreen)
            br
            br
            h1 Any other questions?
            v-btn(href='mailto:addnamehere' id='email' large) Email me
</template>