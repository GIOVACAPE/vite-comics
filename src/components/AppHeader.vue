<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      // NavBar Items
      navItems: [
        {
          text: 'characters',
          url: '#',
          active: false
        },
        {
          text: 'comics',
          url: '#',
          active: true
        },
        {
          text: 'movies',
          url: '#',
          active: false
        },
        {
          text: 'tv',
          url: '#',
          active: false
        },
        {
          text: 'games',
          url: '#',
          active: false
        },
        {
          text: 'collectibles',
          url: '#',
          active: false
        },
        {
          text: 'videos',
          url: '#',
          active: false
        },
        {
          text: 'fans',
          url: '#',
          active: false
        },
        {
          text: 'news',
          url: '#',
          active: false
        },
        {
          text: 'shop',
          url: '#',
          active: false
        },
      ]
    }
  }
}
</script>

<template>
  <header>

    <div class="container-wrapped d-flex flex-between">
      <img src="../assets/dc-logo.png" alt="DC Main Logo">

      <nav>
        <ul>
          <li v-for="item in navItems" :class="(item.active) ? 'active' : ''" class="d-flex align-center">
            <a :href="item.url">{{ item.text }}</a>
          </li>
        </ul>
      </nav>
    </div>

  </header>
</template>

<style lang="scss" scoped>
@use '../styles/_variables.scss' as *;

header {
  width: 100%;
  background-color: $white;

  div.container-wrapped {
    align-items: stretch;
  }
}

img {
  height: 120px;
  padding: 1rem 0;
}


nav ul {
  display: flex;
  height: 100%;
  padding-top: 1rem;

  li {
    list-style-type: none;
    height: 100%;
    margin: 0 1rem;
    border-bottom: 7px solid transparent;

    a {
      text-decoration: none;
      text-transform: uppercase;
      font-weight: 700;
      font-size: .8rem;
      color: black;

      &:hover {
        color: $brand-color;
      }
    }

  }

  li.active {
    border-bottom: 7px solid $brand-color;
  }

  .active a {
    // padding-bottom: 3.33rem;
    color: $brand-color;
  }
}
</style>