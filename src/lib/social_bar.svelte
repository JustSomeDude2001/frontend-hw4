<script lang="ts">
    import { onMount } from 'svelte';
  
    let ghLink = "http://github.com/justsomedude2001";
    let tgLink = "https://t.me/JustSomeDude22";
    let email = "mailto:kim.yaroslavik@gmail.com";
  
    onMount(() => {
      const ghLinkElement = document.querySelector("gh-link");
      ghLinkElement.setAttribute("href", ghLink);
      
      const tgLinkElement = document.querySelector("tg-link");
      tgLinkElement.setAttribute("href", tgLink);
      
      const emailElement = document.querySelector("email");
      emailElement.setAttribute("href", email);
    });
  </script>
  
  <div class="social-bar">
    <p>
      Contact Me:
    </p>
  
    <a id="gh-link">
      <img src="public/github.png" width="20" height="20" alt="github"/>
    </a>
  
    <a id="tg-link">
      <img src="public/telegram.png" width="20" height="20" alt="telegram"/>
    </a>
  
    <a id="email">
      <img src="public/gmail.webp" width="20" height="20" alt="mail"/>
    </a>
  </div>