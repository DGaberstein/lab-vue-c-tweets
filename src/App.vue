<template>
  <div id="app">
    <Tweet v-for="(tweet, index) in tweets" :key="index" :tweet="tweet" />
  </div>
</template>

<script>
import Tweet from './components/Tweet.vue'

export default {
  name: 'App',
  components: {
    Tweet
  },
  data() {
    return {
      tweets: [
        {
          user: {
            name: "John Doe",
            image: "https://via.placeholder.com/50",
            handle: "@johndoe"
          },
          timestamp: "2h ago",
          message: "This is a static tweet message for now."
        },
        {
          user: {
            name: "Jane Doe",
            image: "https://via.placeholder.com/50",
            handle: "@janedoe"
          },
          timestamp: "3h ago",
          message: "Another static tweet message."
        },
        {
          user: {
            name: "Foo Bar",
            image: "https://via.placeholder.com/50",
            handle: "@foobar"
          },
          timestamp: "1h ago",
          message: "Yet another static tweet message."
        }
      ]
    }
  }
}
</script>

<style>
  body {
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Oxygen",
      "Ubuntu", "Cantarell", "Fira Sans", "Droid Sans", "Helvetica Neue",
      sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }

  .app {
    text-align: center;
  }

  .app-logo {
    height: 40vmin;
    pointer-events: none;
  }

  @media (prefers-reduced-motion: no-preference) {
    .app-logo {
      animation: App-logo-spin infinite 20s linear;
    }
  }

  .app-header {
    background-color: #282c34;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-size: calc(10px + 2vmin);
    color: white;
  }

  .app-link {
    color: #61dafb;
  }

  @keyframes App-logo-spin {
    from {
      transform: rotate(0deg);
    }
    to {
      transform: rotate(360deg);
    }
  }

  .app {
    padding: 20px;
  }

  .tweet {
    margin: 0 auto;
    min-width: 480px;
    max-width: 640px;
    min-height: 80px;
    padding: 10px;
    border: 1px solid #ccc;
    display: flex;
    font-size: 1.1rem;
    line-height: 18px;
  }

  .body {
    display: flex;
    flex-direction: column;
    width: 100%;
  }

  .top {
    display: flex;
    line-height: 1.4rem;
  }

  .more {
    margin-left: 20px;
  }

  .profile {
    width: 50px;
    height: 50px;
    border-radius: 50px;
    margin-right: 10px;
  }

  .name {
    font-weight: bold;
    margin-bottom: 0.5em;
    margin-right: 0.3em;
  }

  .handle {
    color: #536471;
    margin-left: 3px;
    margin-right: 3px;
  }

  .timestamp {
    color: #536471;
    font-size: 1.1rem;
  }

  .timestamp::before {
    content: "·";
    padding-right: 0.3em;
    font-size: 1.1rem;
    font-weight: 600;
  }

  .message {
    text-align: left;
    font-stretch: 100%;
    font-weight: 400;
    line-height: 1.6rem;
    overflow-wrap: break-word;
    white-space: pre-wrap;
  }

  .actions {
    padding: 5px 5px;
    width: 360px;
    display: flex;
    justify-content: space-between;
    color: #536471;
  }

</style>