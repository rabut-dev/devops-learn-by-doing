## CKS Usefull Commands


|Command|Description|
|------|-----------|
|`kubectl certificate approve <csr-request-name>`| Approve the CSR request.|
|`<i>, <i0>`|The iteration number indexed from one and from zero, respectively, when referenced within a template being applied to an attribute or attributes. Is only visible to the template being applied to the iterator values.|
|`<attribute.property>`|Looks for property of attribute as a property (C#), then accessor methods like getProperty() or isProperty() or hasProperty(). If that fails, StringTemplate looks for a raw field of the attribute called property. Evaluates to the empty string if no such property is found.|
|`<attribute.(expr)>`|Indirect property lookup. Same as attribute.property except use the value of expr as the property name. Evaluates to the empty string if no such property is found.|
|`<multi-valued-attribute>`|Concatenation of string values of the elements. If multi-valued-attribute is missing, it evaluates to the empty string.|
|`<multi-valued-attribute; separator=expr>`|Concatenation element string values separated by expr.|
|`<[mine, yours]>`|Creates a new multi-valued attribute (a list) with elements of mine first then all of yours.|
|`<template(argument-list)>`|Include template. The argument-list is a list of attribute expressions or attribute assignments where each assignment is of the form arg-of-template=expr. expr is evaluated in the context of the surrounding template not of the invoked template. Example, bold(name) or bold(item=name) of item is an argument of template bold. The sole argument or the final argument, if argument assignments syntax is used, can be the "pass through" argument `...`|
|`<(expr)(argument-list)>`|Include template whose name is computed via expr. The argument-list is a list of attribute expressions or attribute assignments where each assignment is of the form attribute=expr. Example `<(whichFormat)()>` looks up whichFormat's value and uses that as template name. Can also apply an indirect template to an attribute.|
|`<attribute:template(argument-list)>`|Apply template to attribute with optional argument-list.  Example: `<name:bold()>` applies bold() to name's value. The first argument of the template gets the iterated value. The template is not applied to null values.|
|`<attribute:(expr)(argument-list)>`|Apply a template, whose name is computed from expr, to each value of attribute. Example `<data:(name)()>` looks up name's value and uses that as template name to apply to data.|
|`<attribute:t1(argument-list): ... :tN(argument-list)>`|Apply multiple templates in order from left to right. The result of a template application upon a multi-valued attribute is another multi-valued attribute. The overall expression evaluates to the concatenation of all elements of the final multi-valued attribute resulting from templateN's application.|
|`<attribute:{x \| anonymous-template}>`|Apply an anonymous template to each element of attribute.  The iterated value is set to argument x. The anonymous template references ﻿`<x>` to access the iterator value.|
|`<a1,a2,...,aN:{argument-list \| anonymous-template}>`|Parallel list iteration. March through the values of the attributes a1..aN, setting the values to the arguments in argument-list in the same order. Apply the anonymous template.|
|`<attribute:t1(),t2(),`...`,tN()>`|Apply an alternating list of templates to the elements of attribute. The template names may include argument lists.|
|`\<` or `\>`|escaped delimiter prevents `<` or `>` from starting an attribute expression and results in that single character.|
|`<\ >, <\n>, <\t>`|special character(s): space, newline, tab. Can have multiple in single `<...>` expression, e.g. `<\t\t>`.|
|`<\uXXXX>`|Unicode character(s). Can have multiple in single `<...>` expression.|
|`<\\>`|Ignore the immediately following newline char. Allows you to put a newline in the template to better format it without actually inserting a newline into the output|
|`<! comment !>`|Comments, ignored by StringTemplate.|