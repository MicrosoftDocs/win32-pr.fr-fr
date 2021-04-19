---
description: Les références de l’instruction récupèrent toutes les instances d’association qui font référence à une instance source particulière.
ms.assetid: 674be546-e7fd-4150-9d7c-2888d24bf1b3
ms.tgt_platform: multiple
title: RÉFÉRENCES de l’instruction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c7cc624a1e91220fc6bfc89ef0a75878a9cfb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527812"
---
# <a name="references-of-statement"></a><span data-ttu-id="f7976-103">RÉFÉRENCES de l’instruction</span><span class="sxs-lookup"><span data-stu-id="f7976-103">REFERENCES OF Statement</span></span>

<span data-ttu-id="f7976-104">Les références de l’instruction récupèrent toutes les instances d’association qui font référence à une instance source particulière.</span><span class="sxs-lookup"><span data-stu-id="f7976-104">The REFERENCES OF statement retrieves all association instances that refer to a particular source instance.</span></span> <span data-ttu-id="f7976-105">Les références de l’instruction sont similaires aux ASSOCIATORS OF Statement dans sa syntaxe.</span><span class="sxs-lookup"><span data-stu-id="f7976-105">The REFERENCES OF statement is similar to the ASSOCIATORS OF statement in its syntax.</span></span> <span data-ttu-id="f7976-106">Toutefois, au lieu de récupérer des instances de point de terminaison, il récupère les instances d’association intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="f7976-106">However, rather than retrieving endpoint instances, it retrieves the intervening association instances.</span></span>

<span data-ttu-id="f7976-107">Les références de la clause WHERE peuvent inclure un ou plusieurs des mots clés prédéfinis suivants et leurs valeurs :</span><span class="sxs-lookup"><span data-stu-id="f7976-107">The REFERENCES OF WHERE clause can include one or more of the following predefined keywords and their values:</span></span>


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



<span data-ttu-id="f7976-108">Pour spécifier un objet source, utilisez un chemin d’accès d’objet valide pour ObjetSource.</span><span class="sxs-lookup"><span data-stu-id="f7976-108">To specify a source object, use any valid object path for SourceObject.</span></span> <span data-ttu-id="f7976-109">Comme avec l’instruction SELECT, la clause WHERE est facultative et est utilisée pour définir davantage la requête.</span><span class="sxs-lookup"><span data-stu-id="f7976-109">As with the SELECT statement, the WHERE clause is optional and is used to further define the query.</span></span> <span data-ttu-id="f7976-110">Autrement dit, l’instruction suivante est parfaitement valide :</span><span class="sxs-lookup"><span data-stu-id="f7976-110">That is, the following statement is perfectly valid:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



<span data-ttu-id="f7976-111">Le mot clé **ClassDefsOnly** indique que l’instruction retourne un jeu de résultats d’objets de définition de classe plutôt que des instances réelles des classes d’association.</span><span class="sxs-lookup"><span data-stu-id="f7976-111">The **ClassDefsOnly** keyword indicates that the statement returns a result set of class definition objects rather than actual instances of the association classes.</span></span> <span data-ttu-id="f7976-112">Ces objets contiennent des définitions de classes auxquelles appartiennent les instances qui font référence à l’objet source.</span><span class="sxs-lookup"><span data-stu-id="f7976-112">These objects contain definitions of classes to which the instances that reference the source object belong.</span></span> <span data-ttu-id="f7976-113">Par exemple, l’instruction suivante retourne les définitions des classes **AdapterDriver** et **AdapterProtocol** :</span><span class="sxs-lookup"><span data-stu-id="f7976-113">For example, the following statement returns definitions for the **AdapterDriver** and **AdapterProtocol** classes:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



