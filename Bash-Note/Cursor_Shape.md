# To change the cursor shape to a box, add this to `~/.bashrc`:

```
echo -e '\e[2 q'
```

### Cursor Shapes:
- `\e[0 q` → Default (blinking block)  
- `\e[1 q` → Blinking block  
- `\e[2 q` → Steady block  
- `\e[3 q` → Blinking underline  
- `\e[4 q` → Steady underline  
- `\e[5 q` → Blinking bar  
- `\e[6 q` → Steady bar  

Reload with:  
```
source ~/.bashrc
```
