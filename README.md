# JAVASCRIPT CLASSES

##### Classes are templates to create objects.<br>
#### INHERITANCE
- When parent class properties and methods extend to child classes.<br>
  <br>
  |KEYWORD|DESCRIPTION|
  |----|----|
  |`EXTENDS`|To create a child sub class that extends a parents |
  |`SUPER()`| Used so a child class calls the parent class constructor when it adds properties|
  |`STATIC`| defines a static method for a class|

##### The METHOD is CALLED ON THE CLASS NOT on AN INSTANCES of the class.<br>
- JavaScript calls a constructor method when we create a new instance of a class (see below).<br>

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
  
  #### // THIS IS ALLOWED, generateName called on the CLASS Animal

            console.log(Animal.generateName());
  
  ####  // THIS IS NOT ALLOWED, generateName called on the INSTANCE tyson
  
        const tyson = new Animal('Tyson');      //creating an instance use the new keyword which call constructor
          tyson.generateName();
  


