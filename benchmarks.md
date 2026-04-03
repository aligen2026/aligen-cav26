# Benchmarks for Submission #343
## Fibonacci numbers
```
int main()
{
    int x1 = 1;
    int x2 = 1;
    int next_x1, next_x2;
    while (1)
    {
        next_x1 = x2;
        next_x2 = x1 + x2;
        x1 = next_x1;
        x2 = next_x2;
    }
    return 0;
}
```


## Jacobsthal numbers
```
int main()
{
    int x1 = 0;
    int x2 = 1;
    int next_x1, next_x2;
    while (1)
    {
        next_x1 = x2;
        next_x2 = 2 * x1 + x2;
        x1 = next_x1;
        x2 = next_x2;
    }
    return 0;
}
```


## Pell numbers
```
int main()
{
    int x1 = 0;
    int x2 = 1;
    int next_x1, next_x2;
    while (1)
    {
        next_x1 = x2;
        next_x2 = x1 + 2 * x2;
        x1 = next_x1;
        x2 = next_x2;
    }
    return 0;
}
```

## Perrin numbers
```
int main()
{
    int x1 = 3;
    int x2 = 0;
    int x3 = 2;
    int next_x1, next_x2, next_x3;
    while (1)
    {
        next_x1 = x2;
        next_x2 = x3;
        next_x3 = x1 + x2;

        x1 = next_x1;
        x2 = next_x2;
        x3 = next_x3;
    }
    return 0;
}
```


## Tribonacci numbers 
```
int main()
{
    int x1 = 1;
    int x2 = 1;
    int x3 = 2;
    int next_x1, next_x2, next_x3;
    while (1)
    {
        next_x1 = x2;
        next_x2 = x3;
        next_x3 = x1 + x2 + x3;

        x1 = next_x1;
        x2 = next_x2;
        x3 = next_x3;
    }
    return 0;
}
```


## Example 6.2
```
int main()
{
    int x1 = 1;
    int x2 = 1;
    int x3 = 1;
    int x4 = 1;
    int next_x1, next_x2, next_x3, next_x4;
    while (1)
    {
        next_x1 = x1 - x2 - 2 * x3;
        next_x2 = 3 * x1 + x2 + 2 * x3 + 2 * x4;
        next_x3 = -x1 - x4;
        next_x4 = 4 * x1 + x2 + x3 + 2 * x4;

        x1 = next_x1;
        x2 = next_x2;
        x3 = next_x3;
        x4 = next_x4;
    }
    return 0;
}
```


## css2003
```
int x1, x2, x3;
    x1 = 1;
    x2 = 1;
    x3 = 0;
    while (x1 < 1001)
    {
        x1 = x1 + 1;
        x2 = x2 + x3;
        x3 = x3 - 1;
    }
    return 0;
```


## afnp2014
```
int main()
{
    int x1 = 1;
    int x2 = 0;
    while (x2 < 1000)
    {
        x1 = x1 + x2;
        x2 = x2 + 1;
    }
    return 0;
}
```


## gsv2008 
```
int main()
{
    int x1, x2;
    x1 = -50;
    x2 = 10;

    while (x1 < 0)
    {
        x1 = x1 + x2;
        x2++;
    }
    return 0;
}
```


## cggmp2005
```
int main()
{
    int x1, x2;
    x1 = 1;
    x2 = 10;
    while (x2 >= x1)
    {
        x1 = x1 + 2;
        x2 = -1 + x2;
    }
    return 0;
}
```



## bhmr2007
```
int main()
{
    int x1, x2, x3, x4,
    x1 = 0;
    x2 = 0;
    x3 = 0;
    x4 = 10;
    while (x1 < x4)
    {
        if (x2 <= 3)
        {
            x2 = x2 + 1;
            x3 = x3 + 2;
        }
        else
        {
            x2 = x2 + 2;
            x3 = x3 + 1;
        }
        x1 = x1 + 1;
    }
    return 0;
}
```
We add `x2 <= 3` at the first 'if'.

## gcnr2008
```
int main()
{
	int x1, x2, x3, x4;
	x1 = x2 = x3 = x4 = 0;
	while (x2 < 10000)
	{
		if (__VERIFIER_nondet_int())
		{
			x1 = x1 + 1;
			x2 = x2 + 100;
		}
		else if (__VERIFIER_nondet_int())
		{
			if (x1 >= 4)
			{
				x1 = x1 + 1;
				x2 = x2 + 1;
			}
		}
		else if (x2 > 10 * x4 && x3 >= 100 * x1)
		{
			x2 = -x2;
		}
		x4 = x4 + 1;
		x3 = x3 + 10;
	}
	return 0;
}
```



## gj2007
```
int main()
{
    int x1 = 0;
    int x2 = 50;
    while (x1 < 100)
    {
        if (x1 < 50)
        {
            x1 = x1 + 1;
        }
        else
        {
            x1 = x1 + 1;
            x2 = x2 + 1;
        }
    }
    return 0;
}

```


## See-Saw
```
int main()
{
    int x1 = 0;
    int x2 = 0;
    while (1)
    {
        if (x1 >= 5 && x1 <= 7)
        {
            x1 += 2;
            x2 += 1;
        }
        else if (x1 <= 4)
        {
            x1 += 1;
            x2 += 2;
        }
        else if (x1 >= 7 && x1 <= 9)
        {
            x1 += 1;
            x2 += 3;
        }
        else if (x1 >= 9)
        {
            x1 += 2;
            x2 += 1;
        }
    }
    return 0;
}
```
