# cuddly-pancake
first project

// Find the acute angle formed by the two hands of a clock

#include <stdio.h>
#include <stdlib.h>
#include <math.h>

int hourHand = 0;
int minuteHand = 0;
int bigger = 0;
int smaller = 0;
int angle = 0;

// Each minute is 6 degrees

printf("Enter at which minute the hour hand is pointing to:\n");
scanf("%d", &hourHand);
printf("Enter at which minute the minute hand it pointing to:\n");
scanf("%d", &minuteHand);

if (hourHand > minuteHand) {
  bigger = hourHand;
  smaller = minuteHand;
}
else if (minuteHand > hourHand) {
  bigger = minuteHand;
  smaller = hourHand;
}
else if (minuteHand == hourHand) {
  printf("The acute angle formed by the two hands is 0 degrees.");
  return 0;
}

if ((bigger - smaller) <= 30) {
  angle = 6 * (bigger - smaller);
  printf("The acute angle formed by the two hands is %d degrees.", angle);
}

else {
  angle = 6 * (60 - (bigger - smaller));
  printf("The acute angle formed by the two hands is %d degrees.", angle);
}

return 0;

