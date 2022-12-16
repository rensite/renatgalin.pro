<template lang="pug">
header.header.content
  .header-logo
    .header-avatar
      img(src="https://avatars.githubusercontent.com/u/31538214")
    .header-info
      h1.header-info-name Renat Galin 
      p.header-info-skill Front-End Dev / Designer
  .header-nav
    .header-nav-close menu
    .header-nav__layout
      .header-nav-menu
        .header-nav-link contact me
      .header-nav-contacts
        a(href="#").header-nav-social
        a(href="#").header-nav-social
        a(href="#").header-nav-social
        a(href="#").header-nav-social
RouterView
footer.footer.content
  .footer-copyright &copy; Renat Galin | Front-End Dev/Designer, 2022
</template>

<style lang="scss">
  .header {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    padding: 1.8rem 0;

    @include mqPhones {
      padding: 1.2rem 0;
      align-items: center;
    }

    &-logo {
      display: flex;
      align-items: flex-end;
      gap: 2rem;

      @include mqPhones {
        align-items: center;
        gap: 1rem;
      }
    }
    
    &-avatar {
      width: 8rem;
      height: 8rem;
      overflow: hidden;
      border-radius: 50%;
      border: 1px solid #eee;

      @include mqPhones {
        width: 5.2rem;
        height: 5.2rem;
      }
    }
  }
  
  .header-info {
    margin-bottom: 1.2rem;

    @include mqPhones {
      margin-bottom: .2rem;
    }
    
    &-name {
      font-size: 3.3rem;
      font-weight: 700;
      text-transform: uppercase;
      line-height: 1;
      margin-bottom: .5rem;

      @include mqPhones {
        font-size: 2.2rem;
        margin-bottom: 0;
      }
    }
      
    &-skill {
      font-size: 1.9rem;
      font-weight: 400;
      line-height: 1;
      margin: 0;

      @include mqPhones {
        font-size: 1.25rem;
      }
    }
  }
    
  .header-nav {

    @include mqPhones {
      margin-bottom: 0;
    }
    
    &__layout {
      display: grid;
      gap: .8rem;
      margin-bottom: 1.4rem;

      @include mqPhones {
        display: grid;
        display: none;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100vh;
        z-index: 999;
        background: #fff;
        place-items: center;
        grid-template-rows: 1fr auto;
        padding-bottom: 2.4rem;
      }
    }

    &-close {
      display: none;

      @include mqPhones {
        width: auto;
        height: 3.3rem;
        display: flex;
        font-size: 1.3rem;
        line-height: 1;
        align-items: flex-end;
        color: var(--color-text);
        
        &::before,
        &::after {
          content: '';
          width: 2.9rem;
          height: .4rem;
          background-color: var(--color-text);
          position: absolute;
          right: 0;
        }

        &::before {
          top: .3rem;
        }

        &::after {
          top: 1.2rem;
        }
      }
    }
      
    &-menu,
    &-contacts {
      display: grid;
      grid-auto-flow: column;
      justify-content: right;
      gap: 1.2rem;
    }

    &-menu {
      @include mqPhones {
        grid-auto-flow: row;
        height: max-content;
        place-content: center;
        text-align: center;
      }
    }

    &-contacts {
      @include mqPhones {
        height: max-content;
        place-content: center;
      }
    }

    &-link {
      &, &:visited {
        text-decoration: none;
        color: #000;
        font-weight: 400;
        font-size: 1.7rem;
      }
    }

    &-social {
      &, &:visited {
        width: 2.4rem;
        height: 2.4rem;
        border-radius: 50%;
        background: #ccc;
        display: block;
      }
    }
  }

  .footer {
    padding-top: 1rem;
    padding-bottom: 1rem;

    &-copyright {
      font-size: 14px;
      opacity: .5;
    }
  }
</style>
