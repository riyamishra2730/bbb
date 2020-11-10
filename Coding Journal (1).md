## My Exhilarating Journey Of Coding :

#### Friday, 3rd july . Day 1 :

​	Day 1 was my trial class from 04:00 pm - 05:00 pm with an exceedingly wonderful  teacher Riya Mishra maa'm from Whitehat Jr. I learnt the importance of coding and got super excited about the same from her motivating words. I got so excited that 2 hours after the class I was still trying to figure out how to code on P5.js Web Editor  (and believe it or not, she had not even taught me how to code!). My ma'am motivated me to work hard and earn a trip to Silicon Valley by showing me videos on amazing kids who had created awesome apps. So basically in in the trial class, this is what I did: - 

````javascript
  createCanvas(400, 400);
}

function draw() {
 
  background("white");
  
  rect(390, mouseY, 10, 70);
  
  rect(0, 150, 10, 70 );
  
  rect(200,200,10,10);
}
````

I created a ball, computer paddle and player paddle and made them move. So, that was how wonderful my day 1 was, that's enough information for you to hold today :) Bye... 

#### Saturday, 10 july . Day 2 :

​	Day 2 I had my class from 01:00 pm - 02:00 pm on object oriented programing in which I learnt how to create a ball and a player paddle an made them move with the mouse. Here is what i did in class :

````javascript
class Paddle {
  
  constructor(){
    this.width = 10;
    this.height = 70;
    this.xPosition = 0;
    this.yPosition= 0;
  }
  
  
  display(){
    rect(this.xPosition, this.yPosition, this.width, this.height);
  };
}

function setup(){
  createCanvas(400,400);
}

function draw() {
  //set background to white
  background("white");
  
  //player Paddle
  var playerPaddle = new Paddle();
  playerPaddle.xPosition = 390;
  playerPaddle.yPosition = mouseY;
  
  playerPaddle.display();
  
  //draw the ball
  rect(200,200,10,10);
}
````

Then I got a project in which the story was : You, as a Mayor of the city, need to create sufficient housing, so that there are no homeless people in your city. You have a fixed amount of space to create housing and buildings for every family in the city. There are 360 families who live in the city. Each Floor can house 2 families, in two adjacent apartments. Hence, a building of 12 floors will house 24 families. You have space to create only 10 buildings. Your task is to create an arrangement of buildings in the city. You can control how high a building can be, by assigning the floors to a building. and here is what I made: -

````javascript
var b1, b2, b3, b4, b5, b6, b7, b8;

function setup() {
  createCanvas(400, 400);
  b1=new Building();
  b1.position=1;
  b1.floors=36;
  
  b2=new Building();
  b2.position=2;
  b2.floors=27;
  
  b3=new Building();
  b3.position=3;
  b3.floors=9;
  
  b4=new Building();
  b4.position=4;
  b4.floors=18;
  
  b5=new Building();
  b5.position=5;
  b5.floors=27;
  
  b6=new Building();
  b6.position=6;
  b6.floors=9;
  
  b7=new Building();
  b7.position=7;
  b7.floors=36;
  
  b8=new Building();
  b8.position=8;
  b8.floors=18;
  
}

function draw() {
  background("lightblue");
  fill("yellow");
  //sun
  circle(200,60,70);
  fill("violet");
  b1.display();
  fill("indigo");
  b2.display();
  fill("blue");
  b3.display();
  fill("green");
  b4.display();
  fill("orange");
  b5.display();
  fill("pink");
  b6.display();
  fill("red");
  b7.display();
  fill("black");
  b8.display();
  
}
````

As an extra challenge to myself, I figured out how to fill in colour in the buildings and created a circle (sun)...

That is enough information for you to hold today... Bye :)

#### Saturday, 11 july . Day 3 : 

​	Day 3, my class was from 10:00 am - 11:00 am in which i learnt about Sprite Objects in which I use Sprite Class to create an animated ball in a playground project where I experimented with different sprite properties and functions, and in class I created this :

````javascript
var ball = createSprite(200,200,10,10);

ball.velocityX = -2;
ball.velocityY = -3;

function draw() {
  
  background("white");
  
  
  createEdgeSprites();
  
  ball.bounceOff(edges);
  
  drawSprites();
}

````

​	This was my first step towards the Ping Pong Game... afterwards I got the project in which one of the factions on Planet Herosa, the **Squarian people**, really liked my work. Lord Squarier, the faction leader, had entrusted me to create a game for the Squarian people.

The instructions were:

- Have a square game board or table.

- There should be square pieces which can be moved around

