# Module-3Assignment
```

Create a class Car with the following properties:
● brand: a string representing the brand of the car
● model: a string representing the model of the car
● year: an integer representing the year the car was made
● milesDriven: a double representing the number of miles driven by the car
The class should have the following methods:
● drive(double miles): a method that takes a double parameter representing the
number of miles driven and adds it to the milesDriven property
● getMilesDriven(): a method that returns the value of the milesDriven property
● getBrand(): a method that returns the value of the brand property
● getModel(): a method that returns the value of the model property
● getYear(): a method that returns the value of the year property


● getAge(): a method that returns the age of the car (i.e. the difference between the
current year and the year property)
★ The class should also have a static property called numberOfCars that keeps track
of the number of Car objects that have been created. This property should be
incremented every time a Car object is created.
In the main() function, create three Car objects with different brands, models, and years.
Drive each car a different number of miles using the drive() method.
Print out the brand, model, year, and miles driven for each car using the
getBrand(), getModel(), getYear(), and getMilesDriven() methods, respectively.
Also print out the age of each car using the getAge() method.
Finally, print out the total number of Car objects created using the numberOfCars static
propert

```

```
class Car {
  String brand;
  String model;
  int year;
  double milesDriven = 0;
  static int numberOfCars = 0;

  Car(this.brand, this.model, this.year) {
    numberOfCars++;
  }

  void drive(double miles) {
    milesDriven += miles;
  }

  double getMilesDriven() {
    return milesDriven;
  }

  String getBrand() {
    return brand;
  }

  String getModel() {
    return model;
  }

  int getYear() {
    return year;
  }

  int getAge() {
    return DateTime.now().year - year;
  }
}
void main() {
  Car car1 = Car('Toyota', 'Camry', 2010);
  Car car2 = Car('Honda', 'Accord', 2015);
  Car car3 = Car('Ford', 'Mustang', 2020);

  car1.drive(10000);
  car2.drive(20000);
  car3.drive(5000);

  print('Car 1:');
  print('Brand: ${car1.getBrand()}');
  print('Model: ${car1.getModel()}');
  print('Year: ${car1.getYear()}');
  print('Miles driven: ${car1.getMilesDriven()}');
  print('Age: ${car1.getAge()}');

  print('Car 2:');
  print('Brand: ${car2.getBrand()}');
  print('Model: ${car2.getModel()}');
  print('Year: ${car2.getYear()}');
  print('Miles driven: ${car2.getMilesDriven()}');
  print('Age: ${car2.getAge()}');

  print('Car 3:');
  print('Brand: ${car3.getBrand()}');
  print('Model: ${car3.getModel()}');
  print('Year: ${car3.getYear()}');
  print('Miles driven: ${car3.getMilesDriven()}');
  print('Age: ${car3.getAge()}');

  print('Total number of cars created: ${Car.numberOfCars}');
}

```
