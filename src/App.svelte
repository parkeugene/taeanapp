<script>
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte'
  import { Footer, FooterCopyright, FooterLinkGroup, FooterLink } from 'flowbite-svelte'
  import { Carousel} from 'flowbite-svelte';
  import { scale } from 'svelte/transition';
  import { quintOut } from 'svelte/easing';
  import { Skeleton } from 'flowbite-svelte';
  export const images = [
    {
      alt: '청년들이 만들어가는 새로운 태안',
      src: 'https://taeanyouth.netlify.app/images/main-slide/main-slide-img-01.png',      
    },
    {
      alt: '...',
      src: 'https://taeanyouth.netlify.app/images/main-slide/main-slide-img-02.png',      
    },
    {
      alt: '..',
      src: 'https://taeanyouth.netlify.app/images/main-slide/main-slide-img-03.png',
    },
    {
      alt: '...',
      src: 'https://taeanyouth.netlify.app/images/main-slide/main-slide-img-04.png',

    },
  ];

</script>


<Navbar let:hidden let:toggle>
  <NavBrand href="/">
    <img
      src="https://taeanyouth.netlify.app/images/logo/logo.svg"
      class="mr-3 h-6 sm:h-9"
      alt="Logo"
    />    
  </NavBrand>
  <NavHamburger on:click={toggle} />
  <NavUl {hidden} >
    <NavLi href="#" class="text-2xl md:hover:text-blue-500">태안Talk</NavLi>
    <NavLi href="#" class="text-2xl md:hover:text-blue-500">태안人터뷰</NavLi>
    <NavLi href="#" class="text-2xl md:hover:text-blue-500">태안 청년정책</NavLi>
    <NavLi href="#" class="text-2xl md:hover:text-blue-500">새소식</NavLi>
  </NavUl>
</Navbar>

  <Carousel {images} duration="3000" let:Controls let:Indicators>
    <Controls />
    <Indicators />
  </Carousel>

<div class="mt-5 px-5">
  <span class="text-2xl">주요서비스</span>  
  <Skeleton size="xxl" class="mt-8 mb-2.5" />
</div>

<Footer class="mt-10">
  <FooterCopyright href="/" by="TaeanYouth™" year={2024} />
</Footer>