<span data-ttu-id="f7976-114">Le mot clé **RequiredQualifier** indique que les objets Association retournés doivent inclure le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="f7976-114">The **RequiredQualifier** keyword indicates that the returned association objects must include the specified qualifier.</span></span> <span data-ttu-id="f7976-115">Le mot clé **RequiredQualifier** peut être utilisé pour inclure des instances particulières d’associations dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="f7976-115">The **RequiredQualifier** keyword can be used to include particular instances of associations in the result set.</span></span> <span data-ttu-id="f7976-116">Par exemple, l’instruction suivante retourne les instances d’association qui incluent un qualificateur appelé **AdapterTag**:</span><span class="sxs-lookup"><span data-stu-id="f7976-116">For example, the following statement returns association instances that include a qualifier called **AdapterTag**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



<span data-ttu-id="f7976-117">Le mot clé **ResultClass** indique que les objets Association retournés doivent appartenir ou être dérivés de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f7976-117">The **ResultClass** keyword indicates that the returned association objects must belong to or be derived from the specified class.</span></span> <span data-ttu-id="f7976-118">Par exemple, l’instruction suivante retourne les associations de la classe **AdapterDriver** ou des sous-classes de **AdapterDriver**:</span><span class="sxs-lookup"><span data-stu-id="f7976-118">For example, the following statement returns associations of the **AdapterDriver** class or subclasses of **AdapterDriver**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



<span data-ttu-id="f7976-119">Les mots clés **ClassDefsOnly** et **ResultClass** s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="f7976-119">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="f7976-120">Leur utilisation conjointe entraîne une erreur de requête non valide.</span><span class="sxs-lookup"><span data-stu-id="f7976-120">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="f7976-121">Le mot clé **role** indique que les associations retournées sont uniquement celles dans lesquelles l’objet source joue un rôle particulier.</span><span class="sxs-lookup"><span data-stu-id="f7976-121">The **Role** keyword indicates that the returned associations are only those in which the source object plays a particular role.</span></span> <span data-ttu-id="f7976-122">Le rôle est défini par la propriété spécifiée, une propriété de référence de type [ref](references.md). Le mot clé **role** est utile dans les associations où un objet donné peut jouer un rôle dans certains cas et un autre rôle dans d’autres, par exemple dans les associations hiérarchiques.</span><span class="sxs-lookup"><span data-stu-id="f7976-122">The role is defined by the specified property, a reference property of type [ref](references.md). The **Role** keyword is useful in associations where a certain object can play one role in some cases and another role in others, such as in hierarchical associations.</span></span> <span data-ttu-id="f7976-123">Le mot clé **role** peut être utilisé pour récupérer toutes les associations dans lesquelles l’objet source joue le rôle de parent, par exemple.</span><span class="sxs-lookup"><span data-stu-id="f7976-123">The **Role** keyword can be used to retrieve all of the associations in which the source object plays the role of parent, for example.</span></span> <span data-ttu-id="f7976-124">L’instruction suivante illustre la syntaxe pour la récupération des associations qui ont une propriété **parent** référençant l’objet source en tant que parent :</span><span class="sxs-lookup"><span data-stu-id="f7976-124">The following statement illustrates the syntax for retrieving associations that have a **parent** property referencing the source object as the parent:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> <span data-ttu-id="f7976-125">Les requêtes complexes ne peuvent pas utiliser « and » ou « or » pour séparer les mots clés pour les ASSOCIateurs de et les références d’instructions.</span><span class="sxs-lookup"><span data-stu-id="f7976-125">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and REFERENCES OF statements.</span></span> <span data-ttu-id="f7976-126">En outre, le signe égal est le seul opérateur valide qui peut être utilisé avec les mots clés dans ces requêtes.</span><span class="sxs-lookup"><span data-stu-id="f7976-126">Furthermore, the equal sign is the only valid operator that can be used with the keywords in these queries.</span></span> <span data-ttu-id="f7976-127">Par exemple, la requête suivante est valide :</span><span class="sxs-lookup"><span data-stu-id="f7976-127">For example, the following query is valid:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> <span data-ttu-id="f7976-128">Les exemples suivants ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="f7976-128">The next examples are not valid.</span></span> <span data-ttu-id="f7976-129">Le premier exemple n’utilise pas le signe égal et le deuxième exemple tente d’utiliser par erreur le mot clé **et** :</span><span class="sxs-lookup"><span data-stu-id="f7976-129">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 



