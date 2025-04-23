#  Heading 
A consistent heading component for your application.
User profile
This information will be displayed publicly.
 
```
<flux:heading>User profile</flux:heading>
<flux:text class="mt-2">This information will be displayed publicly.</flux:text>
```

##  [Sizes](https://fluxui.dev/components/heading#sizes)
Flux offers three different heading sizes that should cover most use cases in your app.
Default
14px · Use liberally—think input and toast labels.
Large
16px · Use sparingly—think modal and card headings.
Extra large
24px · Use rarely—think hero text.
 
```
<flux:heading>Default</flux:heading>
<flux:heading size="lg">Large</flux:heading>
<flux:heading size="xl">Extra large</flux:heading>
```

##  [Heading level](https://fluxui.dev/components/heading#heading-level)
Control the heading level: h1, h2, h3, that will be used for the heading element. Without a level prop, the heading will default to a div.
### User profile
This information will be displayed publicly.
 
```
<flux:heading level="3">User profile</flux:heading>
<flux:text class="mt-2">This information will be displayed publicly.</flux:text>
```

##  Examples 
###  [Leading subheading](https://fluxui.dev/components/heading#leading-subheading)
Subheadings can be placed above headings for a more interesting arrangment.
Year to date
$7,532.16
15.2%
 
```
<div>
    <flux:text>Year to date</flux:text>

    <flux:heading size="xl" class="mb-1">$7,532.16</flux:heading>

    <div class="flex items-center gap-2">
        <flux:icon.arrow-trending-up variant="micro" class="text-green-600 dark:text-green-500" />

        <span class="text-sm text-green-600 dark:text-green-500">15.2%</span>
    </div>
</div>
```


##  Reference 
###  [flux:heading](https://fluxui.dev/components/heading#fluxheading)
Prop |  Description  
---|---  
size  |  Size of the heading. Options: base, lg, xl. Default: base.  
level  |  HTML heading level. Options: 1, 2, 3, 4. Default: renders as a div if not specified.  
accent  |  If true, applies accent color styling to the heading.  
###  [flux:text](https://fluxui.dev/components/heading#fluxtext)
Prop |  Description  
---|---  
size  |  Size of the text. Options: sm, base, lg, xl. Default: base.  
