# react-use-hover

Detect whether the mouse is hovering an element. The hook returns a ref and a boolean value indicating whether the element with that ref is currently being hovered. Just add the returned ref to any element whose hover state you want to monitor. One potential bug with this method: If you have logic that changes the element that hoverRef is added to then your event listeners will not necessarily get applied to the new element. If you need this functionality then use this alternate version that utilizes a callback ref.

**Usage**

```javascript
npm i @reactdev/react-use-hover
```

```javascript
import useHover from "@reactdev/react-use-hover";
```

```javascript
function App() {
  const [hoverRef, isHovered] = useHover();

  return <div ref={hoverRef}>{isHovered ? "😁" : "☹️"}</div>;
}
```
