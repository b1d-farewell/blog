+++ 
date = 2022-08-19
title = "expression - strange behavior of std::cout in c++ - Stack Overflow"
description = ""
slug = ""
authors = []
tags = []
categories = []
externalLink = "https://stackoverflow.com/questions/19231779/strange-behavior-of-stdcout-in-c?rq=1"
series = []
+++

# expression - strange behavior of std::cout in c++ - Stack Overflow

> [!example]- [๐งทๅ้จ้พๆฅ](<http://localhost:7026/unread/4>) [๐ๅค้จ้พๆฅ](<>)    
> URI:: [๐งท](<http://localhost:7026/unread/4>) [๐](<>) 
> intURI:: [๐งทๅ้จ้พๆฅ](<http://localhost:7026/reading/4>)

%%
> [!example]+ **Comments**  
> ```dataview
> TABLE 
>     WITHOUT ID
>     link(Source, dateformat(date(Source), "yyyy-MM-dd")) as Date___, 
>     regexreplace(rows.Comments,"^@@\[\[.+?\]\]\s","") as "Comments"
> FROM "journals"
> WHERE  contains(cmnt, this.file.name)
> FLATTEN cmnt as Comments
> WHERE contains(Comments, this.file.name)
> GROUP BY file.link as Source
> SORT rows.file.day desc
> ```
>  **Description**:: #include &lt;iostream&gt;

int a(int &amp;x) {
    x = -1;
    return x;
}

int main () {
    int x = 5;
    std::cout &lt;&lt; a(x) &lt;&lt; " " &lt;&lt; x &lt;&lt; std::endl;
}
Why output is "-1...
%%

> [!md] Metadata  
> **ๆ ้ข**:: [expression - strange behavior of std::cout in c++ - Stack Overflow](https://stackoverflow.com/questions/19231779/strange-behavior-of-stdcout-in-c?rq=1)  
> **ๆฅๆ**:: [[2022-08-19]]  

## Annotations


> [!srhl6] [[SR4@expression - strange behavior of std::cout in c++ - Stack Overflow|๐]] <mark style="background-color: #ffb7da">Highlights</mark> [๐งท](<http://localhost:7026/unread/4#id=1660854650227>) [๐](<#id=1660854650227>)   
> evaluation of `a(x)` and `x` is not specified. It's unspecified behaviour what happens, in your case the compiler decided to evaluate `x` first, `a(x)` afterwards.
> ^sran-1660854650227

