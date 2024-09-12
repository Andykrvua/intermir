<template>
  <footer class="footer container">
    <div class="footer-wrapper">
      <RouterLink to="/">
        <img src="/logo.svg" width="178" height="55" alt="Логотип" />
      </RouterLink>
      <nav class="footer-nav">
        <ul class="footer-nav-list">
          <li><RouterLink class="footer-nav-link" to="/about">Для клієнтів</RouterLink></li>
          <li><RouterLink class="footer-nav-link" to="/about">Про нас</RouterLink></li>
          <li><RouterLink class="footer-nav-link" to="/about">Бренди</RouterLink></li>
          <li><RouterLink class="footer-nav-link" to="/about">Особистий кабінет</RouterLink></li>
          <li><RouterLink class="footer-nav-link" to="/about">Контакти</RouterLink></li>
        </ul>
      </nav>
      <div class="subscribe">
        <p class="subtitle-bold">Підпишіться на розсилку</p>
        <form class="subscribe-form">
          <input class="base-input" type="email" name="email" id="email" placeholder="Email" />
          <button class="btn accent-btn">Підписатися</button>
        </form>
        <div class="subscribe-soc">
          <RouterLink to="/">
            <img src="/footer-soc/Instagram.svg" width="24" height="24" alt="Instagram" />
          </RouterLink>
          <RouterLink to="/">
            <img src="/footer-soc/facebook.svg" width="24" height="24" alt="Facebook" />
          </RouterLink>
          <RouterLink to="/">
            <img src="/footer-soc/linkedin.svg" width="24" height="24" alt="Linkedin" />
          </RouterLink>
          <RouterLink to="/">
            <img src="/footer-soc/telegram.svg" width="24" height="24" alt="Telegram" />
          </RouterLink>
        </div>
      </div>
    </div>
    <p class="copyright">© 2024 All right reserved</p>
  </footer>
</template>

<style scoped lang="scss">
.footer {
  &-wrapper {
    display: grid;
    grid-template-columns: max-content 1fr max-content;
    align-items: start;
  }

  &-nav {
    margin-inline-start: 5rem;

    &-list {
      display: flex;
      align-items: flex-start;
      flex-direction: column;

      li {
        display: flex;
      }
    }

    &-link {
      padding: 0.75rem 1.5rem;
      color: var(--content-primary);
      transition: opacity var(--base-transition);
      @media (hover: hover) {
        &:hover {
          opacity: 0.6;
        }
      }
    }
  }

  .subscribe {
    .subtitle-bold {
      margin-block-end: 1rem;
    }

    &-form {
      display: flex;
      flex-direction: column;

      .accent-btn {
        margin-block-start: 0.5rem;
      }
    }

    &-soc {
      display: flex;
      gap: 1rem;
      margin-block-start: 2.5rem;
    }
  }

  .copyright {
    margin-block: 8.25rem 1.5rem;
    text-align: center;
    color: var(--content-secondary);
  }
}
</style>
