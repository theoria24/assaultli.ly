<template>
  <div class="layout">
    <header class="header">
      <h1>
        <g-link to="/">{{ $static.metadata.siteName }}</g-link>
      </h1>
    </header>
    <slot />
    <footer>
      <hr />
      <div>
        このページのソースコードは
        <g-link to="https://github.com/theoria24/assaultli.ly">GitHub</g-link>
        上で管理されています。修正の必要がある場合は
        <g-link to="https://github.com/theoria24/assaultli.ly/issues/new"
          >Issue</g-link
        >
        や
        <g-link to="https://github.com/theoria24/assaultli.ly/compare"
          >Pull request</g-link
        >
        をお願いします。
      </div>
      <hr />
      <div>
        &copy; 2020<!-- -{{ new Date().getFullYear() }}-->
        assaultli.ly
      </div>
    </footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.nav__link {
  margin-left: 20px;
}
</style>
