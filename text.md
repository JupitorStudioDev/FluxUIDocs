#  Text 
Consistent typographical components like text and link.
Text component
This is the standard text component for body copy and general content throughout your application.
 
```
<flux:heading>Text component</flux:heading>
<flux:text class="mt-2">This is the standard text component for body copy and general content throughout your application.</flux:text>
```

##  [Size](https://fluxui.dev/components/text#size)
Use standard Tailwind to control the size of the text so that you can more easily adapt to different screen sizes.
Larger text size
Default text size
Smaller text
 
```
<flux:text class="text-base">Base text size</flux:text>
<flux:text>Default text size</flux:text>
<flux:text class="text-xs">Smaller text</flux:text>
```

##  [Color](https://fluxui.dev/components/text#color)
Use standard Tailwind to control the color of the text so that you can more easily adapt to different screen sizes.
Strong text color
Default text color
Muted text color
Colored text
 
```
<flux:text variant="strong">Strong text color</flux:text>
<flux:text>Default text color</flux:text>
<flux:text variant="subtle">Muted text color</flux:text>
<flux:text color="blue">Colored text</flux:text>
```

##  [Link](https://fluxui.dev/components/text#link)
Use the link component to create clickable text that navigates to other pages or resources.
Visit our [documentation](https://fluxui.dev/components/text) for more information.
 
```
<flux:text>Visit our <flux:link href="#">documentation</flux:link> for more information.</flux:text>
```

##  [Link variants](https://fluxui.dev/components/text#link-variants)
Links can be styled differently based on their context and importance.
[Default link](https://fluxui.dev/components/text)
[Ghost link](https://fluxui.dev/components/text)
[Subtle link](https://fluxui.dev/components/text)
 
```
<flux:link href="#">Default link</flux:link>
<flux:link href="#" variant="ghost">Ghost link</flux:link>
<flux:link href="#" variant="subtle">Subtle link</flux:link>
```

##  Related components 
[ Heading  Create hierarchical section headings ](https://fluxui.dev/components/heading) [ Card  Containers for content with consistent styling ](https://fluxui.dev/components/card)
##  Reference 
###  [flux:text](https://fluxui.dev/components/text#fluxtext)
Prop |  Description  
---|---  
size  |  Size of the text. Options: xs, sm, base, lg. Default: base.  
variant  |  Text variant. Options: strong, subtle. Default: default.  
color  |  Color of the text. Options: default, red, orange, yellow, lime, green, emerald, teal, cyan, sky, blue, indigo, violet, purple, fuchsia, pink, rose. Default: default.  
inline  |  If true, the text element will be a span instead of a p.  
###  [flux:link](https://fluxui.dev/components/text#fluxlink)
Prop |  Description  
---|---  
href  |  The URL that the link points to. Required.  
variant  |  Link style variant. Options: default, ghost, subtle. Default: default.  
external  |  If true, the link will open in a new tab.  
