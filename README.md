# cs_lesson1
hello world

经典性“hello, world”程序可以写为：

using System;

class Hello

{

static void Main() 

{

Console.WriteLine("hello, world");

}

}

C# 程序的源代码通常存储在一个或多个以 .cs 为文件扩展名的文本文件（如 hello.cs）中。可以通过
Visual Studio .NET 所提供的命令行编译器，使用以下命令行指令来编译此程序：

csc hello.cs
它产生一个名为 hello.exe 的应用程序。当此应用程序运行时，它产生的输出是：
hello, world

仔细观察此程序可以发现：

• “using System;”指令引用一个名为 System 的命名空间，它由 Microsoft .NET Framework 类库定
义。此命名空间包含 Main 方法中引用的 Console 类。命名空间提供了一种分层方法来组织一个或多个
程序中的各种元素。用“using”指令指定一个命名空间后，该命名空间中的所有成员均可直接被引用。所
以，在“hello, world”程序中，可直接使用 Console.WriteLine（而不必使用
System.Console.WriteLine）。

• Main 方法是 Hello 类的成员。它具有 static 修饰符，因此 Main 方法是相对于类 Hello 本身而不
是相对于此类的实例。

• 应用程序的入口点（即当程序开始运行时首先被调用的方法）总是名为 Main 的静态方法。

• “hello, world”输出依靠类库实现。C# 语言本身不提供类库，它使用公共的类库（Visual Basic .NET 和
Visual C++ .NET 也使用它）。

对 C 和 C++ 开发人员而言，值得注意的是一些“没有”出现在“hello, world”程序中的东西。

• 该程序中的 Main 方法不是全局的。C# 不支持全局级别的方法和变量；这类元素总是包含在类型声明（如
类声明和结构声明）中。

• 该程序没有使用“::”运算符和“->”运算符。在 C# 中，“::”根本不是运算符，而“->”运算符仅在
一小部分程序中使用，即那些涉及不安全代码的程序（第 A 节）。分隔符“.”在复合名称中使用，如
Console.WriteLine。

• 该程序没有包含前向声明。C# 中声明出现的顺序并不重要，所以不需要作前向声明。

• 该程序没有使用 #include 导入程序文本。程序间的依赖项通过符号而不是文本来控制。这样就消除了由
多种语言编写的应用程序之间的障碍。例如，Console 类不需要用 C# 编写。
