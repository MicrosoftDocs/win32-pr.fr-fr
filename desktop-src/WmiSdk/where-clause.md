---
description: Utilisez la clause WHERE pour limiter l’étendue d’une requête de données, d’événement ou de schéma.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: WHERE, clause (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a6a51657dac26a002890bde8346cd7570f6057f2ace5cdfb5350d6c90d0fee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312180"
---
# <a name="where-clause-wmi"></a>WHERE, clause (WMI)

Utilisez la clause WHERE pour limiter l’étendue d’une requête de données, d’événement ou de schéma. Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md). La clause WHERE est constituée d’une propriété ou d’un mot clé, d’un opérateur et d’une constante. toutes les clauses where doivent spécifier l’un des opérateurs prédéfinis qui sont inclus dans le langage de requête WMI (Windows Management Instrumentation (WMI) Query Language (WQL). Vous pouvez ajouter la clause WHERE à l’instruction SELECT en utilisant l’une des formes suivantes :


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



où \* est l’élément interrogé à propos de, Class est la classe dans laquelle interroger, et constant, Operator et Property sont la constante, l’opérateur et la propriété ou le mot clé à utiliser. Pour plus d’informations sur l’instruction SELECT, consultez [instruction SELECT pour les requêtes de données](select-statement-for-data-queries.md), [instruction SELECT pour les requêtes d’événement](select-statement-for-event-queries.md)ou [instruction SELECT pour les requêtes de schéma](select-statement-for-schema-queries.md).

La valeur de la constante doit être du type correct pour la propriété. En outre, l’opérateur doit faire partie de la liste des [opérateurs WQL](wql-operators.md)valides. Un nom de propriété ou une constante doit apparaître de chaque côté de l’opérateur dans la clause WHERE.

Vous pouvez utiliser des littéraux de chaîne, tels que « NTFS », dans une clause WHERE. Si vous souhaitez inclure les caractères spéciaux suivants dans votre chaîne, vous devez d’abord placer le caractère dans une séquence d’échappement en faisant précéder le caractère d’une barre oblique inverse ( \\ ) :

-   barre oblique inverse ( \\ \\ )
-   guillemets doubles ( \\ ")
-   guillemets simples ( \\ ')

Les expressions arithmétiques arbitraires ne peuvent pas être utilisées. Par exemple, la requête suivante retourne uniquement les instances de la [**classe \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) qui représentent des lecteurs NTFS :


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



Les noms de propriétés ne peuvent pas figurer des deux côtés de l’opérateur. La requête suivante est un exemple de requête non valide :


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



Pour la plupart des utilisations des descripteurs de classe dans une clause WHERE, WMI signale que la requête n’est pas valide et retourne une erreur. Toutefois, utilisez l’opérateur point (.) pour les propriétés de type **Object** dans WMI. Par exemple, la requête suivante est valide si prop est une propriété valide de MyClass et est un **objet** de type :

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

Les tests de comparaison ne respectent jamais la casse. Autrement dit, les trois instructions suivantes ont toutes la **valeur true**:


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



Vous pouvez construire une requête qui comprend des types de données booléens, mais les seuls types d’opérandes booléens valides sont les types =, ! = et <> . La valeur **true** est équivalente au nombre 1, et la valeur **false** équivaut au nombre 0. Les exemples suivants sont des requêtes qui comparent une valeur booléenne aux valeurs **true** ou **false**.


```sql
SELECT * FROM MyClass WHERE BoolProp = 1
SELECT * FROM MyClass WHERE BoolProp = TRUE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
SELECT * FROM MyClass WHERE BoolProp = 0
SELECT * FROM MyClass WHERE BoolProp = FALSE
SELECT * FROM MyClass WHERE BoolProp != 1
SELECT * FROM MyClass WHERE BoolProp != FALSE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
```



Les exemples suivants sont des requêtes non valides qui tentent d’utiliser des opérandes non valides.


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



Plusieurs groupes de propriétés, d’opérateurs et de constantes peuvent être combinés dans une clause WHERE à l’aide d’opérateurs logiques et de sous-expressions entre parenthèses. Chaque groupe doit être joint avec les [opérateurs](wql-operators.md) and, or ou not comme indiqué dans les requêtes suivantes. La première requête récupère toutes les instances de la [**classe \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) avec la propriété **Name** définie sur C ou D :


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



La deuxième requête récupère les disques nommés « C : » ou « D : » uniquement s’ils disposent d’une certaine quantité d’espace libre et ont des systèmes de fichiers NTFS :


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



Cet exemple montre une requête de schéma à l’aide de la clause WHERE.


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



La classe meta \_ Class identifie cela comme une requête de schéma, la propriété appelée \_ \_ This identifie la classe cible de la requête et l' [opérateur ISA](isa-operator-for-schema-queries.md) demande des définitions pour les sous-classes de la classe cible. Par conséquent, la requête ci-dessus retourne la définition de la classe myClassName et les définitions de toutes ses sous-classes.

L’exemple suivant est une requête de données utilisant les [associateurs de l’instruction](associators-of-statement.md) avec où :


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



L’exemple suivant montre une requête de schéma utilisant des ASSOCIateurs de et où :


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



L’exemple suivant est une requête de données qui utilise les [références de l’instruction](references-of-statement.md) et où :


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



Ce dernier exemple est une requête de schéma utilisant des références de et où :


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



Outre le format [DateTime](date-and-time-format.md) WMI, la clause WHERE WQL prend en charge plusieurs autres formats de date et d’heure :

-   [Formats de date pris en charge par WQL](wql-supported-date-formats.md)
-   [Formats d’heure pris en charge par WQL](wql-supported-time-formats.md)

 

 
