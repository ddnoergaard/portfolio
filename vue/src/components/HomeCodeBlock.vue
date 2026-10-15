<script setup></script>

<template>
  <div class="code-container">
    <div class="top-bar">
      <div class="text">
        &lt; / &gt; <span style="font-size: small">DeveloperController.cs</span>
      </div>
      <div class="top-bar-actions">
        <div class="text">-</div>
        <div class="text">&#9633;</div>
        <div class="text">X</div>
      </div>
    </div>
    <div class="code-block-container">
      <pre
        class="code"
        aria-hidden="true"
      ><code><span class="attr">[HttpGet]</span><br><span class="attr">[ProducesResponseType(StatusCodes.Status200OK)]</span><br><span class="attr">[ProducesResponseType(StatusCodes.Status404NotFound)]</span>
<span class="kw">public async</span> <span class="type">Task</span>&lt;<span class="type">IActionResult</span>&gt; Get(<span class="kw">int</span> year)
{
    <span class="kw">return</span> Ok(<span class="kw">new</span> <span class="type">Developer</span>
    {
        Name = <span class="str">"Daniel Nørgaard"</span>,
        BirthYear = 1998,
        Studying = <span class="str">"Computer Science"</span>,
        Academy = <span class="str">"Zealand, Roskilde"</span>
        Stack = <span class="kw">new</span>[] { <span class="str">"C#"</span>, <span class="str">".NET"</span>, <span class="str">"Vue"</span>, <span class="str">"Js"</span> },
        Specializations = <span class="str">"Backend"</span>
    });
}</code></pre>
    </div>
  </div>
</template>

<style scoped>
.code-container {
  width: 100%;
  height: 50%;
  background-color: var(--primary-text);
  border-radius: 8px;
  padding: 0.5rem;
}

.top-bar {
  display: flex;
  justify-content: space-between;
  border-bottom: 1px solid var(--secondary-text);
  padding-bottom: 0.5rem;
  transition: all ease 0.3s;
}

.top-bar:hover {
  background-color: #211b1b;
}

.top-bar-actions {
  display: flex;
  gap: 1rem;
  justify-content: center;
  cursor: pointer;
}

.text {
  color: var(--background);
  font-family:
    Consolas,
    Monaco,
    Lucida Console,
    Liberation Mono,
    DejaVu Sans Mono,
    Bitstream Vera Sans Mono,
    Courier New;
}

.text-secondary {
  color: #c6acac;
}

.code {
  color: var(--background);
  font-size: 0.9rem;
  line-height: 1.6;
}

.kw {
  color: var(--orange-primary);
}

.type {
  color: var(--sage-green-secondary);
}

.str {
  color: var(--background);
  opacity: 0.75;
}

.attr {
  color: var(--sage-green-secondary);
  opacity: 0.8;
}
</style>
