---
description: Récupère toutes les instances associées à une instance source particulière.
ms.assetid: d6bd9643-523d-4d81-8bf1-da52ccc7524d
ms.tgt_platform: multiple
title: ASSOCIATORS OF Statement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec595584efb5c32342e5bbdaa8bae309b21b29d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320030"
---
# <a name="associators-of-statement"></a><span data-ttu-id="44210-103">ASSOCIATORS OF Statement</span><span class="sxs-lookup"><span data-stu-id="44210-103">ASSOCIATORS OF Statement</span></span>

<span data-ttu-id="44210-104">Les ASSOCIateurs de l’instruction récupèrent toutes les instances associées à une instance source particulière.</span><span class="sxs-lookup"><span data-stu-id="44210-104">The ASSOCIATORS OF statement retrieves all instances that are associated with a particular source instance.</span></span> <span data-ttu-id="44210-105">Les instances récupérées sont appelées points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="44210-105">The instances that are retrieved are referred to as the endpoints.</span></span> <span data-ttu-id="44210-106">Chaque point de terminaison est retourné autant de fois qu’il y a d’associations entre celui-ci et l’objet source.</span><span class="sxs-lookup"><span data-stu-id="44210-106">Each endpoint is returned as many times as there are associations between it and the source object.</span></span> <span data-ttu-id="44210-107">Par exemple, supposons qu’il existe des instances A, B, X et Y. Il existe deux instances d’association, une qui lie A et X et une autre qui lie B et Y. La requête suivante retourne le point de terminaison unique X :</span><span class="sxs-lookup"><span data-stu-id="44210-107">For example, assume there are instances A, B, X, and Y. Two association instances exist, one that links A and X and another that links B and Y. The following query returns the single endpoint X:</span></span>


```sql
ASSOCIATORS OF {A}
```



<span data-ttu-id="44210-108">Toutefois, si une autre association lie A et X, la requête ci-dessus retourne deux points de terminaison X.</span><span class="sxs-lookup"><span data-stu-id="44210-108">However, if there is another association linking A and X, the above query returns two X endpoints.</span></span>

<span data-ttu-id="44210-109">La syntaxe de base pour les ASSOCIateurs d’instruction est la suivante :</span><span class="sxs-lookup"><span data-stu-id="44210-109">The basic syntax for the ASSOCIATORS OF statement is:</span></span>

``` syntax
ASSOCIATORS OF {ObjectPath}
```

<span data-ttu-id="44210-110">Notez que les accolades font partie de la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="44210-110">Note that the braces are part of the syntax.</span></span> <span data-ttu-id="44210-111">Tout chemin d’accès d’objet valide peut être utilisé pour ObjectPath.</span><span class="sxs-lookup"><span data-stu-id="44210-111">Any valid object path can be used for ObjectPath.</span></span> <span data-ttu-id="44210-112">Les jetons dans le chemin d’accès de l’objet ne peuvent pas contenir d’espace blanc.</span><span class="sxs-lookup"><span data-stu-id="44210-112">The tokens within the object path cannot contain any white space.</span></span> <span data-ttu-id="44210-113">Par exemple, la requête de la liste suivante retourne les instances associées au disque logique spécifié :</span><span class="sxs-lookup"><span data-stu-id="44210-113">For example, the query in the following list returns instances that are associated with the specified logical disk:</span></span>

<dl> <dt>

<span data-ttu-id="44210-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande</span><span class="sxs-lookup"><span data-stu-id="44210-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span data-ttu-id="44210-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About</span><span class="sxs-lookup"><span data-stu-id="44210-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="44210-116">Comme avec l' [instruction SELECT](select-statement-for-data-queries.md), les ASSOCIateurs d’une instruction peuvent inclure une [clause WHERE](where-clause.md), mais la clause WHERE d’un associateur d’instruction est très différente de la clause SELECT statementWHERE.</span><span class="sxs-lookup"><span data-stu-id="44210-116">As with the [SELECT statement](select-statement-for-data-queries.md), an ASSOCIATORS OF statement can include a [WHERE clause](where-clause.md), but the WHERE clause for an ASSOCIATORS OF statement is very different from the SELECT statementWHERE clause.</span></span>

<span data-ttu-id="44210-117">La [clause WHERE](where-clause.md) des associateurs de l’instruction peut inclure un ou plusieurs des mots clés prédéfinis suivants et leurs valeurs :</span><span class="sxs-lookup"><span data-stu-id="44210-117">The [WHERE clause](where-clause.md) of the ASSOCIATORS OF statement can include one or more of the following predefined keywords and their values:</span></span>


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



<span data-ttu-id="44210-118">Notez que les sous-clauses facultatives ne sont pas séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="44210-118">Note that the optional subclauses are not separated by commas.</span></span>

