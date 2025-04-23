#  Dark mode 
Flux supports dark mode out of the box.
Light  Dark  System 
##  Set up Tailwind 
To take full advantage of Flux's dark mode controls, you will need to ensure that Tailwind CSS is configured to use the selector strategy for dark mode by adding this to your resources/views/app.css file:
 
```
@import \"tailwindcss\";
@import '../../vendor/livewire/flux/dist/flux.css';\"

@custom-variant dark (&:where(.dark, .dark *));
```

By doing this, Flux can now toggle on and off dark mode by adding/removing a .dark class to the  element of your application.
##  Disabling dark mode handling 
By default, Flux will handle the appearance of your application by adding a dark class to the html element depending on the user's system preference or selected appearance.
If you don't want Flux to handle this for you, you can remove the @fluxAppearance directive from your layout file.
 
```
<head>
    ...
--    @fluxAppearance
</head>
```

Now you can handle the appearance of your application manually.
##  JavaScript utilities 
Managing dark mode in your own application is cumbersome. Here are a few essential behaviors you have to implement:
  * Add/remove the .dark class to the  element 
  * Store the users preference in local storage 
  * Honor the system preference if system is selected 
  * Listen for changes in the system preference after a page has loaded 


To save you from this complexity, Flux provides two JavaScript/Alpine utilities for making it easy to manage dark mode:
 
```
// Get/set a users color scheme preference...
$flux.appearance = 'light|dark|system'

// Get/set the current color scheme of your app...
$flux.dark = 'true|false'
```

Given these two utilities, you can now use Alpine to easily build widgets to manage dark mode.
For example, here's how you would write a simple dark mode toggle button:
 
```
<flux:button x-data x-on:click="$flux.dark = ! $flux.dark">Toggle</flux:button>
```

Or if you wanted to allow a user to choose their preferred color scheme, you could write:
 
```
<flux:radio.group x-data x-model="$flux.appearance">
    <flux:radio value="light">Light</flux:radio>
    <flux:radio value="dark">Dark</flux:radio>
    <flux:radio value="system">System</flux:radio>
</flux:radio.group>
```

If you want to use these utilities outside of Alpine, you can instead access .appearance and .dark on the global window.Flux JavaScript object from anywhere in your application:
 
```
let button = document.querySelector('...')

button.addEventListener('click', () => {
    Flux.dark = ! Flux.dark
})
```

##  Examples 
Rather than offer a one-size-fits-~~all~~ none solution, Flux provides a few examples of how you can use these utilities to build your own dark mode controls.
##  Toggle button 
A simple toggle button to allow uesrs to control dark mode from something like a navbar or sidebar.
 
```
<flux:button x-data x-on:click="$flux.dark = ! $flux.dark" icon="moon" variant="subtle" aria-label="Toggle dark mode" />
```

##  Dropdown menu 
More robust than a simple toggle button, this dropdown menu allows users to choose between light, dark, and system modes.
Light  Dark  System 
 
```
<flux:dropdown x-data align="end">
    <flux:button variant="subtle" square class="group" aria-label="Preferred color scheme">
        <flux:icon.sun x-show="$flux.appearance === 'light'" variant="mini" class="text-zinc-500 dark:text-white" />
        <flux:icon.moon x-show="$flux.appearance === 'dark'" variant="mini" class="text-zinc-500 dark:text-white" />
        <flux:icon.moon x-show="$flux.appearance === 'system' && $flux.dark" variant="mini" />
        <flux:icon.sun x-show="$flux.appearance === 'system' && ! $flux.dark" variant="mini" />
    </flux:button>

    <flux:menu>
        <flux:menu.item icon="sun" x-on:click="$flux.appearance = 'light'">Light</flux:menu.item>
        <flux:menu.item icon="moon" x-on:click="$flux.appearance = 'dark'">Dark</flux:menu.item>
        <flux:menu.item icon="computer-desktop" x-on:click="$flux.appearance = 'system'">System</flux:menu.item>
    </flux:menu>
</flux:dropdown> 
```

##  Toggle switch 
A simple toggle switch to allow users to control dark mode from something like a settings page.
Dark mode 
 
```
<flux:switch x-data x-model="$flux.dark" label="Dark mode"  />
```

##  Segmented radio 
A simple toggle switch to allow users to control dark mode from something like a settings page.
Light  Dark  System 
 
```
<flux:radio.group x-data variant="segmented" x-model="$flux.appearance">
    <flux:radio value="light" icon="sun">Light</flux:radio>
    <flux:radio value="dark" icon="moon">Dark</flux:radio>
    <flux:radio value="system" icon="computer-desktop">System</flux:radio>
</flux:radio.group>
```

Alternatively, you can use an icon-only variant to save horizontal space:
 
```
<flux:radio.group x-data variant="segmented" x-model="$flux.appearance">
    <flux:radio value="light" icon="sun" />
    <flux:radio value="dark" icon="moon" />
    <flux:radio value="system" icon="computer-desktop" />
</flux:radio.group>      
```

