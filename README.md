## Hi there 👋 
Currently doing nothing.

#include<stdio.h>

int main(){
	int k,i,j,a,b=0,u;
	scanf("%d",&i);
	u=i;
	for(j=0;j<u;j++,i--,b++){
			
		for(a=0;a<b;a++)
			printf(" ");
			
		for(k=0;k<i;k++)
			printf("*");
			
		printf("\n");	
	}
}


















#include<stdio.h>

int main(){
	int i,j,k,a,b,c;
	scanf("%d",&i);
	a=i;
	b=i-1;
	c=i/2;
	for(;a>0;a--){
		k=b;
		j=c;
		for(;b>0;b--){
			printf(" ");
		}
		b=k-1;
		for(;c>0;c--){
			printf("*");
		}
		c=i/2;
		printf("\n");
	}
}

#include<stdio.h>

int main (){
int a , b , m , n ;
	scanf ("%d %d" , &m , &n );
for ( b=1 ; b<=n ; b++){
	for(a=1 ; a<=m ; a++){
         printf("%d     " , a*b);	
}
	printf("\n");
} 

}
		
		
		
	














#include<stdio.h>

int main(){
	int i,j,a,b;
	
	scanf("%d",&a);
	
	for(i=1;i<=a;i++){
		if(i==1 || i==a){
			for(b=0;b<a;b++)
			printf("*");
			printf("\n");
			
		}else{
			for(j=1;j<=a;j++){
				if(j==1 || j==a){
					printf("*");
				}
				printf(" ");
			}
			printf("\n");
		}
	}
}






#include<stdio.h>

int main(){
	int k,i,j,a,b=0,u;
	scanf("%d",&i);
	u=i;
	for(j=0;j<u;j++,i--,b++){
			
		for(a=0;a<b;a++)
			printf(" ");
			
		for(k=0;k<i;k++)
			printf("*");
			
		printf("\n");	
	}
}

















#include<stdio.h>

int main(){
	int c=1,b=0,a,j=0.,i,k=1,n,r,t;
	scanf("%d",&r);
	scanf("%d",&n);
	
	for(a=0;a<r;a++,b++){
		c=c*(n-b);
	}
	
	for(i=0;i<r;i++,j++){
		k=k*(r-j);
	}
	
	printf("%d",c/k);
}







#include <stdio.h>

int main() {

    int n, i, r = 0;
    scanf("%d", &n);

    if (n == 0 || n == 1)
        r = 1;

    for (i = 2; i <= n / 2; ++i) {

        if (n % i == 0) {
            r = 1;
            break;
        }
    }


    if (r == 0)
        printf("prime");
    else
        printf("composite");

}









#include <stdio.h>

int main() {
    int i, j = 0, l = 1, k;

    scanf("%d", &i);

    while (i != 0) {
        k = i % 2;
        i = i/ 2;
        j = j + (k * l);
        l = l * 10;
    }

    printf("%d", j);

    return 0;
}






#include <stdio.h>

int main() {
    int n, c = 0, num = 2 , b,i;

    scanf("%d", &n);

    while (c < n) {
        b = 1;
        for (i = 2; i <= num / 2; i++) {
            if (num % i == 0) {
                b = 0;
                break;
            }
        }
        if (b) {
            c++;
            if (c == n) {
                printf("%d",num);
                break;
            }
        }
        num++;
    }
}






#include<stdio.h>

int f(int i){
	if(i==1 || i==2){
		return 1;
	}
	
	
	int a[i],c;
	return(f(i-2)+f(i-1));
	

}

int main(){
int a,i,c;
scanf("%d",&a);
for(i=1;i<=a;i++){
	printf("%d ",f(i));
}

}


#include <stdio.h>

int main() { 
    int n,i,j,b;
    scanf("%d", &n);
    int a[n];
    for (i = 0; i < n; i++) {
         scanf("%d", &a[i]);
    } 
    for (i = 0; i < n; i++) {
        for (j = i+1; j < n; j++) {
            if (a[i] < a[j]) {
                b = a[i];
                a[i] = a[j];
                a[j] = b;
            }
        }
    }
    for (i = 0; i < n; i++) {
        if(i==n-1){
        	printf("%d", a[i]);	
		}else{
			printf("%d-", a[i]);
		}
    }
}




#include<stdio.h>

int main(){
	
	int i, j, z, c = 0, t = 1,u = 0;
	char a[101];
	gets(a);

	for (i = 0; a[i] != NULL; i++) {
		if (a[i] == '!') {
			u = u - 33;
		}
		else if (a[i] == '.') {
			u = u - 46;
		}
		for (j = i + 1; a[j] != NULL; j++) {
			if (a[i] == a[j]) {
				t = 0;
				break;
			}
		}
		if (t == 0) {
			t = 1;
		}
		else {
			c = c + a[i];
			t = 1;
		}
	}
	u = u+c;
	if (u == 2879) {
		printf("Yes");
	}
	else {
		printf("No");
	}
	
}

#include<stdio.h>
#include<string.h>

struct node {
	char a[50];
	struct node* link;

};

