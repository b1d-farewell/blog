+++ 
date = 2022-08-19
title = "equation solving - Updating the initial guess by using the previous solution - Mathematica Stack Exchange"
description = "Consider the following equation:
$
 \frac{1}{y^2 - 0.3x^2} - \frac{1}{x^2} = 1
 $
I am required to ......"
slug = ""
authors = []
tags = []
categories = []
externalLink = "https://mathematica.stackexchange.com/questions/272243/updating-the-initial-guess-by-using-the-previous-solution"
series = []
+++

# equation solving - Updating the initial guess by using the previous solution - Mathematica Stack Exchange

> [!example]- [๐งทๅ้จ้พๆฅ](<http://localhost:7026/unread/6>) [๐ๅค้จ้พๆฅ](<>)    
> URI:: [๐งท](<http://localhost:7026/unread/6>) [๐](<>) 
> intURI:: [๐งทๅ้จ้พๆฅ](<http://localhost:7026/reading/6>)

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
>  **Description**:: Consider the following equation:
$
 \frac{1}{y^2 - 0.3x^2} - \frac{1}{x^2} = 1
 $
I am required to ......
%%

> [!md] Metadata  
> **ๆ ้ข**:: [equation solving - Updating the initial guess by using the previous solution - Mathematica Stack Exchange](https://mathematica.stackexchange.com/questions/272243/updating-the-initial-guess-by-using-the-previous-solution)  
> **ๆฅๆ**:: [[2022-08-19]]  

## Annotations


> [!srhl6] [[SR6@equation solving - Updating the initial guess by using the previous solution - Mathematica Stack Exchange|๐]] <mark style="background-color: #ffb7da">Highlights</mark> [๐งท](<http://localhost:7026/unread/6#id=1660855040025>) [๐](<#id=1660855040025>)   
> Consider the following equation:
> 
> 1y2โ0.3x2โ1x2=1
> 
> I am required to solve for y for a list of x values, between 0 and 1, using `FindRoot`, see below.
> 
> ```
> f[y_, x_] := 1/(y^2 - 0.3*x^2) - 1
> ```
> ^sran-1660855040025