<span data-ttu-id="44210-119">Le mot clé **AssocClass** indique que les points de terminaison retournés doivent être associés à la source par le biais de la classe spécifiée ou de l’une de ses classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="44210-119">The **AssocClass** keyword indicates that the returned endpoints must be associated with the source through the specified class or one of its derived classes.</span></span> <span data-ttu-id="44210-120">Par exemple, la requête de la liste suivante retourne uniquement les points de terminaison associés à la source par le biais de la classe d’association [**Win32 \_ SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) ou de l’une de ses classes dérivées :</span><span class="sxs-lookup"><span data-stu-id="44210-120">For example, the query in the following list returns only endpoints that are associated with the source through the [**Win32\_SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) association class or any of its derived classes:</span></span>

<dl> <dt>

<span data-ttu-id="44210-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande</span><span class="sxs-lookup"><span data-stu-id="44210-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span data-ttu-id="44210-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About</span><span class="sxs-lookup"><span data-stu-id="44210-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="44210-123">Le mot clé **ClassDefsOnly** indique que la clause retourne un jeu de résultats d’objets de définition de classe plutôt que des instances réelles des classes.</span><span class="sxs-lookup"><span data-stu-id="44210-123">The **ClassDefsOnly** keyword indicates that the clause returns a result set of class definition objects rather than actual instances of the classes.</span></span> <span data-ttu-id="44210-124">Ces objets sont les définitions des classes auxquelles appartiennent les instances de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="44210-124">These objects are the definitions of classes to which the endpoint instances belong.</span></span> <span data-ttu-id="44210-125">Par exemple, la requête de la liste suivante retourne les définitions des classes Win32 [**\_ Directory**](/windows/desktop/CIMWin32Prov/win32-directory) et [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) :</span><span class="sxs-lookup"><span data-stu-id="44210-125">For example, the query in the following list returns definitions for the [**Win32\_Directory**](/windows/desktop/CIMWin32Prov/win32-directory) and [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) classes:</span></span>

<dl> <dt>

<span data-ttu-id="44210-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande</span><span class="sxs-lookup"><span data-stu-id="44210-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span data-ttu-id="44210-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About</span><span class="sxs-lookup"><span data-stu-id="44210-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

<span data-ttu-id="44210-128">Les mots clés **ClassDefsOnly** et **ResultClass** s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="44210-128">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="44210-129">Leur utilisation conjointe entraîne une erreur de requête non valide.</span><span class="sxs-lookup"><span data-stu-id="44210-129">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="44210-130">Le mot clé **RequiredAssocQualifier** indique que les points de terminaison retournés doivent être associés à l’objet source par le biais d’une classe d’association qui inclut le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="44210-130">The **RequiredAssocQualifier** keyword indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span> <span data-ttu-id="44210-131">Ce type de filtrage est utilisé pour éliminer les largeurs de points de terminaison, sauf si les points de terminaison sont associés à la cible via un ensemble particulier de classes d’association avec balises.</span><span class="sxs-lookup"><span data-stu-id="44210-131">This type of filtering is used to eliminate broad ranges of endpoints unless the endpoints are associated with the target through a particular set of tagged association classes.</span></span> <span data-ttu-id="44210-132">Par exemple, la requête de la liste suivante retourne des instances de point de terminaison si la classe d’association inclut un qualificateur appelé **Association**.</span><span class="sxs-lookup"><span data-stu-id="44210-132">For example, the query in the following list returns endpoint instances if the association class includes a qualifier called **Association**.</span></span>

<dl> <dt>

<span data-ttu-id="44210-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande</span><span class="sxs-lookup"><span data-stu-id="44210-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span data-ttu-id="44210-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About</span><span class="sxs-lookup"><span data-stu-id="44210-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="44210-135">Le mot clé **RequiredQualifier** indique que les points de terminaison retournés associés à l’objet source doivent inclure le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="44210-135">The **RequiredQualifier** keyword indicates that the returned endpoints associated with the source object must include the specified qualifier.</span></span> <span data-ttu-id="44210-136">Le mot clé **RequiredQualifier** peut être utilisé pour inclure des types particuliers d’instances dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="44210-136">The **RequiredQualifier** keyword can be used to include particular types of instances in the result set.</span></span> <span data-ttu-id="44210-137">Par exemple, la requête de la liste suivante retourne des instances de point de terminaison qui incluent un qualificateur appelé [**paramètres régionaux**](swbemobjectpath-locale.md).</span><span class="sxs-lookup"><span data-stu-id="44210-137">For example, the query in the following list returns endpoint instances that include a qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span>

<dl> <dt>

