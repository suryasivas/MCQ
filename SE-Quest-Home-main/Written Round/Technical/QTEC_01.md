# TEC_01

#### [01] Write a program to give the following output for the given input
####      Eg 1: Input: a1b10
              Output: abbbbbbbbbb
####      Eg: 2: Input: b3c6d15
              Output: bbbccccccddddddddddddddd


```c

#include <stdio.h>

int main() {
    char str[50];
    char alpha = 0;
    int num = 0,i,j;
    printf("Enter a String: ");
    scanf("%s",str);
    for (i=0; str[i]; i++){
        
        if ((str[i] >= 'A' && str[i] <= 'Z')||(str[i] >= 'a' && str[i] <= 'z')){
            if (alpha != 0){
                //Final output
                for (j=0; j<num; j++){
                    printf("%c",alpha);
                }
            num = 0;
            }
            alpha = str[i];
        }
        
        else if (str[i] >= '0' && str[i] <= '9'){
            num = num*10+str[i]-48;
        }
        
        
    }
    //Last character will not be printed if you didn't give the below statement
    for (j=0; j<num; j++){
            printf("%c",alpha);
    }
    
    return 0;
}

```

[To Experiment with Code Click Here It Will Bring You To A Free Online Compiler](https://www.onlinegdb.com/online_c_compiler)

#### [02] Input: ZOHOquest
####      Output:
          Z       Z
           O     O 
            H   H  
             O O   
              q    
             u u   
            e   e  
           s     s 
          t       t

## This is the famous question asked in ZOHO interviews!!! 
```c

#include <stdio.h>
#include <string.h>

char str[50];
int len;

void PrintCrossPattern(){
    //Understand the below code on this function to print your own cross string
    int i,j;
    
    for(i=0; str[i]; i++){
        for(j=0; str[j]; j++){
            if(i==j){
                printf("%c",str[i]);
            }
            else if(i+j==len){
                printf("%c",str[i]);
            }
            else{
                printf(" ");
            }
        }
    printf("\n");
    }
}


int main()
{
    while("TRUE"){
        
        printf("Enter a String: ");
        scanf("%s",str);
        len = strlen(str) - 1;
        
        if(len%2 == 0){
            PrintCrossPattern();
            break;
        }
        else{
            printf("Please enter a Odd length string\n");
        }
    }
    
    return 0;
    
}

```

[To Experiment with Code Click Here It Will Bring You To A Free Online Compiler](https://www.onlinegdb.com/online_c_compiler)

#### [03] Find output for the given program 

```c

#include <stdio.h>
int main() {
   int year;
   printf("Enter a year: ");
   scanf("%d", &year);

   // leap year if perfectly dvisible by 400
   if (year % 400 = 0) {
      printf("%d is a leap year.", year);
   }

   else {
      printf("%d is not a leap year.", year);
   }

   return 0;
}

```



## ANS: main.c:8:19: error: lvalue required as left operand of assignment
    if (year % 400 = 0) {
                   ^

### Explanation :
  While checking for equality **double equal to (==)** need to be used. 
  
  Correct code :
    
    main.c:8:19: if (year % 400 == 0)

[To Experiment with Code Click Here It Will Bring You To A Free Online Compiler](https://www.onlinegdb.com/online_c_compiler)


