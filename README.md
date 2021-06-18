#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main()
{
/* Conditions */
    char vipList[] = "AHMED";
    int minAge = 18;
    int maxAge = 30;
    int minHeight = 170;
    int maxHeight = 190;
    int password = 3579;
    int tries = 0;
 /* User's informations */
    int userAge;
    int userHeight;
    char userName[20];
    int code;
/* user's input */
    printf("What's your name Sir?\n");
    scanf("%s",userName);
/* fonctions */
    if(strcmp(userName,vipList) == 0 )
        {
            printf("Welcome Mr. %s\n",userName);
        }
        else
        {
            printf("how old are you Sir?\n");
            scanf("%d",&userAge);
            /* Age condition */
            if(userAge >= minAge && userAge <= maxAge)
            {
                printf("what's you height Sir?\n");
                scanf("%d",&userHeight);
                /* Height condition */
                if(userHeight >= minHeight && userHeight < maxHeight)
                {
                    while (tries < 3)
                    {
                        /* Password condition */
                        printf("Enter the invite code please\n");
                        scanf("%d",&code);
                        if(code == password)
                        {
                            printf("Welcome Sir you are allowed to enter\n");
                            break;
                        }
                        else
                        {
                            printf("Failed\n");
                            tries++;
                        }
                    }
                }
                else if (userHeight < minHeight)
                {
                    printf("Sorry you are too short Sir\n");
                }
                else
                {
                    printf("Sorry you are so tall Sir\n");
                }
            }
            else if( userAge > maxAge)
            {
                printf("You are too old Sir\n");
            }
            else
            {
                printf("you are too young Sir\n");
            }
        }
    return 0;
 }
