# changes

## App.tsx

1. Root div

Change className="min-h-screen flex flex-col" to className="h-screen flex flex-col overflow-hidden".

2. Main

Change className="flex-1 " to className="flex-1 overflow-auto".

---

## Header.tsx

3. Header element

Change className="w-full max-w-5xl mx-auto flex items-center pr-4" to className="w-full".

4. Wrap the nav in a div

Right after the opening <header> tag, add:

```html
<div className="max-w-5xl mx-auto flex items-center pr-4"></div>
```

and move all existing header content (all Buttons and the DropdownMenu) inside this div.

5. Close the wrapper

Before the closing </header>,

add:

```
</div>
```

so the new div correctly wraps the nav content.

---

**Result:** The app is fixed to the viewport height, the header bar is full width with nav still centered in a max-w-5xl band, and only the main area scrolls (scrollbar only there).
