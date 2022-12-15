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
      a(href="#").menu-link Blog
      a(href="#").menu-link GitHub
      a(href="#").menu-link Projects
    .header-nav-contacts
      a(href="#").contact-link
      a(href="#").contact-link
      a(href="#").contact-link
      a(href="#").contact-link
RouterView
</template>

<style lang="stylus" scoped>
  .header
    display: flex
    justify-content: space-between
    align-items: flex-end
    padding: 12px 0;

    &-logo
      display: flex
      align-items: flex-end
      gap: 20px
    
    &-avatar
      width: 80px
      height: 80px
      overflow: hidden
      border-radius: 50%
      border: 1px solid #eee;
  
  .header-info
      margin-bottom: 12px
      
      &-name
        font-size: 32px
        font-weight: 700
        text-transform: uppercase
        line-height: 1
        margin: 0 0 5px
        
      &-skill
        font-size: 19px
        font-weight: 400
        line-height: 1
        margin: 0
        
    img
      width: 100%
      height: 100%
    
  .header-nav
    display: grid
    gap: 8px
    margin-bottom: 14px
      
    &-menu,
    &-contacts
      display: grid
      grid-auto-flow: column
      justify-content: right
      gap: 12px
    
.contact-link
  width: 24px
  height: 24px
  border-radius: 50%
  background: #ccc
  display: block

a.menu-link
  &, &:visited
    text-decoration: none
    color: #000
    font-weight: 400
    font-size: 17px
</style>
