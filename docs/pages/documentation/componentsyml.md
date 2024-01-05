# Components.yml
<h4 class="fw-light">Define which React components should be added on given views.</h4><br/>

<div class="alert alert-dark bg-body mt-3 rounded-4 border" role="alert">
  <i class="bi bi-pin-angle-fill mb-1" style="font-size:23px; float: left;"></i>
  <div class="ps-3 ms-3"><b>This documentation page is still being written.</b> You might run into unfinished explainations, incorrect instructions, outdated or misinformation.</div>
</div><br/>

### **What is Components.yml?**
While you can add React components to your extension without a `Components.yml` file, they won't be applied anywhere. `Components.yml` allows you to tell Blueprint where to apply a specific component, one or multiple targets.

<br/>

### **Configuration**
The YAML file shown below contains all configuration options that are currently supported by Blueprint's components feature.

```yaml
Navigation:
  NavigationBar:
    BeforeNavigation: ""
    AdditionalItems: ""
    AfterNavigation: ""
```

<br/>

### **Paths**
Paths towards component files are **different** from how you would normally define file paths for extension configuration files.

Component file paths cannot escape the components directory **and** cannot end with `.tsx`, `.ts`, `.jsx` or `.js`.

<div class="row">
  <div class="col pt-2 mx-2">
    <span class="text-success-emphasis fw-bolder">Correct usage:</span>
<div><pre><code class="hljs language-yaml hl-escape mt-2">Option: "Component"</code></pre></div>
    <div class="mb-2"><i class="bi bi-check-lg text-success-emphasis"></i> <span class="text-success-emphasis">Points towards <code>Component.tsx</code>.</span></div>
  </div>
  <div class="col py-2 mx-2">
    <span class="text-danger-emphasis fw-bolder">Incorrect usage:</span>
<div><pre><code class="hljs language-yaml hl-escape mt-2">Option: "../Component.tsx"</code></pre></div>
    <div class="mb-2"><i class="bi bi-x-lg text-secondary"></i> <span class="text-secondary">Points towards <code>../Component.tsx.tsx</code>.</span></div>
    <div class="mb-2"><i class="bi bi-x-lg text-secondary"></i> <span class="text-secondary">Attempts to escape component directory.</span></div>
  </div>
</div>