---
description: Utilisez la clause WHERE pour limiter l’étendue d’une requête de données, d’événement ou de schéma.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: WHERE, clause (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0587bffb1a10c4611773de8a61fdb7ac1576952
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386718"
---
# <a name="where-clause-wmi"></a><span data-ttu-id="e8531-103">WHERE, clause (WMI)</span><span class="sxs-lookup"><span data-stu-id="e8531-103">WHERE Clause (WMI)</span></span>

<span data-ttu-id="e8531-104">Utilisez la clause WHERE pour limiter l’étendue d’une requête de données, d’événement ou de schéma.</span><span class="sxs-lookup"><span data-stu-id="e8531-104">Use the WHERE clause to narrow the scope of a data, event, or schema query.</span></span> <span data-ttu-id="e8531-105">Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="e8531-105">For more information, see [Querying with WQL](querying-with-wql.md).</span></span> <span data-ttu-id="e8531-106">La clause WHERE est constituée d’une propriété ou d’un mot clé, d’un opérateur et d’une constante.</span><span class="sxs-lookup"><span data-stu-id="e8531-106">The WHERE clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="e8531-107">Toutes les clauses WHERE doivent spécifier l’un des opérateurs prédéfinis qui sont inclus dans le langage de requête WMI (Windows Management Instrumentation (WMI) Query Language (WQL).</span><span class="sxs-lookup"><span data-stu-id="e8531-107">All WHERE clauses must specify one of the predefined operators that are included in the Windows Management Instrumentation (WMI) Query Language (WQL).</span></span> <span data-ttu-id="e8531-108">Vous pouvez ajouter la clause WHERE à l’instruction SELECT en utilisant l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8531-108">You can append the WHERE clause to the SELECT statement using one of the following forms:</span></span>


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



<span data-ttu-id="e8531-109">où \* est l’élément interrogé à propos de, Class est la classe dans laquelle interroger, et constant, Operator et Property sont la constante, l’opérateur et la propriété ou le mot clé à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e8531-109">where \* is the item queried about, class is the class in which to query, and constant, operator, and property are the constant, operator, and property or keyword to use.</span></span> <span data-ttu-id="e8531-110">Pour plus d’informations sur l’instruction SELECT, consultez [instruction SELECT pour les requêtes de données](select-statement-for-data-queries.md), [instruction SELECT pour les requêtes d’événement](select-statement-for-event-queries.md)ou [instruction SELECT pour les requêtes de schéma](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="e8531-110">For more information about the SELECT statement, see [SELECT Statement for Data Queries](select-statement-for-data-queries.md), [SELECT Statement for Event Queries](select-statement-for-event-queries.md), or [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="e8531-111">La valeur de la constante doit être du type correct pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="e8531-111">The value of the constant must be of the correct type for the property.</span></span> <span data-ttu-id="e8531-112">En outre, l’opérateur doit faire partie de la liste des [opérateurs WQL](wql-operators.md)valides.</span><span class="sxs-lookup"><span data-stu-id="e8531-112">Moreover, the operator must be among the list of valid [WQL operators](wql-operators.md).</span></span> <span data-ttu-id="e8531-113">Un nom de propriété ou une constante doit apparaître de chaque côté de l’opérateur dans la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="e8531-113">Either a property name or a constant must appear on either side of the operator in the WHERE clause.</span></span>

<span data-ttu-id="e8531-114">Vous pouvez utiliser des littéraux de chaîne, tels que « NTFS », dans une clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="e8531-114">You may use string literals, such as "NTFS", in a WHERE clause.</span></span> <span data-ttu-id="e8531-115">Si vous souhaitez inclure les caractères spéciaux suivants dans votre chaîne, vous devez d’abord placer le caractère dans une séquence d’échappement en faisant précéder le caractère d’une barre oblique inverse ( \\ ) :</span><span class="sxs-lookup"><span data-stu-id="e8531-115">If you wish to include the following special characters in your string, you must first escape the character by prefixing the character with a backslash (\\):</span></span>

-   <span data-ttu-id="e8531-116">barre oblique inverse ( \\ \\ )</span><span class="sxs-lookup"><span data-stu-id="e8531-116">backslash (\\\\)</span></span>
-   <span data-ttu-id="e8531-117">guillemets doubles ( \\ ")</span><span class="sxs-lookup"><span data-stu-id="e8531-117">double quotes (\\")</span></span>
-   <span data-ttu-id="e8531-118">guillemets simples ( \\ ')</span><span class="sxs-lookup"><span data-stu-id="e8531-118">single quotes (\\')</span></span>

<span data-ttu-id="e8531-119">Les expressions arithmétiques arbitraires ne peuvent pas être utilisées.</span><span class="sxs-lookup"><span data-stu-id="e8531-119">Arbitrary arithmetic expressions cannot be used.</span></span> <span data-ttu-id="e8531-120">Par exemple, la requête suivante retourne uniquement les instances de la [**classe \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) qui représentent des lecteurs NTFS :</span><span class="sxs-lookup"><span data-stu-id="e8531-120">For example, the following query returns only the instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class that represent NTFS drives:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



<span data-ttu-id="e8531-121">Les noms de propriétés ne peuvent pas figurer des deux côtés de l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="e8531-121">Property names cannot appear on both sides of the operator.</span></span> <span data-ttu-id="e8531-122">La requête suivante est un exemple de requête non valide :</span><span class="sxs-lookup"><span data-stu-id="e8531-122">The following query is an example of an invalid query:</span></span>


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



<span data-ttu-id="e8531-123">Pour la plupart des utilisations des descripteurs de classe dans une clause WHERE, WMI signale que la requête n’est pas valide et retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="e8531-123">For most uses of class descriptors in a WHERE clause, WMI flags the query as invalid and returns an error.</span></span> <span data-ttu-id="e8531-124">Toutefois, utilisez l’opérateur point (.) pour les propriétés de type **Object** dans WMI.</span><span class="sxs-lookup"><span data-stu-id="e8531-124">However, use the dot (.) operator for properties of type **object** in WMI.</span></span> <span data-ttu-id="e8531-125">Par exemple, la requête suivante est valide si prop est une propriété valide de MyClass et est un **objet** de type :</span><span class="sxs-lookup"><span data-stu-id="e8531-125">For example, the following query is valid if Prop is a valid property of MyClass and is type **object**:</span></span>

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

<span data-ttu-id="e8531-126">Les tests de comparaison ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="e8531-126">Comparison tests are always case-insensitive.</span></span> <span data-ttu-id="e8531-127">Autrement dit, les trois instructions suivantes ont toutes la **valeur true**:</span><span class="sxs-lookup"><span data-stu-id="e8531-127">That is, the following three statements all evaluate to **TRUE**:</span></span>


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



<span data-ttu-id="e8531-128">Vous pouvez construire une requête qui comprend des types de données booléens, mais les seuls types d’opérandes booléens valides sont les types =, ! = et <> .</span><span class="sxs-lookup"><span data-stu-id="e8531-128">You can construct a query that includes Boolean data types, but the only valid Boolean operand types are the =, != and <> types.</span></span> <span data-ttu-id="e8531-129">La valeur **true** est équivalente au nombre 1, et la valeur **false** équivaut au nombre 0.</span><span class="sxs-lookup"><span data-stu-id="e8531-129">The value **TRUE** is equivalent to the number 1, and the value **FALSE** is equivalent to the number 0.</span></span> <span data-ttu-id="e8531-130">Les exemples suivants sont des requêtes qui comparent une valeur booléenne aux valeurs **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="e8531-130">The following examples are of queries that compare a Boolean value against the values **TRUE** or **FALSE**.</span></span>


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



<span data-ttu-id="e8531-131">Les exemples suivants sont des requêtes non valides qui tentent d’utiliser des opérandes non valides.</span><span class="sxs-lookup"><span data-stu-id="e8531-131">The following examples are of invalid queries that attempt to use invalid operands.</span></span>


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



<span data-ttu-id="e8531-132">Plusieurs groupes de propriétés, d’opérateurs et de constantes peuvent être combinés dans une clause WHERE à l’aide d’opérateurs logiques et de sous-expressions entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="e8531-132">Multiple groups of properties, operators, and constants can be combined in a WHERE clause using logical operators and parenthetical subexpressions.</span></span> <span data-ttu-id="e8531-133">Chaque groupe doit être joint avec les [opérateurs](wql-operators.md) and, or ou not comme indiqué dans les requêtes suivantes.</span><span class="sxs-lookup"><span data-stu-id="e8531-133">Each group must be joined with the AND, OR, or NOT [operators](wql-operators.md) as is shown in the following queries.</span></span> <span data-ttu-id="e8531-134">La première requête récupère toutes les instances de la [**classe \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) avec la propriété **Name** définie sur C ou D :</span><span class="sxs-lookup"><span data-stu-id="e8531-134">The first query retrieves all instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class with the **Name** property set to either C or D:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



<span data-ttu-id="e8531-135">La deuxième requête récupère les disques nommés « C : » ou « D : » uniquement s’ils disposent d’une certaine quantité d’espace libre et ont des systèmes de fichiers NTFS :</span><span class="sxs-lookup"><span data-stu-id="e8531-135">The second query retrieves disks named "C:" or "D:" only if they have a certain amount of free space remaining and have NTFS file systems:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



<span data-ttu-id="e8531-136">Cet exemple montre une requête de schéma à l’aide de la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="e8531-136">This example shows a schema query using the WHERE clause.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



<span data-ttu-id="e8531-137">La classe meta \_ Class identifie cela comme une requête de schéma, la propriété appelée \_ \_ This identifie la classe cible de la requête et l' [opérateur ISA](isa-operator-for-schema-queries.md) demande des définitions pour les sous-classes de la classe cible.</span><span class="sxs-lookup"><span data-stu-id="e8531-137">The class meta\_class identifies this as a schema query, the property called \_\_this identifies the target class of the query and the [ISA operator](isa-operator-for-schema-queries.md) requests definitions for the subclasses of the target class.</span></span> <span data-ttu-id="e8531-138">Par conséquent, la requête ci-dessus retourne la définition de la classe myClassName et les définitions de toutes ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="e8531-138">Therefore, the preceding query returns the definition for the myClassName class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="e8531-139">L’exemple suivant est une requête de données utilisant les [associateurs de l’instruction](associators-of-statement.md) avec où :</span><span class="sxs-lookup"><span data-stu-id="e8531-139">The following example is a data query using the [ASSOCIATORS OF statement](associators-of-statement.md) with WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



<span data-ttu-id="e8531-140">L’exemple suivant montre une requête de schéma utilisant des ASSOCIateurs de et où :</span><span class="sxs-lookup"><span data-stu-id="e8531-140">The next example shows a schema query using ASSOCIATORS OF and WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="e8531-141">L’exemple suivant est une requête de données qui utilise les [références de l’instruction](references-of-statement.md) et où :</span><span class="sxs-lookup"><span data-stu-id="e8531-141">The following example is a data query using the [REFERENCES OF statement](references-of-statement.md) and WHERE:</span></span>


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



<span data-ttu-id="e8531-142">Ce dernier exemple est une requête de schéma utilisant des références de et où :</span><span class="sxs-lookup"><span data-stu-id="e8531-142">This last example is a schema query using REFERENCES OF and WHERE:</span></span>


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="e8531-143">Outre le format [DateTime](date-and-time-format.md) WMI, la clause WHERE WQL prend en charge plusieurs autres formats de date et d’heure :</span><span class="sxs-lookup"><span data-stu-id="e8531-143">In addition to the WMI [DATETIME](date-and-time-format.md) format, the WQL WHERE clause supports several other date and time formats:</span></span>

-   [<span data-ttu-id="e8531-144">Formats de date pris en charge par WQL</span><span class="sxs-lookup"><span data-stu-id="e8531-144">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
-   [<span data-ttu-id="e8531-145">Formats d’heure pris en charge par WQL</span><span class="sxs-lookup"><span data-stu-id="e8531-145">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)

 

 
