# New-object-New-collection-to-litteral
Macro that converts New object and New collection to literal

the method newToLitteral is the converter itself
the method MACRO_newToLitteral calls the function above in macro context
the xml part is to be added in a macro xml file 

example, from this:
```4d
$o:=New object("txt1"; "azerty"; "ob"; New object("txt2"; "azerty"))
$c:=New collection("azerty"; 123; False; New object("txt1"; "azerty"); New collection(1; 2; 3))
```
result:
```4d
$c:=["azerty"; 123; False; {txt1: "azerty"}; [1; 2; 3]]
$c:=["azerty"; 123; False; {txt1: "azerty"}; [1; 2; 3]]
```

