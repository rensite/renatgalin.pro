<template lang="pug">
header.header.content
  .header-logo
    .header-avatar
      img(src="https://avatars.githubusercontent.com/u/31538214")
    .header-info
      h1.header-info-name Renat Galin 
      p.header-info-skill Front-End Dev / Designer
  .header-nav
    .header-nav-menu
      .header-nav-link contact me
    .header-nav-contacts
      a(href="#").header-nav-social
      a(href="#").header-nav-social
      a(href="#").header-nav-social
      a(href="#").header-nav-social
RouterView
</template>

<style lang="scss">
  .header {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    padding: 1.8rem 0;

    &-logo {
      display: flex;
      align-items: flex-end;
      gap: 2rem;
    }
    
    &-avatar {
      width: 8rem;
      height: 8rem;
      overflow: hidden;
      border-radius: 50%;
      border: 1px solid #eee;
    }
  }
  
  .header-info {
    margin-bottom: 1.2rem;
    
    &-name {
      font-size: 3.3rem;
      font-weight: 700;
      text-transform: uppercase;
      line-height: 1;
      margin: 0 0 .5rem;
    }
      
    &-skill {
      font-size: 1.9rem;
      font-weight: 400;
      line-height: 1;
      margin: 0;
    }
  }
    
  .header-nav {
    display: grid;
    gap: .8rem;
    margin-bottom: 1.4rem;
    
    @include mqPhones {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100vh;
      z-index: 999;
      background: #fff;
      place-items: center;
      grid-template-rows: 1fr auto;
      padding-bottom: 24px;
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
</style>
