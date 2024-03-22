The term "constructor" in programming refers to a special method or function that is automatically called when an instance of a class or an object is created. Its primary purpose is to initialize the newly created object.
---
## constructor function:

 - they usually start with capital letter to distinguish from normal function
 - have **function** keyword at start
 - instance is created using the **`new`**  keyword, when a  **`new`**  keyword is used with the constructor function then a object instance is created and is referred to by  **`this`**  keyword. 
 - **`this`** keyword also defines the constructor function , it refers to the current instance of the object. Like if new object is created then the **`this`** keyword will refer and create properties for that object
``` js
    function hi(ii){
        this.ii = ii;
        this.greet= function(){
            console.log('hi vro '+this.ii)
        }
    }
    
    const j = new hi('loli');
    console.log(j.ii);
    j.greet() 
   ```

here you can new keyword is used to create a instance of function by creating a object
