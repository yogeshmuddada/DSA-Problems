
````
int largest=1;
int slargest=Integer.MIN_VALUE;
		for(int i=0;i<n;i++)
			{
				if(a[i]>largest)
				largest=a[i];
			}
		for(int i=0;i<n;i++)
			{
				if(a[i]>slargest && a[i]<largest)
				slargest=a[i];
			}
		System.out.println(slargest);
````

### Optimised solution:

````
 int a[]={1,7,5,2,7,3};
        
        int large=a[0];
        int slarge=a[0];
        for(int i=1;i<a.length;i++){
            if(a[i]>large){
            slarge=large;
            large=a[i];
            }
            else if(a[i]>slarge && a[i]<large){
                slarge=a[i];
            }
        }
        System.out.println(slarge);
````

>if a student got the higest marks then he will be the first of that class. if a student got a few more marks then higest person then he will become the first and previous student become the second.
