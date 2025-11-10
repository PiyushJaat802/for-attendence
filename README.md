# #include <stdio.h>
// #include<stdlib.h>

int strLength(char *str)    {
    int x = 0;
    for(; *(str+x); x++);
    return x;
}

char* strCat(char *str1, char *str2)    {
    int ansSize = (strLength(str1) + strLength(str1) + 1);

    char ans = (char) calloc(ansSize, sizeof(char));
    int x;
    
    for( x = 0; str1[x]; x++)   
        ans[x] = str1[x];
    
    for(int z = 0; str2[z]; x++,z++)   
        ans[x] = str2[z];

    return ans;
}

char* strCopy(char *str1, char *str2)   {
    for(int x = 0; str2[x]; x++)
        str1[x] = str2[x];

    return str1;
}


int main()  {
char fname[20] = "Piyush";
    char lname[20] = "Jaat";
    printf("Length of FName :- %d\n",strLength(fname));
    printf("Length of LName :- %d\n",strLength(lname));
    char *fullName = strCat(fname,lname);
    printf("Full Name :- %s\n",fullName);
    printf("Length of full Name :- %d\n",strLength(fullName));

    strCopy(fname, "Mohammad");
    printf("F Name :- %s\n",fname);
    


    printf("\n");
    return 0;
}
