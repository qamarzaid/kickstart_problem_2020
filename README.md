### Google Kickstart Problem 2020
### Round-H
#### Problem 1: Retype
```
After spending many hours studying for programming competitions, you decided to take a rest 
and play video games. You are currently playing an adventure game called Quick Start.

This game has N levels, and you are currently on the K-th level. Unfortunately, you just 
realized that to beat the boss at the final level, you will need a special sword, which 
can be picked up at level S. You have already completed that level, but you forgot to 
pick up the sword at that level.

Now you want to pick up the sword and finish the game in the least amount of time possible,
and for that you have two options:

Restart the game and complete all levels again, starting from level 1.
Move to previous levels until you reach level S, pick up the sword and complete all the 
remaining levels, starting from level S.
Every time you enter a level you have to exit it, either by completing it and going to
the next level or
by moving to a previous level or by finishing / exiting the game. Exiting any level takes 1 minute. 
That means, for example, that it took you L minutes to complete the first L levels.

Your task is to discover which option would result in the least amount of total time to finish the game 
(including the time you have already spent).
```
##### Input
```
The first line of the input gives the number of test cases, T. T test cases follow.

The first (and only) line of each test case contains three integers N, K and S: the number of levels in
the game, the current level you are in, and the level where you have to pick up the sword, respectively.
```
##### Output
```
For each test case, output one line containing Case #x: y, where x is the test case number (starting from 1)
and y is the least amount of total time to finish the game.
```
##### E.g.

###### Input
```
2
10 5 2
10 7 6
```
###### Output
```
Case #1: 15
Case #2: 12
```
##### Code:
```c++
#include<bits/stdc++.h>
using namespace std;

#define pb push_back
#define mk make_pair


void solve(int i)
{
	long n, k, s;
	cin>>n>>k>>s;

	long t1 = k + (k - s) + (n - s);
	long t2 = k + n;

	if (t1 >= t2)
	{
		cout<<"Case "<<"#"<<i<<":"<<" "<<t2<<"\n";
	}

	else
	{
		cout<<"Case "<<"#"<<i<<":"<<" "<<t1<<"\n";
	}
}

int main()
{
	ios::sync_with_stdio(0);
	cin.tie(0);

	int t;
	int i = 0;
	cin>>t;
	while (t-- > 0)
	{
	    i++;
		solve(i);
	}
}
```
[Code Demo Link](https://replit.com/@ZaidQamar/retype#main.cpp)

![](https://media.giphy.com/media/jR03rPYvUSzkMVXtHH/giphy.gif)

#### Problem 2: Boring Numbers
![](https://media.giphy.com/media/XuDlhFtiWXZEk/giphy.gif)
```
Ron read a book about boring numbers. According to the book, a positive number is called boring if all
of the digits at even positions in the number are even and all of the digits at odd positions are odd.
The digits are enumerated from left to right starting from 1. For example, the number 1478 is boring 
as the odd positions include the digits {1, 7} which are odd and even positions include the digits
{4, 8} which are even.

Given two numbers L and R, Ron wants to count how many numbers in the range [L, R] (L and R inclusive)
are boring. Ron is unable to solve the problem, hence he needs your help.
```
##### Input
```
The first line of the input gives the number of test cases, T. T test cases follow.
Each test case consists of a single line with two numbers L and R.
```
##### Output
```
For each test case, output one line containing Case #x: y, where x is the test case 
number (starting from 1) and y is the count of boring numbers.
```
##### Sample Input
```
3
5 15
120 125
779 783
```
##### Sample Output
```
Case #1: 6
Case #2: 3
Case #3: 2
```
