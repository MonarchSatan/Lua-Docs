* `--@shortcut_func purchase item in store gems.`

* `sendPacket`

* **properties:**

`int: type`
`string: packet`

```lua
function purchase(str)
sendPacket(2, 'action|buy\nitem|'.. str)
end 

purchase('world_lock')
```

* `--@shorcut_func get amount of item in inventory.`

* `getInventory`

* **properties:**

`int: item`
`int: amount`

```lua
function getItemCount(int_item)
for _, item in pairs(getInventory()) do
if item.id == tonumber(int_item) then
return item.amount
end
end
return 0
end

logToConsole('i have '.. getItemCount(242) ..' world lock!')
```