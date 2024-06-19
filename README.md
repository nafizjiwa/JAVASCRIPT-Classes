# JAVASCRIPT CLASSES


#### Classes are templates for objects.<br>
- JavaScript calls a constructor method when we create a new instance of a class.<br>
         constructor() {                }
- INHERITANCE is when properties and methods of a parent class extend to child classes.<br>
  <br>
  |KEYWORD|DESCRIPTION|
  |----|----|
  |`EXTENDS`|To create a child sub class that extends a parents |
  |`SUPER`| A child class constructor calls the parent class constructor using the super() method|
  |`STATIC`| defines a static method for a class|

##### The METHOD is CALLED ON THE CLASS NOT on AN INSTANCES of the class.<br>

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
        
        // Child class
         class Cat extends Animal {
           constructor(name, usesLiter) {
             super(name);
             this.usesLiter = usesliter;
           }
         }
  
  #### // THIS IS ALLOWED, called on the CLASS Animal

            console.log(Animal.generateName());
  
  ####  // THIS IS NOT ALLOWED called on the INSTANCE tyson
  
        const tyson = new Animal('Tyson');            //creating an instance
          tyson.generateName();
  


