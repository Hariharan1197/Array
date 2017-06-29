import java.util.*;
public class Hello {
public static int[] swap(int[] arr)
{
    int minIndex=0;
    int maxIndex=0;
    for(int i=1;i<arr.length;++i)
    {
        if(arr[i]<arr[minIndex])
        {
            minIndex=i;
        }
        if(arr[i]>arr[maxIndex])
        {
            maxIndex=i;
        }
    }
    int t;
    if(maxIndex!=minIndex)
    {
        t=arr[minIndex];
        arr[minIndex]=arr[maxIndex];
        arr[maxIndex]=t;
    }
    return arr;
}
    public static void main(String[] args) {
		//Your Code Here
		Scanner in=new Scanner(System.in);
		int n=in.nextInt();
		int []a=new int[n];
		int j;
		for(j=0;j<n;j++)
		{
		    a[j]=in.nextInt();
		}
		for(int i:swap(a))
		{
		    System.out.println(i);
		}

	}
}
