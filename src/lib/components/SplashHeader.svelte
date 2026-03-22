<script>
    let {
        kicker = '',
        headline = '',
        deck = '',
        byline = '',
        pubDate = ''
        } = $props();
</script>
  
<div class="header-box">
<div class="container">
<div class="story-header">
    <h1>{headline}</h1>
<img class="rule" src="/curly-rule-dark.png" alt="Rule" />
</div>
    <p class="deck">{deck}</p>
        <div class="byline-container">
            <p class="byline">{byline}</p>
            <p class="pubdate">{pubDate}</p>
        </div>
    <span class="kicker">{kicker}</span>
</div>
</div>



<style lang="scss">
  @use '$lib/styles' as *;

  :global(.story-theme) {
    --color-accent: #3f7745;
    --color-border: #1e4524;
    --color-header-box: #c4cdc4;

    .header-box {
      top: 0;
      left: 0;
      right: 0;
      z-index: 100;
      background: linear-gradient(
      180deg,
      var(--color-header-box) 0%,
      transparent 40%,
      transparent 100%
    );
      margin: 0 auto;
    }

    .story-header {
      text-align: center;
      padding: var(--spacing-xl) var(--spacing-md);
    }

    .byline-container {
    display: flex;
    justify-content: space-between;
    /* Add additional styling here */
    }  

    .kicker {
      text-align: left;
      display: block;
      font-family: var(--font-sans);
      font-size: var(--font-size-xs);
      text-transform: uppercase;
      letter-spacing: 0.15em;
      color: var(--color-accent);
      margin-bottom: var(--spacing-xs);
    }

    .story-header h1 {
      font-family: var(--font-story-header);
      font-size: var(--font-size-dramatic);
      font-weight: var(--font-weight-normal);
      line-height: var(--leading-tight);
      color: var(--color-dark);
      margin-bottom: var(--spacing-xxl);
    }

    .rule {
      display: block;
      height: auto;
      width: auto;
      max-width: var(--max-width-xxs);
      margin: 0 auto var(--spacing-sm);
      margin-bottom: var(--spacing-xl);
    }

    .rule-2 {
      border: none;
      border-top: var(--border-width-accent) solid var(--color-accent);
      max-width: var(--max-width-xs);
      margin: 0 auto var(--spacing-sm);
    }

    .deck {
      text-align: left;
      font-family: var(--font-sans);
      font-size: var(--font-size-lg);
      color: var(--color-border);
      line-height: var(--leading-normal);
      color: var(--color-text);
      max-width: var(--max-width);
      margin: 0 auto var(--spacing-sm);
      margin-bottom: var(--spacing-lg);
      padding: 0 var(--spacing-md);
    }

    .byline {
      float: left;
      font-family: var(--font-sans);
      font-size: var(--font-size-sm);
      text-transform: sentence-case;
      letter-spacing: 0.05em;
      color: var(--color-accent);
      margin-bottom: var(--spacing-xxs);
    }

    .pubdate {
      float: right;
      font-family: var(--font-sans);
      font-size: var(--font-size-sm);
      text-transform: uppercase;
      letter-spacing: 0.05em;
      color: var(--color-accent);
    }

    @include mobile {
      .story-header h1 {
        font-size: var(--font-size-3xl);
      }

      .deck {
        font-size: var(--font-size-lg);
      }
    }
}
</style>