# Youtube Channel TechSith Javascript
https://www.youtube.com/user/techSithTube/playlists


## Object creation patterns
* Constructor Pattern
* Factory Pattern
* Prototype Pattern
* Dynamic Prototype Pattern

Javascript has no formal classes support

### Constructor pattern
* for simple obect creation

### Factory Constructor pattern
* all instances have all the properties (redundant)


## Method creation
Pizza.getCrust = function(){
  return this.crust;
};

<!-- Prototype is a shared area to store things -->
Pizza.prototype.getCrust = function(){
  return this.crust;
};

### Prototype pattern
* you have to create an empty Object
* you can't create everything in one line
* can be confusing

### Dynamic Prototype pattern
* useful for many object creations

# Closures in Javascript
## Lexical scoping
Variables outside the function/object are accessible due to lexical scoping.

* Every function where you use a variable from outside is a closure
* Looking at functions console.dir(functionWithoutbrackets);
* function brackets tell to execute it
* 'closures are just functions with preserved data (locally used)'