<span data-ttu-id="44210-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande</span><span class="sxs-lookup"><span data-stu-id="44210-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span data-ttu-id="44210-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About</span><span class="sxs-lookup"><span data-stu-id="44210-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="44210-140">Le mot clé **ResultClass** indique que les points de terminaison retournés associés à l’objet source doivent appartenir ou être dérivés de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="44210-140">The **ResultClass** keyword indicates that the returned endpoints associated with the source object must belong to or be derived from the specified class.</span></span> <span data-ttu-id="44210-141">Par exemple, la requête de la liste suivante retourne des instances de point de terminaison dérivées de la classe de [**\_ répertoire CIM**](/windows/desktop/CIMWin32Prov/cim-directory) :</span><span class="sxs-lookup"><span data-stu-id="44210-141">For example, the query in the following list returns endpoint instances that are derived from the [**CIM\_Directory**](/windows/desktop/CIMWin32Prov/cim-directory) class:</span></span>

<dl> <dt>

<span data-ttu-id="44210-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande</span><span class="sxs-lookup"><span data-stu-id="44210-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span data-ttu-id="44210-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About</span><span class="sxs-lookup"><span data-stu-id="44210-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

<span data-ttu-id="44210-144">Les mots clés **ClassDefsOnly** et **ResultClass** s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="44210-144">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="44210-145">Leur utilisation conjointe entraîne une erreur de requête non valide.</span><span class="sxs-lookup"><span data-stu-id="44210-145">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="44210-146">Le mot clé **ResultRole** indique que les points de terminaison retournés doivent jouer un rôle particulier dans leur association avec l’objet source.</span><span class="sxs-lookup"><span data-stu-id="44210-146">The **ResultRole** keyword indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="44210-147">Le rôle est défini par la propriété spécifiée, une propriété de référence de type [ref](references.md). Par exemple, le mot clé **ResultRole** peut être utilisé pour récupérer tous les points de terminaison qui ont la propriété **GroupComponent** dans leur association avec un objet source, comme l’illustre la requête suivante.</span><span class="sxs-lookup"><span data-stu-id="44210-147">The role is defined by the specified property, a reference property of type [ref](references.md). For example, the **ResultRole** keyword can be used to retrieve all endpoints that have the **GroupComponent** property in their association with a source object, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="44210-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande</span><span class="sxs-lookup"><span data-stu-id="44210-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span data-ttu-id="44210-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About</span><span class="sxs-lookup"><span data-stu-id="44210-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="44210-150">Le mot clé **role** indique que les points de terminaison retournés participent à une association avec l’objet source dans lequel l’objet source joue un rôle particulier.</span><span class="sxs-lookup"><span data-stu-id="44210-150">The **Role** keyword indicates that the returned endpoints participate in an association with the source object where the source object plays a particular role.</span></span> <span data-ttu-id="44210-151">Le rôle est défini par la propriété spécifiée, une propriété de référence de type **ref**. Par exemple, le mot clé **role** peut être utilisé pour récupérer tous les points de terminaison associés à un objet source qui ont la propriété **GroupComponent** , comme l’illustre la requête suivante.</span><span class="sxs-lookup"><span data-stu-id="44210-151">The role is defined by the specified property, a reference property of type **ref**. For example, the **Role** keyword can be used to retrieve all endpoints associated with a source object that have the **GroupComponent** property, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="44210-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Demande</span><span class="sxs-lookup"><span data-stu-id="44210-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span data-ttu-id="44210-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>About</span><span class="sxs-lookup"><span data-stu-id="44210-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> <span data-ttu-id="44210-154">Les requêtes complexes ne peuvent pas utiliser « and » ou « or » pour séparer les mots clés pour les ASSOCIateurs de et les [références d'](references-of-statement.md) instructions.</span><span class="sxs-lookup"><span data-stu-id="44210-154">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and [REFERENCES OF](references-of-statement.md) statements.</span></span> <span data-ttu-id="44210-155">En outre, le signe égal est le seul opérateur valide qui peut être utilisé dans ces requêtes.</span><span class="sxs-lookup"><span data-stu-id="44210-155">Furthermore, the equal sign is the only valid operator that can be used in such queries.</span></span> <span data-ttu-id="44210-156">Par exemple, la requête suivante est valide :</span><span class="sxs-lookup"><span data-stu-id="44210-156">For example, the following query is valid:</span></span>

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> <span data-ttu-id="44210-157">Les exemples suivants ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="44210-157">The next examples are not valid.</span></span> <span data-ttu-id="44210-158">Le premier exemple n’utilise pas le signe égal et le deuxième exemple tente à tort d’utiliser le mot clé **et** .</span><span class="sxs-lookup"><span data-stu-id="44210-158">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword.</span></span>

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
