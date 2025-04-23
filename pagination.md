Flux Pro component
This component is only available in the Pro version of Flux. 
[ Upgrade to Pro -> ](https://fluxui.dev/pricing) [ Upgrade to Pro -> ](https://fluxui.dev/pricing)
#  Pagination 
Display a series of buttons to navigate through a list of items.
Showing 1 to 5 of 24 results 
1
2 3 4 5
 
```
<!-- $orders = Order::paginate() -->
<flux:pagination :paginator="$orders" />
```

##  [Simple paginator](https://fluxui.dev/components/pagination#simple-paginator)
Use the simple paginator when working with large datasets where counting the total number of results would be expensive. The simple paginator provides \"Previous\" and \"Next\" buttons without displaying the total number of pages or records.
 
```
<!-- $orders = Order::simplePaginate() -->
<flux:pagination :paginator="$orders" />
```

##  [Large result set](https://fluxui.dev/components/pagination#large-result-set)
When working with large result sets, the pagination component automatically adapts to show a reasonable number of page links. It shows the first and last pages, along with a window of pages around the current page, and adds ellipses for any gaps to ensure efficient navigation through numerous pages.
Showing 1 to 75 of 1000 results 
1
2 3 4 5 6 7 8 9 10
...
66 67
 
```
<!-- $orders = Order::paginate(5) -->
<flux:pagination :paginator="$orders" />
```

##  Reference 
###  [flux:pagination](https://fluxui.dev/components/pagination#fluxpagination)
Prop |  Description  
---|---  
paginator  |  The paginator instance to display.  
