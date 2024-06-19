# JAVASCRIPT CLASSES


- Classes are templates for objects.<br>
- JavaScript calls a constructor method when we create a new instance of a class.<br>
- INHERITANCE is when properties and methods of a parent class extend to child classes.<br>
-'extends' keyword to creates a subclass.<br>
-'super' keyword calls the constructor() of a parent class.<br>
-Static methods are called on the class, but NOT on AN INSTANCES of the class.<br>
- To call a static method we call it on the original class

         class Animal {
          constructor(name) {
            this._name = name;
            this._behavior = 0;
          }
            
          static generateName() {
            const names = ['Angel', 'Spike', 'Buffy', 'Willow', 'Tara'];
            const randomNumber = Math.floor(Math.random()*5);
            return names[randomNumber];
          }
        }
  
        console.log(Animal.generateName());
  
  #### // THIS IS ALLOWED
  
        const tyson = new Animal('Tyson');
          tyson.generateName();
  
  ####  // THIS IS NOT ALLOWED