- The primary piece in the game should be white.

- All other pieces should be dark gray

  

So, here is what I created :

```` javascript
var squaride = createSprite(206, 128, 25, 25);
var pin1 = createSprite(200, 300, 20, 20);
var pin2 = createSprite(180, 320, 20, 20);
var pin3 = createSprite(220, 320, 20, 20);
var pin4 = createSprite(160, 340, 20, 20);
var pin5 = createSprite(200, 340, 20, 20);
var pin6 = createSprite(240, 340, 20, 20);
squaride.velocityX = 4;
squaride.velocityY = 0.5;

squaride.shapeColor="white";
pin1.shapeColor="darkgrey";
pin2.shapeColor="darkgrey";
pin3.shapeColor="darkgrey";
pin4.shapeColor="darkgrey";
pin5.shapeColor="darkgrey";
pin6.shapeColor="darkgrey";
function draw() {
background("yellow");
createEdgeSprites();
squaride.bounceOff(edges);
pin1.bounceOff(edges);
pin2.bounceOff(edges);
pin3.bounceOff(edges);
pin4.bounceOff(edges);
pin5.bounceOff(edges);
pin6.bounceOff(edges);
squaride.bounce(pin1);
squaride.bounce(pin2);
squaride.bounce(pin3);
squaride.bounce(pin4);
squaride.bounce(pin5);
squaride.bounce(pin6);
pin1.bounce(pin2);
pin1.bounce(pin3);
pin1.bounce(pin4);
pin1.bounce(pin5);
pin1.bounce(pin6);
pin2.bounce(pin3);
pin2.bounce(pin4);
pin2.bounce(pin5);
pin2.bounce(pin6);
pin3.bounce(pin4);
pin3.bounce(pin5);
pin3.bounce(pin6);
pin4.bounce(pin5);
pin4.bounce(pin6);
pin5.bounce(pin6);
drawSprites();
}
````

That's a huge programme. Right ? So, that was how wonderful my day 3 was, that's enough information for you to hold today :) Bye... 

#### Saturday, 18 july . Day 4 :

​	Day 4 , my class was from 10:00 am - 11:00 am on Conditional Programming in which I used conditional programming to add control to the ball's movements. I built a little game using the ball's movements and added some challenge to it using the "if" statement. so, here is what I did: -

````javascript
var ball = createSprite(200,200,10,10);

ball.velocityY = 2;
ball.velocityX = 3;

function draw() {
  background("white");
  createEdgeSprites();
  ball.bounceOff(edges);
  
  if(keyDown(UP_ARROW)) {
    ball.velocityX = 0;
    ball.velocityY = -2;
  }
  
  drawSprites();
}
````

After that, I even learnt how to make the ball reset to its original position if it touches another object using "sprite.isTouching" statement from the sprite tool box. I made kind of a "miniature" maze in class, something like this: -

````javascript
var ball = createSprite(200,200,10,10);
ball.shapeColor="blue";

ball.velocityY = 2;
ball.velocityX = 3;

var wall1= createSprite(10,50,20,100);
wall1.shapeColor="yellow";
var wall2= createSprite(50,50,20,200);
wall2.shapeColor="blue";
var wall3= createSprite(80,130,20,400);
wall3.shapeColor="red";

function draw() {
  background("white");
  createEdgeSprites();
  ball.bounceOff(edges);
  
  if(keyDown(UP_ARROW)) {
    ball.velocityX = 0;
    ball.velocityY = -2;
  }
 if (keyDown(DOWN_ARROW)) {
   ball.velocityX = 0;
   ball.velocityY = 2;
 }
 if (keyDown(RIGHT_ARROW)) {
   ball.velocityX = 2;
   ball.velocityY = 0;
 }
 if (keyDown(LEFT_ARROW)) {
   ball.velocityX = -2;
   ball.velocityY = 0;
   
 }
 if (ball.isTouching(wall1)||ball.isTouching(wall2)||ball.isTouching(wall3)) {
  ball.x=200;
  ball.y=200;
 }

 drawSprites();
}

````

Then as a Project I had to help Sophia who loves to play maze games, where her mother helps her create actual mazes using cardboard pieces at home. Sophia has just embarked on a coding learning journey and she is eager to try her hand at creating a virtual game of maze. So, I helped Sophia build a such a game with a path that leads to a golden cup...

