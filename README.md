# student-j
import  java.util.Scanner;
class student
{
String name;
int rno;

void read()
{
Scanner inp=new Scanner(System.in);
System.out.println("enter name:");
name=inp.nextLine();
System.out.println("enter rno:");
rno=inp.nextInt();
}
}

class test extends student
{
int j;
int s[]=new int[6];
void marks()
{
Scanner inp=new Scanner(System.in);
System.out.println("enter marks:");
for(j=0;j<6;j++)
{
s[j]=inp.nextInt();
}
}
}
class result extends test
{
int i;
int sum=0;
void total()
{
for(int i:s)
{
sum=sum+i;
}
System.out.println("total marks obtained by the student"+name+"is"+sum);
}
}
class studentDemo4
{
public static void main(String[] args)
{
int m,i;
Scanner inp=new Scanner(System.in);
System.out.println("enter no.of students:");
m=inp.nextInt();
result r[]=new result[m];
for(i=0;i<m;i++)
{
r[i]=new result();
System.out.println("enter details of student:"+(i+1));
r[i].read();
r[i].marks();
r[i].total();
}
}
}










