---
description: Récupère toutes les instances associées à une instance source particulière.
ms.assetid: d6bd9643-523d-4d81-8bf1-da52ccc7524d
ms.tgt_platform: multiple
title: ASSOCIATORS OF Statement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec595584efb5c32342e5bbdaa8bae309b21b29d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518928"
---
# <a name="associators-of-statement"></a>ASSOCIATORS OF Statement

Les ASSOCIateurs de l’instruction récupèrent toutes les instances associées à une instance source particulière. Les instances récupérées sont appelées points de terminaison. Chaque point de terminaison est retourné autant de fois qu’il y a d’associations entre celui-ci et l’objet source. Par exemple, supposons qu’il existe des instances A, B, X et Y. Il existe deux instances d’association, une qui lie A et X et une autre qui lie B et Y. La requête suivante retourne le point de terminaison unique X :


```sql
ASSOCIATORS OF {A}
```



Toutefois, si une autre association lie A et X, la requête ci-dessus retourne deux points de terminaison X.

La syntaxe de base pour les ASSOCIateurs d’instruction est la suivante :

``` syntax
ASSOCIATORS OF {ObjectPath}
```

Notez que les accolades font partie de la syntaxe. Tout chemin d’accès d’objet valide peut être utilisé pour ObjectPath. Les jetons dans le chemin d’accès de l’objet ne peuvent pas contenir d’espace blanc. Par exemple, la requête de la liste suivante retourne les instances associées au disque logique spécifié :

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Comme avec l' [instruction SELECT](select-statement-for-data-queries.md), les ASSOCIateurs d’une instruction peuvent inclure une [clause WHERE](where-clause.md), mais la clause WHERE d’un associateur d’instruction est très différente de la clause SELECT statementWHERE.

La [clause WHERE](where-clause.md) des associateurs de l’instruction peut inclure un ou plusieurs des mots clés prédéfinis suivants et leurs valeurs :


```sql
ASSOCIATORS OF {ObjectPath} WHERE
    AssocClass = AssocClassName
    ClassDefsOnly
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
```



Notez que les sous-clauses facultatives ne sont pas séparées par des virgules.

Le mot clé **AssocClass** indique que les points de terminaison retournés doivent être associés à la source par le biais de la classe spécifiée ou de l’une de ses classes dérivées. Par exemple, la requête de la liste suivante retourne uniquement les points de terminaison associés à la source par le biais de la classe d’association [**Win32 \_ SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) ou de l’une de ses classes dérivées :

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

Le mot clé **ClassDefsOnly** indique que la clause retourne un jeu de résultats d’objets de définition de classe plutôt que des instances réelles des classes. Ces objets sont les définitions des classes auxquelles appartiennent les instances de point de terminaison. Par exemple, la requête de la liste suivante retourne les définitions des classes Win32 [**\_ Directory**](/windows/desktop/CIMWin32Prov/win32-directory) et [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) :

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

Les mots clés **ClassDefsOnly** et **ResultClass** s’excluent mutuellement. Leur utilisation conjointe entraîne une erreur de requête non valide.

Le mot clé **RequiredAssocQualifier** indique que les points de terminaison retournés doivent être associés à l’objet source par le biais d’une classe d’association qui inclut le qualificateur spécifié. Ce type de filtrage est utilisé pour éliminer les largeurs de points de terminaison, sauf si les points de terminaison sont associés à la cible via un ensemble particulier de classes d’association avec balises. Par exemple, la requête de la liste suivante retourne des instances de point de terminaison si la classe d’association inclut un qualificateur appelé **Association**.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Le mot clé **RequiredQualifier** indique que les points de terminaison retournés associés à l’objet source doivent inclure le qualificateur spécifié. Le mot clé **RequiredQualifier** peut être utilisé pour inclure des types particuliers d’instances dans le jeu de résultats. Par exemple, la requête de la liste suivante retourne des instances de point de terminaison qui incluent un qualificateur appelé [**paramètres régionaux**](swbemobjectpath-locale.md).

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Le mot clé **ResultClass** indique que les points de terminaison retournés associés à l’objet source doivent appartenir ou être dérivés de la classe spécifiée. Par exemple, la requête de la liste suivante retourne des instances de point de terminaison dérivées de la classe de [**\_ répertoire CIM**](/windows/desktop/CIMWin32Prov/cim-directory) :

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

Les mots clés **ClassDefsOnly** et **ResultClass** s’excluent mutuellement. Leur utilisation conjointe entraîne une erreur de requête non valide.

Le mot clé **ResultRole** indique que les points de terminaison retournés doivent jouer un rôle particulier dans leur association avec l’objet source. Le rôle est défini par la propriété spécifiée, une propriété de référence de type [ref](references.md). Par exemple, le mot clé **ResultRole** peut être utilisé pour récupérer tous les points de terminaison qui ont la propriété **GroupComponent** dans leur association avec un objet source, comme l’illustre la requête suivante.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

Le mot clé **role** indique que les points de terminaison retournés participent à une association avec l’objet source dans lequel l’objet source joue un rôle particulier. Le rôle est défini par la propriété spécifiée, une propriété de référence de type **ref**. Par exemple, le mot clé **role** peut être utilisé pour récupérer tous les points de terminaison associés à un objet source qui ont la propriété **GroupComponent** , comme l’illustre la requête suivante.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> Les requêtes complexes ne peuvent pas utiliser « and » ou « or » pour séparer les mots clés pour les ASSOCIateurs de et les [références d'](references-of-statement.md) instructions. En outre, le signe égal est le seul opérateur valide qui peut être utilisé dans ces requêtes. Par exemple, la requête suivante est valide :

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> Les exemples suivants ne sont pas valides. Le premier exemple n’utilise pas le signe égal et le deuxième exemple tente à tort d’utiliser le mot clé **et** .

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