````javascript
var sofia= createSprite(30,40,20,20);
var cup = createSprite(350, 350,50,50);
var cardboard1=createSprite(75,0,10,300);
var cardboard2=createSprite(100,200,200,10);
var cardboard3=createSprite(350,120,10,150);
var cardboard4=createSprite(308,270,160,10);
var cardboard5=createSprite(350,50,80,10);
var cardboard6=createSprite(170,20,10,150);
var cardboard7=createSprite(168,100,80,10);
var cardboard8=createSprite(260,170,10,200);
var cardboard9=createSprite(62,286,10,150);
var cardboard10=createSprite(130,360,140,10);
var cardboard11=createSprite(202,348,10,75);
var cardboard12=createSprite(134,310,10,100);
var cardboard13=createSprite(140,150,120,10);
var cardboard14=createSprite(135,255,50,10);
var cardboard15=createSprite(205,30,80,10);
var cardboard16=createSprite(344,200,80,10);
var cardboard17=createSprite(114,0,10,120);
var cardboard18=createSprite(18,150,10,100);
var cardboard19=createSprite(388,272,10,70);
var cardboard20=createSprite(242,378,90,10);
var cardboard21=createSprite(284,360,10,40);
var cardboard22=createSprite(270,338,60,10);
sofia.shapeColor="yellow";
cup.shapeColor="yellow";
cardboard1.shapeColor="orange";
cardboard2.shapeColor="orange";
cardboard3.shapeColor="orange";
cardboard4.shapeColor="orange";
cardboard5.shapeColor="orange";
cardboard6.shapeColor="orange";
cardboard7.shapeColor="orange";
cardboard8.shapeColor="orange";
cardboard9.shapeColor="orange";
cardboard10.shapeColor="orange";
cardboard11.shapeColor="orange";
cardboard12.shapeColor="orange";
cardboard13.shapeColor="orange";
cardboard14.shapeColor="orange";
cardboard15.shapeColor="orange";
cardboard16.shapeColor="orange";
cardboard17.shapeColor="orange";
cardboard18.shapeColor="orange";
cardboard19.shapeColor="orange";
cardboard20.shapeColor="orange";
cardboard21.shapeColor="orange";
cardboard22.shapeColor="orange";
sofia.velocityX=0;
sofia.velocityY=0;
function draw() {
background("violet");
textSize(20);
text("SOFIA", 5, 80);
textSize(20);
text("GOLDEN CUP", 240,306);
if (sofia.isTouching(cup)) {
textFont("georgia");
textSize(50);
text("YOU WIN", 100, 200);}
if (keyWentUp("up")) {
 sofia.velocityX=0;
 sofia.velocityY=0;}
if (keyWentUp("down")) {
 sofia.velocityX=0;
 sofia.velocityY=0;}
if (keyWentUp("right")) {
 sofia.velocityX=0;
 sofia.velocityY=0;}
if (keyWentUp("left")) {
 sofia.velocityX=0;
 sofia.velocityY=0;}
if (keyDown("UP_ARROW")) {
  sofia.velocityX=0;
  sofia.velocityY=-2;}
if (keyDown("DOWN_ARROW")) {
  sofia.velocityX=0;
  sofia.velocityY=2;}
if (keyDown("RIGHT_ARROW")) {
 sofia.velocityX=2;
 sofia.velocityY=0;}
if (keyDown("LEFT_ARROW")) {
 sofia.velocityX=-2;
 sofia.velocitY=0;}
 if (sofia.isTouching(cup)) {
sofia.shapeColor="violet";
cup.shapeColor="violet";}
{if (sofia.isTouching(cardboard1)||sofia.isTouching(cardboard2)||sofia.isTouching(cardboard3)||sofia.isTouching(cardboard4)||sofia.isTouching(cardboard5)||sofia.isTouching(cardboard6)||sofia.isTouching(cardboard7)||sofia.isTouching(cardboard8)||sofia.isTouching(cardboard9)||sofia.isTouching(cardboard10)||sofia.isTouching(cardboard11)||sofia.isTouching(cardboard12)||sofia.isTouching(cardboard13)||sofia.isTouching(cardboard14)||sofia.isTouching(cardboard15)||sofia.isTouching(cardboard16)||sofia.isTouching(cardboard17)||sofia.isTouching(cardboard18)||sofia.isTouching(cardboard19)||sofia.isTouching(cardboard20)||sofia.isTouching(cardboard21)||sofia.isTouching(cardboard22)) {
sofia.x=30;
sofia.y=40;}
createEdgeSprites();
sofia.bounceOff(edges);
drawSprites();}
}
````

... and as a feedback my teacher said, "well done! Keep up the good work!".  So, that was how wonderful my day 4 was, that's enough information for you to hold today :) Bye... 

#### 



