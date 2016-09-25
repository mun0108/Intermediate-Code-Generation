# Intermediate-Code-Generation
[root@golum Intermediate Code Generation]# flex m.l
[root@golum Intermediate Code Generation]# yacc -d m.y
[root@golum Intermediate Code Generation]# gcc lex.yy.c y.tab.c  -lm
[root@golum Intermediate Code Generation]# ./a.out

Enter the Expression: a=((b+c)*(d/e));


	 THREE ADDRESS CODE

B : = 	b	+	c	
C : = 	d	/	e	
D : = 	B	*	C	
E : = 	a	=	D	


	 QUADRAPLE CODE

0	+	b	c	B
1	/	d	e	C
2	*	B	C	D
3	=	a	D	E


	 TRIPLE CODE

0	+	b	c
1	/	d	0
2	*	B	1
3	=	a	2
