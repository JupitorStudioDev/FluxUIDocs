Flux Pro component
This component is only available in the Pro version of Flux. 
[ Upgrade to Pro -> ](https://fluxui.dev/pricing) [ Upgrade to Pro -> ](https://fluxui.dev/pricing)
#  Command palette 
A searchable list of commands.
Assign to… 
⌘A
Create new file  Create new project 
⌘⇧N
Documentation  Changelog  Settings 
⌘,
No results found 
 
```
<flux:command>
    <flux:command.input placeholder="Search..." />

    <flux:command.items>
        <flux:command.item wire:click="..." icon="user-plus" kbd="âA">Assign toâ¦</flux:command.item>
        <flux:command.item wire:click="..." icon="document-plus">Create new file</flux:command.item>
        <flux:command.item wire:click="..." icon="folder-plus" kbd="ââ§N">Create new project</flux:command.item>
        <flux:command.item wire:click="..." icon="book-open">Documentation</flux:command.item>
        <flux:command.item wire:click="..." icon="newspaper">Changelog</flux:command.item>
        <flux:command.item wire:click="..." icon="cog-6-tooth" kbd="â,">Settings</flux:command.item>
    </flux:command.items>
</flux:command> 
```

##  [As a modal](https://fluxui.dev/components/command#as-a-modal)
Open a command palette as a modal for quick access to frequently used commands.
Search... 
⌘K 
Assign to… 
⌘A
Create new file  Create new project 
⌘⇧N
Documentation  Changelog  Settings 
⌘,
No results found 
 
```
<flux:modal.trigger name="search" shortcut="cmd.k">
    <flux:input as="button" placeholder="Search..." icon="magnifying-glass" kbd="âK" />
</flux:modal.trigger>

<flux:modal name="search" variant="bare" class="w-full max-w-[30rem] my-[12vh] max-h-screen overflow-y-hidden">
    <flux:command class="border-none shadow-lg inline-flex flex-col max-h-[76vh]">
        <flux:command.input placeholder="Search..." closable />

        <flux:command.items>
            <flux:command.item icon="user-plus" kbd="âA">Assign toâ¦</flux:command.item>
            <flux:command.item icon="document-plus">Create new file</flux:command.item>
            <flux:command.item icon="folder-plus" kbd="ââ§N">Create new project</flux:command.item>
            <flux:command.item icon="book-open">Documentation</flux:command.item>
            <flux:command.item icon="newspaper">Changelog</flux:command.item>
            <flux:command.item icon="cog-6-tooth" kbd="â,">Settings</flux:command.item>
        </flux:command.items>
    </flux:command>
</flux:modal>    
```

##  Reference 
###  [flux:command](https://fluxui.dev/components/command#fluxcommand)
The root command palette component that wraps the input and items.
Attribute |  Description  
---|---  
data-flux-command  |  Applied to the root element for styling and identification.  
###  [flux:command.input](https://fluxui.dev/components/command#fluxcommandinput)
Prop |  Description  
---|---  
clearable  |  If true, displays a clear button when the input has content.  
closable  |  If true, displays a close button to dismiss the command palette.  
icon  |  Name of the icon displayed at the start of the input. Default: magnifying-glass.  
placeholder  |  Placeholder text displayed when the input is empty.  
###  [flux:command.items](https://fluxui.dev/components/command#fluxcommanditems)
Container for command items. No props available.
###  [flux:command.item](https://fluxui.dev/components/command#fluxcommanditem)
Prop |  Description  
---|---  
icon  |  Name of the icon displayed at the start of the item.  
icon:variant  |  Visual style of the icon. Options: outline (default), solid, mini, micro.  
kbd  |  Keyboard shortcut hint displayed at the end of the item (e.g., ⌘K).  

Attribute |  Description  
---|---  
data-flux-command-item  |  Applied to the item element for styling and identification.  
