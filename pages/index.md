# Welcome to Evidence! 👋

Evidence is a BI tool you can write using just SQL and Markdown.

{#if innerWidth <= 850}

_Note: Evidence has a first-class **mobile** support, but a wider browser window will show **desktop** mode._

{/if}

👉 _If this is your first time using Evidence, try the [**Tutorial** 📚](/tutorial:-basics)._

<br>

## Installing Locally

To connect your own database, you will need to install Evidence locally:

<pre><code style="display: block; width: fit-content;">
npx degit evidence-dev/template my-project
cd my-project
npm install
npm run dev
</code></pre>

Evidence requires **Node** and **npm**. For more detailed installation instructions, including dependencies, see <a href="https://docs.evidence.dev/getting-started/install-evidence" target="_blank">here</a>.

## Learning more

- <a href='https://docs.evidence.dev/getting-started/install-evidence' target="_blank">Getting Started Walkthrough</a>
- <a href='https://www.evidence.dev' target="_blank">Evidence.dev</a>
- <a href='https://github.com/evidence-dev/evidence' target="_blank">Github</a>

<script>
	$: innerWidth = 0
</script>

<svelte:window bind:innerWidth />
