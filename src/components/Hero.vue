<template>
 <section class="hero l-container-pd">
     <img src="/assets/login.png">
     <div class="l-section">
         <div class="hero__content">
             <h1 v-for="subTitle in title" :key="subTitle" class="Title-2">
                 {{subTitle}}
            </h1>
             <p v-if="home == true" class="Title-4">Con nuestros programas de especialización</p>
         </div>
     </div>
 </section>
</template>

<script>
export default {
    name: 'Hero',
    props:{
        home: Boolean,
        title: Array
    }
}
</script>

<style lang="scss">
.hero{
    margin-bottom: 0;
    width: 100%;
    position: relative;
    height: calc( ( 100vw * 500 ) / 1366);
    min-height: 300px;
    overflow: hidden;
    z-index: 2;
    img{
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
    }
    div{
        background: none;
    }
    .l-section{
        position: relative;
        height: 100%;
        display: flex;
        justify-content: flex-start;
        align-items: flex-end;
    }
    &__content{
        .Title-2{
            color: var(--Light);
        }
        .Title-4{
            color: var(--Light);
            max-width: 90%;
            margin-top: 20px;
        }
    }
}

@media screen and (min-width: 520px) {
    .hero{
        &__content{
            .Title-2{
                font-size: 36px;
            }
            .Title-4{
                font-size: var(--large);
            }
        }
    }
}

@media screen and (min-width: 990px) {
    .hero{
        &__content{
            .Title-2{
                font-size: 42px;
            }
            .Title-4{
                margin-bottom: 40px;
            }
        }
    }
}

@media screen and (min-width: 1200px) {
    .hero{
        &__content{
            .Title-2{
                font-size: var(--xx-large);
            }
            .Title-4{
                margin-bottom: 60px;
            }
        }
    }
}

@media screen and (max-width: 819px) {
    .hero{
        img{
            width: 819px;
            left: calc( (819px - 100vw) / -2 );
        }
    }
}
</style>