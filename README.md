# CSA1445---COMPILER-DESIGN
%{
#include <stdio.h>
%}

%%
"+"         { printf("PLUS operator\n"); }
"-"         { printf("MINUS operator\n"); }
"*"         { printf("MULTIPLY operator\n"); }
"/"         { printf("DIVIDE operator\n"); }
.           { printf("INVALID character\n"); }
%%

int main() {
    yylex();
    return 0;
}

int yywrap() {
    return 1;
}