struct node* create(struct node* first, char a[20]) {
	struct node* temp = first;
	struct node* newnode;
	newnode = (struct node*)malloc(sizeof(struct node));
	newnode->link = NULL;
	if (first == NULL) {
		first = newnode;
		strcpy(newnode->a, a);
		return first;
	}
	else {
		for (; temp->link != NULL; temp = temp->link);
		temp->link = newnode;
		strcpy(newnode->a, a);
		return first;
	}
}

void change_word(struct node* first, char b[], char c[]) {
	struct node* temp = first;

	for (;temp->link != NULL; temp = temp->link) {
		if(strcmp(temp->a,b)==0){
			strcpy(temp->a,c);
		}else if(strcmp(temp->a,c)==0){
			strcpy(temp->a,b);
		}
	}
	
	
}

void show(struct node* first) {
	struct node* temp = first;
	for (; temp; temp = temp->link) {
		printf("%s ",temp->a);
	}
}
int main() {
	struct node* first = NULL;
	char a[50];
	char b[50];
	char c[50];

	gets(a);
	gets(b);
	gets(c);

	char* t;
	t = strtok(a, " ");

	for (; t != NULL;) {
		first = create(first, t);
		t = strtok(0, " ");
	}

	change_word(first, b, c);
	show(first);












}








#include<stdio.h>
#include<string.h>

struct node {
	char a[50];
	struct node* link;
};

struct node* create(struct node* first, char a[50]) {
	struct node* temp = first;
	struct node* newnode;
	newnode = (struct node*)malloc(sizeof(struct node));
	newnode->link = NULL;

	if (first == NULL) {
		first = newnode;
		strcpy(newnode->a, a);
		return first;

	}
	else {
		for (; temp->link != NULL; temp = temp->link);
		temp->link = newnode;
		strcpy(newnode->a, a);
		return first;
	}


}

void show(struct node* first) {
	struct node* temp = first;
	for (; temp; temp = temp->link) {
		puts(temp->a);
	}
}

int main() {
	struct node* first = NULL;
	char a[100];
	char b[50][50];
	char c[50];
	gets(a);

	char* t;
	t = strtok(a, " ");

	int i;
	int j;
	int k = 0;
	int h;

	while (t != NULL) {
		first = create(first, t);
		t = strtok(0, " ");
	}

	struct node* temp = first;

	for (; temp; temp = temp->link) {
		strcpy(c, temp->a);
		j = strlen(c) - 1;
		if (strlen(c) == 1) {
			strcpy(b[k], c);
			k++;
		}
		else {

			for (i = 0; i < strlen(c) / 2; i++, j--) {
				if (c[i] == c[j]) {
					if (i == (strlen(c) / 2) - 1) {
						strcpy(b[k], c);
						k++;
					}
				}
				else {
					break;
				}

			}
		}
	}
	char d[50];
	int m;
	
	for (h = 0; h < k - 1; h++) {
        for (m = 0; m < k - h - 1; m++) {
            if (strlen(b[m]) < strlen(b[m + 1])) {
                strcpy(d, b[m + 1]);
                strcpy(b[m + 1], b[m]);
                strcpy(b[m], d);
            }
        }
    }
	if (k == 0) {
		printf("No palindrome word found !!");
	}
	else {

		printf("%d\n", k);
		printf("%s", b);
	}
}














#include <stdio.h>

int strlen(char a[50]) {
    int i;
    for (i = 0; a[i]; i++);
    return i;
}

void f(char* a, const char* b, const char* c, int i) {
    int j = strlen(a);
    int k = strlen(b);
    int h = strlen(c);

    for (int i = 0; i <= j - k; ++i) {
        if (strncmp(a + i, b, k) == 0) {
            memmove(a + i + h, a + i + k, j - i - k + 1);
            memcpy(a + i, c, h);
            i += h - 1;
            i--;
            if (i == 0)
                break;
            j += h - k;
        }
    }
}

int main() {
    char a[201], b[201], c[201];
    int i;

    gets(a);
    gets(b);
    gets(c);
    scanf("%d", &i);

    f(a, b, c, i);

    puts(a);

}
















#include <stdio.h>
#include <time.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>

struct card{
	
	char num[17];
	int pol;
	char pass[5];
	char name[20];
};

char checkpass(char a[],char b[]){
	
	for(int i=0;i<4;i++){
		if(a[i]==b[i]){
			continue;
		}else{
		return 2;
		}
		
	}
	return 1;
}

char checknum(char a[],char b[]){
	
	for(int i=0;i<16;i++){
		if(a[i]==b[i]){
			continue;
		}else{
		return 2;
		}
		
	}
	return 1;
}





