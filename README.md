# codejam
#include<iostream>

using namespace std;
//to check the content of the string
int f=0;
int check(int arr[])
{ int flag=0;
    for(int i=0;i<10;i++)
    {  //cout<<arr[i]<<endl;

        if(arr[i]==0)
        flag++;

    }
    return flag;

}

int main()
{
    int num,newnum;
    int token;
    int a[10]={0};
    int i=1,j=0;
    cout<<"enter the number";
    cin>>num;
//to get the new numbers every time.
    while(i<=10)
    {
        newnum=num*i;
        int last=newnum;
//to access every digit of the number and assign it to the array.
        while(newnum!=0)
    {
        int val=newnum%10;
        newnum=newnum/10;
        switch(val)
        {
            case 0:{ ++a[0];
                    break;
                    }
            case 1: {++a[1];
                     break;}
            case 2: {++a[2];

                    break;}

            case 3: {++a[3];
                    break;}

            case 4: {++a[4];
                    break;}

            case 5: {++a[5];
                    break;}
            case 6: {++a[6];
                     break;
                    }
            case 7: {++a[7];
                    break;
                     }
            case 8: {++a[8];
                    break;
                    }
            case 9:{ ++a[9];
                    break;
                    }


        }
        /* for (i=0;i<10;i++)
         {
             cout<<a[i]<<endl;

         }
        */

    }

      token=check(a);

           if(token==0)

             {
                cout<<":"<<last;

                     f++;

                     break;

             }

           else
           {
            ++i;
           }




}

if(f==0)
{
    cout<<"Insomnia";
}
return 0;

}
