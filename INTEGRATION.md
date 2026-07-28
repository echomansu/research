# Adding the Climate Change Simulator page to echomansu.github.io/research

Everything is self-contained: `smile-climate.html` links to your existing `styles.css`
and carries its own page-specific CSS in a `<style>` block, so **no changes to
`styles.css` are required**.

---

## Step 1 — Copy the page into the repo

Drop `smile-climate.html` into the **root of the `research` repo**, next to
`index.html`, `research.html`, `smile.html`, and `styles.css`.

It will be live at:

```
https://echomansu.github.io/research/smile-climate.html
```

---

## Step 2 — Link it from `research.html`

Your research page currently has an unlinked tile called **"Climate Earth"** (last tile
in the grid). Replace that line:

```html
<article class="tile"><span class="badge">Project</span><h4>Climate Earth</h4><p>Simulation-based climate learning for systems thinking and classroom inquiry.</p></article>
```

with:

```html
<article class="tile"><span class="badge">Project</span><h4><a href="smile-climate.html">Climate Change Simulator</a></h4><p>Role-based 3D climate policy simulation with an AI conversational agent, part of the SMILE program.</p></article>
```

---

## Step 3 — Link it from `smile.html`

Add this section to `smile.html` (a good spot is right after the hero card, before
"Research Questions") so the SMILE hub points to its three environments:

```html
<section class="card">
  <h2>Environments in the SMILE Program</h2>
  <div class="grid-3">
    <article class="tile">
      <span class="badge">Environment</span>
      <h4>Flocking Simulator</h4>
      <p>Emergent collective behavior in sheep, duck and bat groups, supported by the LLM-based Butterfly Tutor.</p>
    </article>
    <article class="tile">
      <span class="badge">Environment</span>
      <h4><a href="smile-climate.html">Climate Change Simulator</a></h4>
      <p>Role-based climate policy simulation with a responsive 3D world and the AI agent Bobby.</p>
    </article>
    <article class="tile">
      <span class="badge">Environment</span>
      <h4>Third Environment</h4>
      <p>Add the name and one-line description of the third environment here.</p>
    </article>
  </div>
</section>
```

---

## Step 4 — Optional: add screenshots

The page contains a ready-made **"Inside the Environment"** section, currently hidden.

1. Create the folder `media/smile-climate/` in the repo.
2. Add four images named:
   - `simulation.png` — main split-screen simulation view
   - `policy_decision.png` — policy decision screen
   - `extreme_events.png` — extreme events in the 3D world
   - `bobby_chat.png` — a chat exchange with Bobby
3. In `smile-climate.html`, find this line and **delete the `style="display:none"` part**:

```html
<section class="card" style="display:none">
```

(If you'd rather not add screenshots, delete that whole section instead — leaving it
hidden is also fine, it simply won't show.)

---

## Step 5 — Things to fill in or decide

- **SMILE acronym.** Your existing `smile.html` expands SMILE as *"Science
  Misconception-Focused Immersive Learning Environment."* The new page uses *"Systems
  Modeling in Intelligent Learning Environment."* Pick one and make both pages agree.
- **The third environment.** Two `TODO` tiles (one on this page, one in the Step 3
  snippet) are placeholders for the third SMILE environment.
- **Project team card.** Add any collaborators I don't know about.
- **Scientific outputs.** Currently lists only the bachelor thesis; add papers, talks,
  or a live demo link as they appear.
- **Result reporting.** The Key Findings section quotes specific numbers from the thesis
  study. Confirm you're comfortable publishing those before the thesis is formally
  deposited or the paper is out.
