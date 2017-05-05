# h1asd

try catch 中使用异步方法，不会捕捉到异步发生的错误，只有添加Task.Wait类的方法，才会捕捉到错误

```c#
try
{
    Task t1 = Task.Run(() =>
    {
        Thread.Sleep(2000);
        Console.WriteLine("kaishi");
        int i = 0;
        int j = 1;
        int k = j / i;
    });

    Task.WaitAll(t1);

}
catch (Exception err)
{

    Console.WriteLine("chucuo");
    Console.WriteLine("dayincuowo :" + err.ToString());
}
```
