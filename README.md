# Very_Cool_Number
import java.util.*;
class Test
{
	public static int very_cool(int n,int k)  // funtion definition
{
    //long long int a[1000000],
	long arr[]=new long[1000000];
	int i=0,j;
    int sum=0;
    while(n>0)
    {
        arr[i]=n%2;
        n=n/2;
        i++;
    }  
    for( j=i-1;j>=2;j--)
    {
        if(arr[j]==1&&arr[j-1]==0&&arr[j-2]==1)
            sum++;
    }
    if(sum>=k)
        return 1;
    else
        return 0;
}

public static void main(String[] args)
{
    Scanner sc= new Scanner(System.in);
    int r,k,s,total_no=0;
    //scanf("%d",&t);
    //scanf("%d%d",&r,&k);
	r= sc.nextInt();
	k= sc.nextInt();
    for(int i=0;i<1;i++)
    {
        //scanf("%d%d",&r,&k);
        for(int j=5;j<=r;j++)
        {
            s=very_cool(j,k);  // function calling
            total_no=total_no+s;
        }
        //printf("%d\n",total_no);
		System.out.println(total_no);
        total_no=0;
    }
    //printf("%d\n",total_no);
        
}

}
