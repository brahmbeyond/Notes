The term "constructor" in programming refers to a special method or function that is automatically called when an instance of a class or an object is created. Its primary purpose is to initialize the newly created object.
---
## constructor function:

 - they usually start with capital letter to distinguish from normal function
 - have **function** keyword at start
 - instance is created using the **`new`**  keyword, when a  **`new`**  keyword is used with the constructor function then a object instance is created and is referred to by  **`this`**  keyword. 
 - **`this`** keyword also defines the constructor function , it refers to the current instance of the object. Like if new object is created then the **`this`** keyword will refer and create properties for that object
``` js
    function hi(ii){
        this.ii = ii;    //this keyword to tell the current object
        // that this property is belongs to that object 
        this.greet= function(){
            console.log('hi vro '+this.ii)
        }
    }
    
    const j = new hi('loli');
    console.log(j.ii);
    j.greet()   
   ```

## classes
classes are like blueprint which has defined in all properties and then those properties are given values by creating object of classes.
like a blueprint of a house is class. the real house made is object .
```js
class House{
    constructor(color){    // constructor define all the properties of the class which it haves 
        this.color = color;
    }
    sofa(){                       // this function will be shared among all the objects which will be created
        console.log('the house color is '+ this.color)
    }
}

const ho1 = new House('red');   // a object is created by using new keyword
console.log(ho1.color);
ho1.sofa()
```
in above code class House is blueprint , with properties defined in constructor, ho1 is the object created using that blueprint and it defined a value (here color) so that blueprint becomes real.
sane blueprint can be used to create many houses or objects with their own properties like different colors.

but like all houses will have sofa like here in this class sofa() will be shared among every created object
