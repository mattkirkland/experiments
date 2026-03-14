# experiments

Web experiments and prototypes.

## Adding a new experiment

1. Create a new folder with your experiment name (e.g., `my-experiment/`)
2. Add your files (at minimum an `index.html`)
3. **Add an entry to the root `index.html`** so it appears on the homepage

Use the template in `index.html`:

```html
<a href="/experiment-name/" class="experiment">
  <h2>Experiment Title</h2>
  <p>Brief description of what this experiment does or explores.</p>
  <div class="meta">Month Year</div>
</a>
```
