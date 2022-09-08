<script lang="ts">
  import Anchor from "$lib/components/Anchor.svelte";
  import IconButton from "$lib/components/IconButton.svelte";
  import Footer from "$lib/components/Footer.svelte";
  let color = "text-blue-300";
  let hover = "sm:hover:text-primary-500";
  let colorClass = `${color} ${hover}`;
  let spacingClass = "mx-5";
  let sizeClass = "h-14 w-11";

  type Icon = {
    link: string;
    iconClass: string;
    name: string;
  };
  const icons: Record<string, Icon> = {
    github: {
      link: "https://github.com/Angus-1",
      iconClass: "fa-2x fab fa-github",
      name: "GitHub",
    },
    linkedin: {
      link: "https://www.linkedin.com/in/asantoyo/",
      iconClass: "fa-2x fab fa-linkedin",
      name: "LinkedIn",
    },
    email: {
      link: "mailto:santoyox714@gmail.com",
      iconClass: "fa-2x far fa-envelope",
      name: "Email",
    },
  };
</script>
<Footer id="Footer" >

  <footer id="theme" class='bottom-0 left-0 flex flex-col w-full gap-8 px-8 py-16 md:gap-12'>
    
    <div class='w-full h-px m-auto bg-gradient-to-r from-transparent via-blue-400 to-transparent'></div>
    <div class='flex flex-col items-center gap-8 md:justify-between md:flex-row'>
      <div class='flex flex-col gap-2'>
        <footer>
            <div class="footer-content">
                <h3>Angel Santoyo</h3>
                <p>Feel free to check out my other projects or contact me below</p>
            </div>
    <div class='w-full h-px m-auto bg-gradient-to-r from-transparent via-gray-700 to-transparent'></div>
    <div class='flex flex-col items-center gap-6 md:flex-row md:justify-between'>
      <div class=copyright>
        &#169; 2022
      </div>
      <div class='flex gap-4 p-2 rounded-md social-wrapper'>

        <!-- if want images remove icon buttons and use below  

        <a href="mailto:santoyox714@gmail.com">         <img src = 'gmail.png'   width="65px"  alt=git/> </a>            
      <a href="https://github.com/Angus-1">            <img src = 'github.png'  width="65px" alt=gmail/> </a>          
      <a href="https://www.linkedin.com/in/asantoyo/"> <img src = 'linkedin.png'width="60px" alt=linkedin/> </a>
      
        -->
        
        <IconButton link={icons.github.link} name={icons.github.name}>
          <svg
            aria-hidden="true"
            focusable="false"
            data-prefix="fab"
            data-icon="github"
            class="svg-inline--fa fa-github fa-w-16 {colorClass} {spacingClass} {sizeClass}"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 496 512"
            ><path
              fill="currentColor"
              d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"
            /></svg
          >
        </IconButton>
    
        <!-- linkedin -->
        <IconButton link={icons.linkedin.link} name={icons.linkedin.name}>
          <svg
            aria-hidden="true"
            focusable="false"
            data-prefix="fab"
            data-icon="linkedin"
            class="svg-inline--fa fa-linkedin fa-w-14 {colorClass} {spacingClass} {sizeClass}"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 448 512"
            ><path
              fill="currentColor"
              d="M416 32H31.9C14.3 32 0 46.5 0 64.3v383.4C0 465.5 14.3 480 31.9 480H416c17.6 0 32-14.5 32-32.3V64.3c0-17.8-14.4-32.3-32-32.3zM135.4 416H69V202.2h66.5V416zm-33.2-243c-21.3 0-38.5-17.3-38.5-38.5S80.9 96 102.2 96c21.2 0 38.5 17.3 38.5 38.5 0 21.3-17.2 38.5-38.5 38.5zm282.1 243h-66.4V312c0-24.8-.5-56.7-34.5-56.7-34.6 0-39.9 27-39.9 54.9V416h-66.4V202.2h63.7v29.2h.9c8.9-16.8 30.6-34.5 62.9-34.5 67.2 0 79.7 44.3 79.7 101.9V416z"
            /></svg
          >
        </IconButton>
    
        <IconButton link={icons.email.link} name={icons.email.name}>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="{colorClass} {spacingClass} {sizeClass}"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
            />
          </svg>
        </IconButton>
      </div>
    </div>
  </footer>
    
   
  </Footer>
  <style>
    @import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,400;0,500;0,700;0,900;1,300&display=swap");
    :root {
    --gray-50: #f9fafb;
    --gray-100: #f3f4f6;
    --gray-300: #d1d5db;
    --gray-400: #93a3af;
    --gray-500: #6b7280;
    --gray-600: #4b5563;
    --gray-700: #374151;
    --gray-800: #1f2937;
    --gray-900: #111827;
    }
    .footer-content h3{
      font-size: 2.1rem;
      font-weight: 500;
      text-transform: capitalize;
      line-height: 3rem;
    }
    .footer-content p{
      max-width: 500px;
      margin: 10px auto;
      color: rgb(131, 176, 204);
      
    } 
    #theme {
    --primary: #1f2937;
    --comp-primary: #f3f4f6;
    --white: white;
    --gray-200: #374151;
    --black: black;
    }
    footer {
    background-color: var(--primary);
    color: var(--white);
    box-shadow: 1px -5px var(--blur) rgba(0, 0, 0, 0.3);
    }
    * {
    transition: all 0.3s ease;
    }
    
    </style>