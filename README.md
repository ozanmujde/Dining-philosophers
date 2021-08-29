# Dining philosophers
## Usage
To compile  
```sh
$ gcc -Wall -o "hw2" "hw2.c" -lpthread 
```
And to run the file 
```sh
$ ./hw2 5
$ ./hw2 <Grup number>
```
## Description
Our code run multiple times for each group you can enter group number as args. If group number < 2 and > 1000 it'll automatically assigned to 5

Each philosopher has to eat pilaf. Until this happen pilaf will refill and money will be charged. If you want to test is pilaf refilled or not you can set gram to 500. Person and gram of pilaf can be changed.

Each philosopher have thread priority between 0 and 5
```sh
pthread_attr_getschedparam (&attr, &param);
	param.sched_priority = (rand() % 5 ); 
	printf("Thread %d has priority %d\n",i,param.sched_priority);
	pthread_attr_setschedparam (&attr, &param);
				
	pthread_create(&thread_id[i], &attr,
		philospher, &phil[i]);
```
