- 👋 Hi, I’m @Dixit8287
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me .
#include<stdio.h>
#include<stdlib.h>
#include<time.h>


int main(void)
{
    int number, guess, count = 1;
    char diff;

    srand(time(NULL));
    
    printf("Select the difficulty level from the following option :- \n a) Easy\n b) Moderate \n c) Hard \n");
    scanf("%s", &diff);
    
    switch(diff)
    {
        case 'a':
        number = rand()%10;
        break;

        case 'b':
        number = rand()%100;
        break;

        case 'c':
        number = rand()%1000;
        break;

        
    }

    
    printf("Guess the number :) ");
    
    for(int i = 0; ; i++)
    {   
        scanf("%d", &guess);

        if(guess > number)
        {
            printf("Lower number please :) ");
            count++;
        }
        else if(guess < number)
        {
            printf("Higher number please :) ");
            count++;
        }
        else if(guess == number)
        {
            printf("Congratulations you have guessed the number ");
            break;
        }
    }
        printf("and it took you %d guesses to guess the number.\n", count);

        return 0;
