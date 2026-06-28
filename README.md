# Quickstart for Bitasmbl project (SvelteKit)

## 1) Install Bitasmbl-CLI package

```bash
npm i bitasmbl-cli
```

## 2) Run bitasmbl command to set up the project

```bash
bitasmbl pull --repoUrl https://github.com/he1snber8/Bitasmbl_masveltekito_b66_417 --appId 417 --repoId 241
```

## 3) Enter into the main directory and start coding!

```bash
cd Bitasmbl_masveltekito_b66_417
```

## Customize requirements in a way you like

Bitasmbl organizes development into requirements. Each requirement describes a feature or implementation goal and can define suggested file locations through a `paths` array.

The `paths` property acts as a mapping guideline, helping contributors understand where related code should live.

You can customize `paths` mappings through the `bitasmbl.json` file.

{"Requirement":"Build habit tracker UI","Paths":["**/src/routes/**","**/src/lib/components/habits/**","**/src/lib/features/habits/**"]}

## Requirement Evaluation

Bitasmbl includes a requirement evaluation workflow that lets contributors select a task and submit work for validation.

Run:

```bash
bitasmbl evaluate
```

Example output:

<pre>
? Available Requirements:

❯ [<span style="color:#9333ea">1</span>] <span style="color:#9333ea"> Define portfolio layout </span>            [3]
  [2] Build showcase components            [3]
  [3] Implement navigation routing         [3]
</pre>

`[x]` on the right represents the number of submission attempts remaining for a requirement.

## Example evaluation result

```svelte
<!--
|--------------------------------------------------------------------------
| BITASMBL EVALUATION
|--------------------------------------------------------------------------
| REQUIREMENT:
| Build portfolio landing page
|
| SCORE: 22/100
| STATUS: FAIL ✕
|
| INSIGHT:
| The page renders basic static content but does not use reusable components,
| structured data, responsive sections, or route-level organization.
|--------------------------------------------------------------------------
-->

<script lang="ts">
  const projects = ["E-commerce App", "Portfolio Site"];
</script>

<main>
  <h1>Hello from SvelteKit</h1>

  <section>
    <h2>Projects</h2>

    {#each projects as project}
      <p>{project}</p>
    {/each}
  </section>
</main>
```

## Learn More

For complete command references, workflow explanations, and additional documentation, visit:

👉 [Bitasmbl Documentation](https://bitasmbl.com/docs)
