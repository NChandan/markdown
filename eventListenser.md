# Event Listeners

## Bubbling 
 neares to farest (inside to outside)



```javascript
document.addEventListener("click", e => {
    console.log("Document Bubbling")
})

grandparent.addEventListener("click", e => {
    console.log("Document Bubbling")
})

parent.addEventListener('click', e => {
    console.log("Parent Bubbling")
})

child.addEventListener('click', e => {
    console.log("Child Bubbling")
})
```

```
<!-- Output -->
 Child
 Parent
 grandparent
 Document
```

##  Capturing 
  **{capture:true} outside to inside**


```javascript
grandparent.addEventListener('click', e => {
    console.log("grandparent capture")
}, { capture: true })

parent.addEventListener('click', e => {
    // e.stopPropagation() // stop after this run
    console.log("Parent capture") 
}, { capture: true })

child.addEventListener('click', e => {
    console.log("Child capture")
}, { capture: true })

document.addEventListener("click", e => {
    console.log("Document capture")
}, { capture: true })
```


```
<!-- Output -->
Document vcapture
grandparent capture
Parent capture
Child capture
```

## stopPropagation

-> Prevent running of remaining code

```javascript
parent.addEventListener('click', e => {
    e.stopPropagation() 
    console.log("Parent Bubbling")
})


grandparent.addEventListener("click", e => {
    console.log("grandparent Bubbling")
})

child.addEventListener('click', e => {
    console.log("Child Bubbling")
})

```
```
<!-- Output -->
 Child Bubbling
```


## Remoev Event
 Run once and removes after that
 ```javascript
child.removeEventListener('click', e => {
console.log("Child Bubbling")
})

 ```
