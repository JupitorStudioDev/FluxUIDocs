#  Header 
A full-width top navigation layout for your application.
[ Fullscreen ](https://fluxui.dev/demo/header) Demo  Code 
![](https://fluxui.dev/img/demo/layout-header.png) ![](https://fluxui.dev/img/demo/layout-header-dark.png)
 
```
<head>
    <!-- ... -->

    @fluxAppearance
</head>
<body class="min-h-screen bg-white dark:bg-zinc-800">
    <flux:header container class="bg-zinc-50 dark:bg-zinc-900 border-b border-zinc-200 dark:border-zinc-700">
        <flux:sidebar.toggle class="lg:hidden" icon="bars-2" inset="left" />

        <flux:brand href="#" logo="https://fluxui.dev/img/demo/logo.png" name="Acme Inc." class="max-lg:hidden dark:hidden" />
        <flux:brand href="#" logo="https://fluxui.dev/img/demo/dark-mode-logo.png" name="Acme Inc." class="max-lg:hidden! hidden dark:flex" />

        <flux:navbar class="-mb-px max-lg:hidden">
            <flux:navbar.item icon="home" href="#" current>Home</flux:navbar.item>
            <flux:navbar.item icon="inbox" badge="12" href="#">Inbox</flux:navbar.item>
            <flux:navbar.item icon="document-text" href="#">Documents</flux:navbar.item>
            <flux:navbar.item icon="calendar" href="#">Calendar</flux:navbar.item>

            <flux:separator vertical variant="subtle" class="my-2"/>

            <flux:dropdown class="max-lg:hidden">
                <flux:navbar.item icon:trailing="chevron-down">Favorites</flux:navbar.item>

                <flux:navmenu>
                    <flux:navmenu.item href="#">Marketing site</flux:navmenu.item>
                    <flux:navmenu.item href="#">Android app</flux:navmenu.item>
                    <flux:navmenu.item href="#">Brand guidelines</flux:navmenu.item>
                </flux:navmenu>
            </flux:dropdown>
        </flux:navbar>

        <flux:spacer />

        <flux:navbar class="me-4">
            <flux:navbar.item icon="magnifying-glass" href="#" label="Search" />
            <flux:navbar.item class="max-lg:hidden" icon="cog-6-tooth" href="#" label="Settings" />
            <flux:navbar.item class="max-lg:hidden" icon="information-circle" href="#" label="Help" />
        </flux:navbar>

        <flux:dropdown position="top" align="start">
            <flux:profile avatar="https://fluxui.dev/img/demo/user.png" />

            <flux:menu>
                <flux:menu.radio.group>
                    <flux:menu.radio checked>Olivia Martin</flux:menu.radio>
                    <flux:menu.radio>Truly Delta</flux:menu.radio>
                </flux:menu.radio.group>

                <flux:menu.separator />

                <flux:menu.item icon="arrow-right-start-on-rectangle">Logout</flux:menu.item>
            </flux:menu>
        </flux:dropdown>
    </flux:header>

    <flux:sidebar stashable sticky class="lg:hidden bg-zinc-50 dark:bg-zinc-900 border rtl:border-r-0 rtl:border-l border-zinc-200 dark:border-zinc-700">
        <flux:sidebar.toggle class="lg:hidden" icon="x-mark" />

        <flux:brand href="#" logo="https://fluxui.dev/img/demo/logo.png" name="Acme Inc." class="px-2 dark:hidden" />
        <flux:brand href="#" logo="https://fluxui.dev/img/demo/dark-mode-logo.png" name="Acme Inc." class="px-2 hidden dark:flex" />

        <flux:navlist variant="outline">
            <flux:navlist.item icon="home" href="#" current>Home</flux:navlist.item>
            <flux:navlist.item icon="inbox" badge="12" href="#">Inbox</flux:navlist.item>
            <flux:navlist.item icon="document-text" href="#">Documents</flux:navlist.item>
            <flux:navlist.item icon="calendar" href="#">Calendar</flux:navlist.item>

            <flux:navlist.group expandable heading="Favorites" class="max-lg:hidden">
                <flux:navlist.item href="#">Marketing site</flux:navlist.item>
                <flux:navlist.item href="#">Android app</flux:navlist.item>
                <flux:navlist.item href="#">Brand guidelines</flux:navlist.item>
            </flux:navlist.group>
        </flux:navlist>

        <flux:spacer />

        <flux:navlist variant="outline">
            <flux:navlist.item icon="cog-6-tooth" href="#">Settings</flux:navlist.item>
            <flux:navlist.item icon="information-circle" href="#">Help</flux:navlist.item>
        </flux:navlist>
    </flux:sidebar>

    <flux:main container>
        <flux:heading size="xl" level="1">Good afternoon, Olivia</flux:heading>

        <flux:text class="mt-2 mb-6 text-base">Here's what's new today</flux:text>

        <flux:separator variant="subtle" />
    </flux:main>

    @fluxScripts
</body>
```

##  [Secondary sidebar](https://fluxui.dev/layouts/header#secondary-sidebar)
Use a sidebar for secondary navigation.
[ Fullscreen ](https://fluxui.dev/demo/header-with-sidebar) Demo  Code 
![](https://fluxui.dev/img/demo/layout-header-with-sidebar.png) ![](https://fluxui.dev/img/demo/layout-header-with-sidebar-dark.png)
 
```
<head>
    <!-- ... -->

    @fluxAppearance
</head>
<body class="min-h-screen bg-white dark:bg-zinc-800">
    <flux:header container class="bg-zinc-50 dark:bg-zinc-900 border-b border-zinc-200 dark:border-zinc-700">
        <flux:sidebar.toggle class="lg:hidden" icon="bars-2" />

        <flux:brand href="#" logo="https://fluxui.dev/img/demo/logo.png" name="Acme Inc." class="max-lg:hidden dark:hidden" />
        <flux:brand href="#" logo="https://fluxui.dev/img/demo/dark-mode-logo.png" name="Acme Inc." class="max-lg:hidden! hidden dark:flex" />

        <flux:navbar class="-mb-px max-lg:hidden">
            <flux:navbar.item icon="home" href="#" current>Home</flux:navbar.item>
            <flux:navbar.item icon="inbox" badge="12" href="#">Inbox</flux:navbar.item>
            <flux:navbar.item icon="document-text" href="#">Documents</flux:navbar.item>
            <flux:navbar.item icon="calendar" href="#">Calendar</flux:navbar.item>

            <flux:separator vertical variant="subtle" class="my-2"/>

            <flux:dropdown class="max-lg:hidden">
                <flux:navbar.item icon:trailing="chevron-down">Favorites</flux:navbar.item>

                <flux:navmenu>
                    <flux:navmenu.item href="#">Marketing site</flux:navmenu.item>
                    <flux:navmenu.item href="#">Android app</flux:navmenu.item>
                    <flux:navmenu.item href="#">Brand guidelines</flux:navmenu.item>
                </flux:navmenu>
            </flux:dropdown>
        </flux:navbar>

        <flux:spacer />

        <flux:navbar class="me-4">
            <flux:navbar.item icon="magnifying-glass" href="#" label="Search" />
            <flux:navbar.item class="max-lg:hidden" icon="cog-6-tooth" href="#" label="Settings" />
            <flux:navbar.item class="max-lg:hidden" icon="information-circle" href="#" label="Help" />
        </flux:navbar>

        <flux:dropdown position="top" align="start">
            <flux:profile avatar="https://fluxui.dev/img/demo/user.png" />

            <flux:menu>
                <flux:menu.radio.group>
                    <flux:menu.radio checked>Olivia Martin</flux:menu.radio>
                    <flux:menu.radio>Truly Delta</flux:menu.radio>
                </flux:menu.radio.group>

                <flux:menu.separator />

                <flux:menu.item icon="arrow-right-start-on-rectangle">Logout</flux:menu.item>
            </flux:menu>
        </flux:dropdown>
    </flux:header>

    <flux:sidebar stashable sticky class="lg:hidden bg-zinc-50 dark:bg-zinc-900 border-r rtl:border-r-0 rtl:border-l border-zinc-200 dark:border-zinc-700">
        <flux:sidebar.toggle class="lg:hidden" icon="x-mark" />

        <flux:brand href="#" logo="https://fluxui.dev/img/demo/logo.png" name="Acme Inc." class="px-2 dark:hidden" />
        <flux:brand href="#" logo="https://fluxui.dev/img/demo/dark-mode-logo.png" name="Acme Inc." class="px-2 hidden dark:flex" />

        <flux:navlist variant="outline">
            <flux:navlist.item icon="home" href="#" current>Home</flux:navlist.item>
            <flux:navlist.item icon="inbox" badge="12" href="#">Inbox</flux:navlist.item>
            <flux:navlist.item icon="document-text" href="#">Documents</flux:navlist.item>
            <flux:navlist.item icon="calendar" href="#">Calendar</flux:navlist.item>

            <flux:navlist.group expandable heading="Favorites" class="max-lg:hidden">
                <flux:navlist.item href="#">Marketing site</flux:navlist.item>
                <flux:navlist.item href="#">Android app</flux:navlist.item>
                <flux:navlist.item href="#">Brand guidelines</flux:navlist.item>
            </flux:navlist.group>
        </flux:navlist>

        <flux:spacer />

        <flux:navlist variant="outline">
            <flux:navlist.item icon="cog-6-tooth" href="#">Settings</flux:navlist.item>
            <flux:navlist.item icon="information-circle" href="#">Help</flux:navlist.item>
        </flux:navlist>
    </flux:sidebar>

    <flux:main container>
        <div class="flex max-md:flex-col items-start">
            <div class="w-full md:w-[220px] pb-4 me-10">
                <flux:navlist>
                    <flux:navlist.item href="#" current>Dashboard</flux:navlist.item>
                    <flux:navlist.item href="#" badge="32">Orders</flux:navlist.item>
                    <flux:navlist.item href="#">Catalog</flux:navlist.item>
                    <flux:navlist.item href="#">Payments</flux:navlist.item>
                    <flux:navlist.item href="#">Customers</flux:navlist.item>
                    <flux:navlist.item href="#">Billing</flux:navlist.item>
                    <flux:navlist.item href="#">Quotes</flux:navlist.item>
                    <flux:navlist.item href="#">Configuration</flux:navlist.item>
                </flux:navlist>
            </div>

            <flux:separator class="md:hidden" />

            <div class="flex-1 max-md:pt-6 self-stretch">
                <flux:heading size="xl" level="1">Good afternoon, Olivia</flux:heading>

                <flux:text class="mb-6 mt-2 text-base">Here's what's new today</flux:text>

                <flux:separator variant="subtle" />
            </div>
        </div>
    </flux:main>

    @fluxScripts
</body>
```


##  Reference 
###  [flux:header](https://fluxui.dev/layouts/header#fluxheader)
Prop |  Description  
---|---  
sticky  |  When present, makes the header sticky when scrolling.  
container  |  When present, constrains the header content to a container width. 

Slot |  Description  
---|---  
default  |  Content to display within the header, typically including branding, navigation, and user profile elements.  

CSS |  Description  
---|---  
class  |  Additional CSS classes applied to the header. Common uses: bg-zinc-50, border-b, sticky, etc.  
###  [flux:sidebar.toggle](https://fluxui.dev/layouts/header#fluxsidebartoggle)

Attribute |  Description  
---|---  
icon  |  The icon to display in the toggle button (e.g., bars-2, x-mark).  
inset  |  Positioning of the toggle button (e.g., left).  

CSS |  Description  
---|---  
class  |  Additional CSS classes applied to the toggle button. Common uses: lg:hidden to show only on mobile.  
###  [flux:main](https://fluxui.dev/layouts/header#fluxmain)

Prop |  Description  
---|---  
container  |  When present, constrains the main content to a container width.  

Slot |  Description  
---|---  
default  |  Content to display within the main content area.  
