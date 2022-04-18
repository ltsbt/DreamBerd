# DreamBerd
DreamBerd is a perfect programming language.

## Exclamation Marks!
Be bold! End every statement with an exclamation mark!
```c
print("Hello world")!
```

If you're feeling extra-bold, you can use even more!!!
```c
print("Hello world")!!!
```

If you're unsure, that's ok. You can put a question mark at the end of a line instead. It prints debug information about that line to the console for you.
```c
print("Hello world")?
```

You might be wondering what DreamBerd uses for the 'not' operator, which is an exclamation mark in most other languages. That's simple - the 'not' operator is a semi-colon instead.
```c
if (;false) {
    print("Hello world")!
}
```

## Declarations
There are four types of declaration. Constant constants can't be changed in any way.
```java
const const name = "Luke"!
```

Constant variables can be edited, but not re-assigned.
```java
const var name = "Luke"!
name.pop()!
name.pop()!
```

Variable constants can be re-assigned, but not edited.
```java
var const name = "Luke"!
name = "Lu"!
```

Variable variables can be re-assigned and edited.
```java
var var name = "Luke"!
name = "Lu"!
name.push("ke")!
```

## Booleans
Booleans can be `true`, `false` or `maybe`.
```java
const var KEYS = {}!
on("keydown", e => KEYS[e.key] = true)!
on("keyup", e => KEYS[e.key] = false)!

function isKeyDown(key) => {
    if (KEYS[key] === undefined) return maybe!
    return KEYS[key]!
}
```

## Equality
JavaScript lets you do different levels of comparison. `==` for loose comparison, and `===` for a more precise check. DreamBerd takes this to another level. You can use `==` to do a loose check.
```java
3.14 == "3.14"! //true
```

You can use `===` to do a more precise check.
```java
3.14 === "3.14"! //false
```

You can use `====` to be even more precise!
```java
const const pi = 3.14!
print(pi ==== pi)! //true
print(3.14 ==== 3.14)! //true
print(3.14 ==== pi)! //false
```

If you want to be much less precise, you can use `=`.
```java
3 = 3.14! //true
```

## Class
You can make classes, but you can only ever make one instance of them.
```java
class Player {
    const var health = 10!
}

const var player1 = new Player()!
const var player2 = new Player()! //Error: Can't have more than one 'Player' instance!
```

This is how you could do this:
```java
class PlayerMaker {
    function makePlayer() => {
        class Player {
            const var health = 10!
        }
        const const player = new Player()!
        return player!
    }
}

const const playerMaker = new PlayerMaker()!
const var player1 = playerMaker.makePlayer()!
const var player2 = playerMaker.makePlayer()!
```

## Types
Type annotations are optional.
```java
const var age: Int = 28!
```
Strings are just arrays of characters.
```java
String == Char[]!
```
Integers are just arrays of digits.
```java
Int == Digit[]!
```
If you want to use a binary representation for numbers, `Int9` and `Int99` types are also available.
```java
const var age: UInt9 = 28!
```

## File Structure
Write five or more equals signs to start a new file. This removes the need for multiple files or any build process.
```java
const const score = 5!
print(score)! //5

=====================

const const score = 3!
print(score)! //3

```

You can give files names.
```java
======= add.db =======
function add(a, b) => {
    return a + b!
}
```

## Export
Many languages allow you to import things from specific files. In DreamBerd, importing is simpler. Instead, you export _to_ specific files!
```java
===== add.db ==
function add(a, b) => {
    return a + b!
}

export add to "main.db"!

===== main.db ==
import add!
add(3, 2)!
```
