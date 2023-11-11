# **Calculate how many increasing, decreasing segment in a vector/array:**


	
	difference=v[1]-v[0], count=0

		then we will iterate the loop and do the following operations:

			1. if difference<0 && v[i]-v[i-1]>0 is true
			we will increase the count variable

			2. again if difference>0 && v[i]-v[i-1]<0 is true
			we will also increase the count variable

			3. in every iteration we will update difference by v[i]-v[i-1]

	then total segment will be count+1

		1 2 3 4 5    4 3 2 1    2 3 4 5 --> 3 segments
	