int main (){
	struct card c1;
	struct card c2;
	
	int t;
	char pass1[5];
	char num1[17];
	char num2[17];
	char name1[20];
	char name2[20];
	int pol1;
	int pol2;
	int polv;
	
	
		
	printf(" etelaat card aval ro vared konid :\n");
	printf(" num:\n");
	fflush(stdin);
		gets(num1);
		fflush(stdin);
	printf(" name:\n");
		gets(name1);
		fflush(stdin);
	printf(" pass:\n");
		gets(pass1);
		fflush(stdin);
	printf(" money:\n");
		scanf("%d",&pol1);
		fflush(stdin);
	
	printf(" etelaat card dovom ro vared konid :\n");
	printf(" num:\n");
		gets(num2);
		fflush(stdin);
	printf(" name:\n");
		gets(name2);
		fflush(stdin);
	printf(" money:\n");
		scanf("%d",&pol2);
		fflush(stdin);
	
	printf(" Khosh amadid be bank elm o farhang");
		sleep(2);
		system("cls");
		
	printf(" ramz khod ra vared konid :\n");
	for(;;){
		gets(c1.pass);
		if(checkpass(c1.pass,pass1)==1){
			break;
		}
		printf("Ramz ra eshtebah vared kardid ! \n");
		printf(" Lotfan ramz khod ra vared konid :");
	
	}
	
	printf("shomare card maghsad ra baraye enteghal pol vared konid :");
	
	for(;;){
		fflush(stdin);
		gets(c2.num);
		if(checknum(c2.num,num2)==1){
			break;
		}
		printf("shomare card na motabar ast ! \n");
		printf(" Lotfan dobare shomare card maghsad ra vared konid :");
	
	}
	printf("lotfan mablagh varizi ro vared konid :");
		for(;;){
			fflush(stdin);
			scanf("%d",&polv);
			if(polv<pol1){
				break;
			}else{
				printf(" mojodi kart shoma kam ast !! dobare talash konid :\n ");
			}
		}
		pol1=pol1-polv;
		pol2=pol2+polv;
		
		printf("amaliat ba movafaghiat anjam shod ! \n");
		printf("mojodi card aval :%d \n",pol1);
		printf("Name card aval :%s \n",name1);
		printf("mojodi card dovom :%d \n",pol2);
		printf("Name card dovom :%s \n",name2);
		
}













#include <stdio.h>
#include <string.h>

int p1(char ch) {
    return (ch >= 'a' && ch <= 'z');
}

char p2(char ch) {
    if (p1(ch)) {
        return ch - ('a' - 'A');
    }
    return ch;
}

int main() {
    char a[101];
    int c[26] = {0};
    gets(a);

	int i;
	
    for (i = 0; i < strlen(a); i++) {
        char ch = a[i];
        if (p1(ch)) {
            c[ch - 'a']++;
        }
    }

    for (i = 0; i < 26; i++) {
        if (c[i] > 0) {
            printf("%c: %d\n", i + 'a', c[i]);
        }
    }
	char ch;
    
	for (ch = 'a'; ch <= 'z'; ch++) {
        for (i = 0; i < strlen(a); i++) {
            if (a[i] == ch || a[i] == p2(ch)) {
                printf("%c",p2(ch));
            }
        }
    }
    printf("\n");

}













#include<stdio.h>
#include<stdlib.h>
#include<string.h>

struct bookinfo{
	int score;
	char fname[50];
	char lname[50];
	char id[50];
};

struct node{ 
	struct bookinfo book;
	struct node *link;
};


struct node *create(){
	
	struct node *temp;
	struct bookinfo book;
		printf("first name : \n");	
		fflush(stdin);
		gets(book.fname);
		fflush(stdin);
		
		printf("last name : \n");	
		gets(book.lname);
		fflush(stdin);
		
		printf("score : \n");
		scanf("%d",&book.score);
		fflush(stdin);
		
		fflush(stdin);
		printf("id : \n");
		gets(book.id);
		fflush(stdin);
	temp = (struct node*)malloc(sizeof(struct node));
	temp->book = book;
	temp->link = NULL;
		return temp;
}

struct node *addend(struct node *first , struct node *newnode){
	struct node * last;
	if(first == NULL){
		first = newnode;
		return first;
	}else{
		for(last=first ; last->link != NULL ; last = last->link);
		last->link = newnode;
		return first;
	}
}



void tartib1(struct node *first){
	struct node *temp=first;
	struct node *temp2=first;
	struct node *temp3=first;
	struct bookinfo booktemp;
	
	for(;temp->link != NULL;temp=temp->link){
		
		for(;temp2->link != NULL;temp2=temp2->link){
			
			if(strcmp(temp2->book.fname,temp2->link->book.fname)==1){
				booktemp = temp2->book;
				temp2->book=temp2->link->book;
				temp2->link->book = booktemp;
			
			}
		}
		temp2=temp3;
	}
	show(first);
}

void show(struct node *first){
	struct node *temp=first;
		for( ; temp ; temp = temp->link){
			printf("first name : %s \n", temp->book.fname);	
				printf("last name : %s \n", temp->book.lname);
				printf("score : %d \n", temp->book.score);
				printf("id : %d \n", temp->book.id);
			printf("-------------- \n");
		}
}

int main(){
	struct node *first = NULL ;
	int i,a,b,j,u,k,k1,k2;
	char tname[50],tname2[50],tname3[50];
	printf("tedad student :\n");
	scanf("%d",&i);
	for(j=1;j<=i;j++){
		printf("Enter detail of student #%d\n",j);
		first=addend(first,create());
	}
	tartib1(first);
			
		
	
}








































































































































<!--
**oneHalfA/oneHalfA** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
