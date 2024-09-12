<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <header class="header container">
    <nav class="header-nav">
      <RouterLink class="header-logo" to="/">
        <img src="/logo.svg" width="178" height="55" alt="Логотип" />
      </RouterLink>
      <ul class="header-nav-list">
        <li><RouterLink class="header-nav-link" to="/about">Для клієнтів</RouterLink></li>
        <li><RouterLink class="header-nav-link" to="/about">Про нас</RouterLink></li>
        <li><RouterLink class="header-nav-link" to="/about">Бренди</RouterLink></li>
        <li><RouterLink class="header-nav-link" to="/about">Особистий кабінет</RouterLink></li>
        <li><RouterLink class="header-nav-link" to="/about">Контакти</RouterLink></li>
      </ul>
      <ul class="header-nav-social-list">
        <li>
          <RouterLink to="/">
            <img src="/facebook.svg" width="40" height="41" alt="Facebook" aria-label="Facebook" />
          </RouterLink>
        </li>
        <li>
          <RouterLink to="/">
            <img src="/telegram.svg" width="40" height="41" alt="Telegram" aria-label="Telegram" />
          </RouterLink>
        </li>
        <li>
          <RouterLink to="/">
            <img src="/whatsapp.svg" width="40" height="41" alt="Whatsapp" aria-label="Whatsapp" />
          </RouterLink>
        </li>
      </ul>
    </nav>
    <div class="user-area">
      <button class="btn accent-btn">Зареєструватися</button>
      <button class="btn base-btn">Увійти</button>
    </div>
  </header>
</template>

<style lang="scss">
.header {
  position: fixed;
  display: flex;
  width: 100%;
  align-items: center;
  gap: 2.5rem;
  padding-block: 1.5rem;
  box-shadow: var(--sh1);
  background-color: var(--background-primary);
  z-index: var(--header-z);

  &-logo {
    display: flex;
    align-self: center;
    flex-shrink: 0;
  }

  &-nav {
    display: flex;
    justify-content: space-between;
    flex-grow: 1;

    &-list,
    &-list li,
    &-social-list {
      display: flex;
      align-items: center;
    }

    &-social-list {
      gap: 1rem;
    }

    &-list {
      flex-wrap: wrap;
    }

    .header-nav-link {
      padding: 0.75rem 1.5rem;
      color: var(--content-primary);
      text-transform: uppercase;
      transition: opacity var(--base-transition);
      @media (hover: hover) {
        &:hover {
          opacity: 0.6;
        }
      }
    }

    &-social-list a {
      display: flex;
      width: 2.5rem;
      height: 2.5rem;
    }
  }

  .user-area {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
  }
}

@media (max-width: 1800px) {
  .header-nav-list {
    display: none;
  }
}

@media (max-width: 1400px) {
  .header-nav-social-list {
    display: none;
  }
}
</style>
