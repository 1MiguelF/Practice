Arrays of Objects Worksheet 						Name: Miguel


1. Complete the following program that is meant to create an array of 10 "movers." A mover is constructed to start at
the left side of the screen with a random height. It moves from left to right across the screen.

Mover [] dots;
void setup() {
  size(1000, 1000);
  background(0);
  dots = new Mover[10];
  for (int i = 0; i < dots.length; i++)
  {
    dots[i] = new Mover();
  }
}
void draw() {
  background(0);
  for (int i = 0; i < dots.length; i++)
  {
    dots[i].move();
    dots[i].show();
  }
}
class Mover {
  int x, y;
  Mover() {
    x = 0;
    y = (int)(Math.random()*1000);
  }
  void move() {
    x++;
  }
  void show() {
    fill(255);
    ellipse(x, y, 20, 20);
  }
}






2. A beginning programmer made a mistake with a very similar mover program. The program crashed as soon as the
program was run. What did the error message say? How would it be fixed?
Mover [] dots;
void setup(){
size(300,300);
background(0);
dots = new Mover[100];
}
void draw(){
for(int i = 0; i < dots.length;i++){
dots[i].move();
dots[i].show();
}
}
class Mover{ /* code not shown */}



There would be an error because there isn’t a for loop in void setup
