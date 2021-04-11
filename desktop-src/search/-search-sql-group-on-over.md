---
description: Le groupe sur...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: REGROUPER... ... Gestion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d7087305f0a5a86f0288ed92ec4bda5b8c882c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112426"
---
# <a name="group-on--over--statement"></a><span data-ttu-id="fca82-103">REGROUPER... ... Gestion</span><span class="sxs-lookup"><span data-stu-id="fca82-103">GROUP ON ... OVER ... Statement</span></span>

<span data-ttu-id="fca82-104">Le groupe sur... ... l’instruction retourne un ensemble de lignes hiérarchique dans lequel les résultats de la recherche sont divisés en groupes basés sur une colonne spécifiée et des plages de regroupement facultatives.</span><span class="sxs-lookup"><span data-stu-id="fca82-104">The GROUP ON... OVER... statement returns a hierarchical rowset in which search results are divided into groups based on a specified column and optional grouping ranges.</span></span> <span data-ttu-id="fca82-105">Si vous regroupez sur la colonne [System. Kind](../properties/props-system-kind.md) , le jeu de résultats est divisé en plusieurs groupes : l’un pour les documents, l’autre pour les communications, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="fca82-105">If you group on the [System.Kind](../properties/props-system-kind.md) column, the result set is divided into multiple groups: one for documents, one for communications, and so on.</span></span> <span data-ttu-id="fca82-106">Si vous regroupez sur [System. Size](../properties/props-system-size.md) et la plage de groupes 100 Ko, le jeu de résultats est divisé en trois groupes : les éléments de taille < 100 Ko, les éléments de taille >= 100 Ko et les éléments sans valeur de taille.</span><span class="sxs-lookup"><span data-stu-id="fca82-106">If you group on [System.Size](../properties/props-system-size.md) and group range 100 KB, the result set is divided into three groups: items of size < 100 KB, items of size >= 100 KB, and items with no size value.</span></span> <span data-ttu-id="fca82-107">Vous pouvez également agréger des regroupements avec des fonctions.</span><span class="sxs-lookup"><span data-stu-id="fca82-107">You can also aggregate groupings with functions.</span></span>

<span data-ttu-id="fca82-108">Cette rubrique aborde les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="fca82-108">This topic covers the following subjects:</span></span>

-   [<span data-ttu-id="fca82-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fca82-109">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="fca82-110">Plages de groupes</span><span class="sxs-lookup"><span data-stu-id="fca82-110">Group Ranges</span></span>](#group-ranges)
-   [<span data-ttu-id="fca82-111">Étiquetage des groupes</span><span class="sxs-lookup"><span data-stu-id="fca82-111">Labeling Groups</span></span>](#labeling-groups)
-   [<span data-ttu-id="fca82-112">Classement des groupes</span><span class="sxs-lookup"><span data-stu-id="fca82-112">Ordering Groups</span></span>](#ordering-groups)
-   [<span data-ttu-id="fca82-113">Imbrication de groupes</span><span class="sxs-lookup"><span data-stu-id="fca82-113">Nesting Groups</span></span>](#nesting-groups)
-   [<span data-ttu-id="fca82-114">Regroupement sur les propriétés de vecteur</span><span class="sxs-lookup"><span data-stu-id="fca82-114">Grouping on Vector Properties</span></span>](#grouping-on-vector-properties)
-   [<span data-ttu-id="fca82-115">Autres exemples</span><span class="sxs-lookup"><span data-stu-id="fca82-115">More Examples</span></span>](#more-examples)
-   [<span data-ttu-id="fca82-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fca82-116">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="fca82-117">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fca82-117">Syntax</span></span>

<span data-ttu-id="fca82-118">Le groupe sur... ... la syntaxe de l’instruction est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fca82-118">The GROUP ON ... OVER ... statement has the following syntax:</span></span>


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



<span data-ttu-id="fca82-119">où les plages de regroupement sont définies comme suit :</span><span class="sxs-lookup"><span data-stu-id="fca82-119">where grouping ranges are defined as follows:</span></span>


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



<span data-ttu-id="fca82-120">Le groupe sur <column> peut être un [identificateur](-search-sql-identifiers.md) standard ou délimité pour une propriété dans la Banque de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fca82-120">The GROUP ON <column> can be a regular or delimited [identifier](-search-sql-identifiers.md) for a property in the property store.</span></span>

<span data-ttu-id="fca82-121">Le facultatif <group ranges> est une liste d’une ou plusieurs valeurs (nombre, date ou chaîne) utilisées pour diviser les résultats en groupes.</span><span class="sxs-lookup"><span data-stu-id="fca82-121">The optional <group ranges> is a list of one or more values (number, date, or string) used for dividing the results into groups.</span></span> <span data-ttu-id="fca82-122"><range limit>Identifie un point de division dans le jeu de résultats retourné, et <label> identifie une étiquette conviviale pour un groupe.</span><span class="sxs-lookup"><span data-stu-id="fca82-122">The <range limit> identifies a division point in the returned result set, and the <label> identifies a user-friendly label for a group.</span></span> <span data-ttu-id="fca82-123">Vous pouvez diviser le jeu de résultats en autant de groupes que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fca82-123">You can divide the result set into as many groups as you need.</span></span>

<span data-ttu-id="fca82-124">Le premier groupe de résultats inclut les éléments dont la valeur minimale possible pour la propriété spécifiée est inférieure à la limite de la première plage.</span><span class="sxs-lookup"><span data-stu-id="fca82-124">The first group of results includes items with the minimum possible value for the specified property up to but not including the first range limit.</span></span> <span data-ttu-id="fca82-125">Ce groupe peut être référencé à l’aide du mot clé MINVALUE.</span><span class="sxs-lookup"><span data-stu-id="fca82-125">This group can be referred to with the MINVALUE keyword.</span></span> <span data-ttu-id="fca82-126">Le deuxième groupe peut être référencé avec le spécificateur de limite de plage lui-même et comprend les éléments dont la valeur de la propriété spécifiée est supérieure ou égale à la limite de la plage.</span><span class="sxs-lookup"><span data-stu-id="fca82-126">The second group can be referred to with the range limit specifier itself and includes items whose value for the specified property is equal to or greater than the range limit.</span></span> <span data-ttu-id="fca82-127">Tous les éléments qui n’ont pas de valeur pour la propriété spécifiée sont retournés en dernier et peuvent être référencés à l’aide du mot clé **null** .</span><span class="sxs-lookup"><span data-stu-id="fca82-127">Any items that do not have a value for the specified property are returned last and can be referred to with the **NULL** keyword.</span></span>

<span data-ttu-id="fca82-128">Par exemple, une limite de plage de « 2006-01-01 » pour la propriété [System. DateCreated](../properties/props-system-datecreated.md) divise le jeu de résultats en éléments dont les dates sont antérieures à 2006-01-01 (groupe MinValue), les éléments dont la date est identique ou postérieure à 2006-01-01 (groupe 2006-01-01) et les éléments sans date (groupe **null** ).</span><span class="sxs-lookup"><span data-stu-id="fca82-128">For example, a range limit of '2006-01-01' for the [System.DateCreated](../properties/props-system-datecreated.md) property divides the result set into items with dates before 2006-01-01 (MINVALUE group), items with dates on or after 2006-01-01 (2006-01-01 group), and items with no date (**NULL** group).</span></span>

<span data-ttu-id="fca82-129">Dans chaque groupe, les résultats sont triés en fonction des valeurs de la colonne regrouper sur par défaut.</span><span class="sxs-lookup"><span data-stu-id="fca82-129">Within each group, the results are sorted by the values in the GROUP ON column by default.</span></span> <span data-ttu-id="fca82-130">La clause [order by](-search-sql-orderby.md) facultative peut contenir un spécificateur de direction de ASC pour l’ordre croissant (de faible à élevé) ou DESC pour l’ordre décroissant (de haut en bas), et l' [ordre dans la clause Group by](-search-sql-orderingroup.md) peut ordonner chaque groupe à l’aide de différentes règles.</span><span class="sxs-lookup"><span data-stu-id="fca82-130">The optional [ORDER BY](-search-sql-orderby.md) clause can contain a direction specifier of either ASC for ascending (low to high) or DESC for descending (high to low), and the [ORDER IN GROUP BY](-search-sql-orderingroup.md) clause can order each group using different rules.</span></span> <span data-ttu-id="fca82-131">Pour plus d’informations, consultez la section [classement des groupes](#ordering-groups) ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="fca82-131">See the [Ordering Groups](#ordering-groups) section below for more information.</span></span>

## <a name="group-ranges"></a><span data-ttu-id="fca82-132">Plages de groupes</span><span class="sxs-lookup"><span data-stu-id="fca82-132">Group Ranges</span></span>

<span data-ttu-id="fca82-133">Le tableau suivant montre comment les résultats sont divisés en groupes en fonction des limites de plage :</span><span class="sxs-lookup"><span data-stu-id="fca82-133">The following table demonstrates how results are divided into groups based the range limits:</span></span>



| <span data-ttu-id="fca82-134">Exemple ( <column> \[ plages de groupes \] )</span><span class="sxs-lookup"><span data-stu-id="fca82-134">Example (<column> \[group ranges\])</span></span>        | <span data-ttu-id="fca82-135">Résultats</span><span class="sxs-lookup"><span data-stu-id="fca82-135">Result</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fca82-136">System. size \[ 1000, 5000\]</span><span class="sxs-lookup"><span data-stu-id="fca82-136">System.Size \[1000, 5000\]</span></span>                       | <span data-ttu-id="fca82-137">Les résultats sont regroupés en quatre compartiments : **MinValue**: taille < 1000</span><span class="sxs-lookup"><span data-stu-id="fca82-137">Results are grouped into four buckets: **MINVALUE**: Size < 1000</span></span><br/> <span data-ttu-id="fca82-138">**1000 :** 1000 <= taille < 5000</span><span class="sxs-lookup"><span data-stu-id="fca82-138">**1000:** 1000 <= Size < 5000</span></span><br/> <span data-ttu-id="fca82-139">**5000 :** Taille >= 5000</span><span class="sxs-lookup"><span data-stu-id="fca82-139">**5000:** Size >= 5000</span></span><br/> <span data-ttu-id="fca82-140">**Null :** Aucune valeur pour la taille</span><span class="sxs-lookup"><span data-stu-id="fca82-140">**NULL:** No value for Size</span></span><br/>                                                                      |
| <span data-ttu-id="fca82-141">System. Author \[ Before ('m'), après ('r')\]</span><span class="sxs-lookup"><span data-stu-id="fca82-141">System.Author \[BEFORE('m'),AFTER('r')\]</span></span>         | <span data-ttu-id="fca82-142">Les résultats sont regroupés en quatre compartiments : **MinValue :** Author < caractère avant « m »</span><span class="sxs-lookup"><span data-stu-id="fca82-142">Results are grouped into four buckets: **MINVALUE:** Author < character before "m"</span></span><br/> <span data-ttu-id="fca82-143">**m :** caractère avant "m" <= auteur < caractère après "r"</span><span class="sxs-lookup"><span data-stu-id="fca82-143">**m:** character before "m" <= Author < character after "r"</span></span><br/> <span data-ttu-id="fca82-144">**r :** caractère après « r » <= auteur</span><span class="sxs-lookup"><span data-stu-id="fca82-144">**r:** character after "r" <= Author</span></span><br/> <span data-ttu-id="fca82-145">**Null :** Aucune valeur pour Author</span><span class="sxs-lookup"><span data-stu-id="fca82-145">**NULL:** No value for Author</span></span><br/>      |
| <span data-ttu-id="fca82-146">System. Author \[ MinValue/'a to l', "m"/m to z'\]</span><span class="sxs-lookup"><span data-stu-id="fca82-146">System.Author \[MINVALUE/'a to l',"m"/'m to z'\]</span></span> | <span data-ttu-id="fca82-147">Les résultats sont regroupés en trois compartiments : **a à l :** auteur < « m »</span><span class="sxs-lookup"><span data-stu-id="fca82-147">Results are grouped into three buckets: **a to l:** Author < "m"</span></span><br/> <span data-ttu-id="fca82-148">**de m à z :** "m" <= auteur</span><span class="sxs-lookup"><span data-stu-id="fca82-148">**m to z:** "m" <= Author</span></span> <br/> <span data-ttu-id="fca82-149">**Null :** Aucune valeur pour Author</span><span class="sxs-lookup"><span data-stu-id="fca82-149">**NULL:** No value for Author</span></span><br/>                                                                                                               |
| <span data-ttu-id="fca82-150">System. DateCreated \[ « 2005-1-01 », « 2006-6-01 »\]</span><span class="sxs-lookup"><span data-stu-id="fca82-150">System.DateCreated \['2005-1-01','2006-6-01'\]</span></span>   | <span data-ttu-id="fca82-151">Les résultats sont regroupés en quatre compartiments :</span><span class="sxs-lookup"><span data-stu-id="fca82-151">Results are grouped into four buckets:</span></span><br/> <span data-ttu-id="fca82-152">**MinValue :** DateCreated < 2005-1-01</span><span class="sxs-lookup"><span data-stu-id="fca82-152">**MINVALUE:** DateCreated < 2005-1-01</span></span><br/> <span data-ttu-id="fca82-153">**2005-1-01 :** 2005-1-01 <= DateCreated < 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="fca82-153">**2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01</span></span><br/> <span data-ttu-id="fca82-154">**2006-1-01 :** DateCreated >= 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="fca82-154">**2006-1-01:** DateCreated >= 2006-6-01</span></span><br/> <span data-ttu-id="fca82-155">**Null :** Aucune valeur pour DateCreated</span><span class="sxs-lookup"><span data-stu-id="fca82-155">**NULL:** No value for DateCreated</span></span><br/> |



 

 

> [!IMPORTANT]
>
> <span data-ttu-id="fca82-156">Correcte `GROUP ON System.Author['m','z','a']`</span><span class="sxs-lookup"><span data-stu-id="fca82-156">Incorrect: `GROUP ON System.Author['m','z','a']`</span></span>
>
> <span data-ttu-id="fca82-157">Correctrices `GROUP ON System.Author['a','m','z']`</span><span class="sxs-lookup"><span data-stu-id="fca82-157">Correct: `GROUP ON System.Author['a','m','z']`</span></span>

 

 

## <a name="labeling-groups"></a><span data-ttu-id="fca82-158">Étiquetage des groupes</span><span class="sxs-lookup"><span data-stu-id="fca82-158">Labeling Groups</span></span>

<span data-ttu-id="fca82-159">Pour améliorer la lisibilité, vous pouvez étiqueter des groupes à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="fca82-159">To improve readability, you can label groups using the following syntax:</span></span>


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



<span data-ttu-id="fca82-160">L’étiquette est séparée de la limite de plage par une barre oblique et est placée entre guillemets simples.</span><span class="sxs-lookup"><span data-stu-id="fca82-160">The label is separated from the range limit with a slash mark and is enclosed in single quotation marks.</span></span> <span data-ttu-id="fca82-161">Si vous ne spécifiez pas d’étiquette, le nom de groupe est la chaîne de limite de plage.</span><span class="sxs-lookup"><span data-stu-id="fca82-161">If you do not specify a label, the group name is the range limit string.</span></span>

<span data-ttu-id="fca82-162">Voici un exemple de groupes d’étiquetage :</span><span class="sxs-lookup"><span data-stu-id="fca82-162">The following is an example of labeling groups:</span></span>


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



<span data-ttu-id="fca82-163">Dans Windows 7 ou version ultérieure, vous pouvez également utiliser une \[ autre \] étiquette générique pour combiner plusieurs plages de regroupement.</span><span class="sxs-lookup"><span data-stu-id="fca82-163">In Windows 7 or later, you can also use a generic \[OTHER\] label to combine multiple grouping ranges.</span></span> <span data-ttu-id="fca82-164">Les résultats de tous les groupes identifiés avec cette étiquette sont combinés dans un groupe avec cette étiquette.</span><span class="sxs-lookup"><span data-stu-id="fca82-164">Results from all groups identified with this label will be combined into one group with this label.</span></span> <span data-ttu-id="fca82-165">Ce groupe de résultats est retourné après tous les autres groupes, à l’exception du groupe **null** .</span><span class="sxs-lookup"><span data-stu-id="fca82-165">This group of results is returned after all other groups except for the **NULL** group.</span></span> <span data-ttu-id="fca82-166">Le groupe **null** contient des résultats pour les éléments qui n’ont pas de valeur pour la propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fca82-166">The **NULL** group contains results for items that do not have a value for the specified property.</span></span> <span data-ttu-id="fca82-167">Avant Windows 7, l' \[ autre \] étiquette est traitée comme toute autre étiquette de groupe.</span><span class="sxs-lookup"><span data-stu-id="fca82-167">Prior to Windows 7 the \[OTHER\] label is treated like any other group label.</span></span>

<span data-ttu-id="fca82-168">Le code suivant est un exemple d’utilisation de l' \[ autre \] étiquette pour les groupes qui seraient créés dans Windows 7 ou version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="fca82-168">The following code is an example of using the \[OTHER\] label for groups that would be created in Windows 7 or later:</span></span>


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



<span data-ttu-id="fca82-169">Le tableau suivant montre les groupes qui seraient créés par le code de regroupement précédent dans Windows 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fca82-169">The following table shows the groups that would be created by the preceding grouping code in Windows 7 or later.</span></span>



| <span data-ttu-id="fca82-170">Group</span><span class="sxs-lookup"><span data-stu-id="fca82-170">Group</span></span>     | <span data-ttu-id="fca82-171">System.Author</span><span class="sxs-lookup"><span data-stu-id="fca82-171">System.Author</span></span> | <span data-ttu-id="fca82-172">System. FileName</span><span class="sxs-lookup"><span data-stu-id="fca82-172">System.FileName</span></span> |
|-----------|---------------|-----------------|
| <span data-ttu-id="fca82-173">0</span><span class="sxs-lookup"><span data-stu-id="fca82-173">0</span></span>         | <span data-ttu-id="fca82-174">1Bill</span><span class="sxs-lookup"><span data-stu-id="fca82-174">1Bill</span></span>         | <span data-ttu-id="fca82-175">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="fca82-175">Lorem.docx</span></span>      |
| <span data-ttu-id="fca82-176">Q</span><span class="sxs-lookup"><span data-stu-id="fca82-176">Q</span></span>         | <span data-ttu-id="fca82-177">Dame</span><span class="sxs-lookup"><span data-stu-id="fca82-177">Queen</span></span>         | <span data-ttu-id="fca82-178">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="fca82-178">Ipsum.docx</span></span>      |
|           | <span data-ttu-id="fca82-179">Robin</span><span class="sxs-lookup"><span data-stu-id="fca82-179">Robin</span></span>         | <span data-ttu-id="fca82-180">dolor.docx</span><span class="sxs-lookup"><span data-stu-id="fca82-180">dolor.docx</span></span>      |
| <span data-ttu-id="fca82-181">O</span><span class="sxs-lookup"><span data-stu-id="fca82-181">Y</span></span>         | <span data-ttu-id="fca82-182">Zara</span><span class="sxs-lookup"><span data-stu-id="fca82-182">Zara</span></span>          | <span data-ttu-id="fca82-183">amet.docx</span><span class="sxs-lookup"><span data-stu-id="fca82-183">amet.docx</span></span>       |
| <span data-ttu-id="fca82-184">\[AUTRES\]</span><span class="sxs-lookup"><span data-stu-id="fca82-184">\[OTHER\]</span></span> | <span data-ttu-id="fca82-185">Abner</span><span class="sxs-lookup"><span data-stu-id="fca82-185">Abner</span></span>         | <span data-ttu-id="fca82-186">nonummy.docx</span><span class="sxs-lookup"><span data-stu-id="fca82-186">nonummy.docx</span></span>    |
|           | <span data-ttu-id="fca82-187">Bob</span><span class="sxs-lookup"><span data-stu-id="fca82-187">Bob</span></span>           | <span data-ttu-id="fca82-188">laoreet.docx</span><span class="sxs-lookup"><span data-stu-id="fca82-188">laoreet.docx</span></span>    |
|           | <span data-ttu-id="fca82-189">Xaria</span><span class="sxs-lookup"><span data-stu-id="fca82-189">Xaria</span></span>         | <span data-ttu-id="fca82-190">magna.docx</span><span class="sxs-lookup"><span data-stu-id="fca82-190">magna.docx</span></span>      |
| <span data-ttu-id="fca82-191">**NULL**</span><span class="sxs-lookup"><span data-stu-id="fca82-191">**NULL**</span></span>  |               | <span data-ttu-id="fca82-192">aliquam.docx</span><span class="sxs-lookup"><span data-stu-id="fca82-192">aliquam.docx</span></span>    |



 

## <a name="ordering-groups"></a><span data-ttu-id="fca82-193">Classement des groupes</span><span class="sxs-lookup"><span data-stu-id="fca82-193">Ordering Groups</span></span>

<span data-ttu-id="fca82-194">Il existe trois façons de commander des éléments dans des groupes :</span><span class="sxs-lookup"><span data-stu-id="fca82-194">There are three ways to order items in groups:</span></span>

-   <span data-ttu-id="fca82-195">Classement par défaut : Si vous ne spécifiez pas le cas contraire, les résultats sont classés en fonction des valeurs de la colonne regrouper sur, dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="fca82-195">Default ordering: If you do not specify otherwise, the results are ordered by the values in the GROUP ON column, in ascending order.</span></span>
-   <span data-ttu-id="fca82-196">Trier par : vous pouvez spécifier l’ordre décroissant dans une clause ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="fca82-196">ORDER BY: You can specify descending order in an ORDER BY clause.</span></span> <span data-ttu-id="fca82-197">Vous devez classer les résultats en fonction de la colonne regrouper sur.</span><span class="sxs-lookup"><span data-stu-id="fca82-197">You must order the results by the GROUP ON column.</span></span>
-   <span data-ttu-id="fca82-198">ORDRE dans regrouper par : vous pouvez spécifier un ordre différent pour chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="fca82-198">ORDER IN GROUP BY: You can specify a different order for each group.</span></span> <span data-ttu-id="fca82-199">Si vous regroupez sur [System. genre](../properties/props-system-kind.md), vous pouvez commander des documents par [System. Author](../properties/props-system-author.md) et Music par [System. Music. Artist](../properties/props-system-music-artist.md).</span><span class="sxs-lookup"><span data-stu-id="fca82-199">If you group on [System.Kind](../properties/props-system-kind.md), you can order documents by [System.Author](../properties/props-system-author.md) and music by [System.Music.Artist](../properties/props-system-music-artist.md).</span></span>

<span data-ttu-id="fca82-200">Pour plus d’informations sur la façon de trier les résultats, consultez les pages de référence des clauses Order [by](-search-sql-orderby.md) et [Order in Group](-search-sql-orderingroup.md) .</span><span class="sxs-lookup"><span data-stu-id="fca82-200">For more information on ordering results, see the [ORDER BY Clause](-search-sql-orderby.md) and [ORDER IN GROUP Clause](-search-sql-orderingroup.md) reference pages.</span></span>

## <a name="nesting-groups"></a><span data-ttu-id="fca82-201">Imbrication de groupes</span><span class="sxs-lookup"><span data-stu-id="fca82-201">Nesting Groups</span></span>

<span data-ttu-id="fca82-202">Vous pouvez imbriquer des groupes avec plusieurs clauses GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="fca82-202">You can nest groups with multiple GROUP ON clauses.</span></span> <span data-ttu-id="fca82-203">L’ordre spécifié dans la requête est directement reflété dans la hiérarchie des groupes de sortie, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="fca82-203">The order specified in the query is directly reflected in the output group hierarchy, as shown in the following example.</span></span>


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| <span data-ttu-id="fca82-204">System. Kind</span><span class="sxs-lookup"><span data-stu-id="fca82-204">System.Kind</span></span>    | <span data-ttu-id="fca82-205">System.Author</span><span class="sxs-lookup"><span data-stu-id="fca82-205">System.Author</span></span> | <span data-ttu-id="fca82-206">System. DateCreated</span><span class="sxs-lookup"><span data-stu-id="fca82-206">System.DateCreated</span></span> |
|----------------|---------------|--------------------|
| <span data-ttu-id="fca82-207">Documents</span><span class="sxs-lookup"><span data-stu-id="fca82-207">documents</span></span>      | <span data-ttu-id="fca82-208">Willa</span><span class="sxs-lookup"><span data-stu-id="fca82-208">Willa</span></span>         | <span data-ttu-id="fca82-209">2006-01-02</span><span class="sxs-lookup"><span data-stu-id="fca82-209">2006-01-02</span></span>         |
|                |               | <span data-ttu-id="fca82-210">2006-01-05</span><span class="sxs-lookup"><span data-stu-id="fca82-210">2006-01-05</span></span>         |
|                | <span data-ttu-id="fca82-211">Zara</span><span class="sxs-lookup"><span data-stu-id="fca82-211">Zara</span></span>          | <span data-ttu-id="fca82-212">2007-06-02</span><span class="sxs-lookup"><span data-stu-id="fca82-212">2007-06-02</span></span>         |
|                |               | <span data-ttu-id="fca82-213">2007-09-10</span><span class="sxs-lookup"><span data-stu-id="fca82-213">2007-09-10</span></span>         |
| <span data-ttu-id="fca82-214">communications</span><span class="sxs-lookup"><span data-stu-id="fca82-214">communications</span></span> | <span data-ttu-id="fca82-215">Abner</span><span class="sxs-lookup"><span data-stu-id="fca82-215">Abner</span></span>         | <span data-ttu-id="fca82-216">2006-04-16</span><span class="sxs-lookup"><span data-stu-id="fca82-216">2006-04-16</span></span>         |
|                | <span data-ttu-id="fca82-217">Jean</span><span class="sxs-lookup"><span data-stu-id="fca82-217">Jean</span></span>          | <span data-ttu-id="fca82-218">2007-02-20</span><span class="sxs-lookup"><span data-stu-id="fca82-218">2007-02-20</span></span>         |
|                | <span data-ttu-id="fca82-219">Willa</span><span class="sxs-lookup"><span data-stu-id="fca82-219">Willa</span></span>         | <span data-ttu-id="fca82-220">2006-10-15</span><span class="sxs-lookup"><span data-stu-id="fca82-220">2006-10-15</span></span>         |
|                | <span data-ttu-id="fca82-221">Zara</span><span class="sxs-lookup"><span data-stu-id="fca82-221">Zara</span></span>          | <span data-ttu-id="fca82-222">2008-01-02</span><span class="sxs-lookup"><span data-stu-id="fca82-222">2008-01-02</span></span>         |



 

 

## <a name="grouping-on-vector-properties"></a><span data-ttu-id="fca82-223">Regroupement sur les propriétés de vecteur</span><span class="sxs-lookup"><span data-stu-id="fca82-223">Grouping on Vector Properties</span></span>

<span data-ttu-id="fca82-224">Le regroupement sur les propriétés vectorielles, les propriétés qui peuvent contenir une ou plusieurs valeurs simultanément, compare les valeurs de vecteur individuellement par défaut.</span><span class="sxs-lookup"><span data-stu-id="fca82-224">Grouping on vector properties, properties that can contain one or more values simultaneously, compares the vector values individually by default.</span></span> <span data-ttu-id="fca82-225">Par exemple, s’il existe un document, Lorem.docx avec la propriété System. Author comme «Theresa ; Zara» et un autre document, Ipsum.docx avec la propriété System. Author comme « Zara », la requête retourne le jeu de résultats dans deux groupes comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="fca82-225">For example, if there is one document, Lorem.docx, with the System.Author property as "Theresa;Zara" and another document, Ipsum.docx, with the System.Author property as "Zara", the query returns the result set in two groups as shown here:</span></span>


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| <span data-ttu-id="fca82-226">System.Author</span><span class="sxs-lookup"><span data-stu-id="fca82-226">System.Author</span></span> | <span data-ttu-id="fca82-227">System. FileName</span><span class="sxs-lookup"><span data-stu-id="fca82-227">System.FileName</span></span> |
|---------------|-----------------|
| <span data-ttu-id="fca82-228">Theresa</span><span class="sxs-lookup"><span data-stu-id="fca82-228">Theresa</span></span>       | <span data-ttu-id="fca82-229">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="fca82-229">Lorem.docx</span></span>      |
| <span data-ttu-id="fca82-230">Zara</span><span class="sxs-lookup"><span data-stu-id="fca82-230">Zara</span></span>          | <span data-ttu-id="fca82-231">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="fca82-231">Lorem.docx</span></span>      |
|               | <span data-ttu-id="fca82-232">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="fca82-232">Ipsum.docx</span></span>      |



 

<span data-ttu-id="fca82-233">Comme vous pouvez le voir, le regroupement sur des propriétés vectorielles retourne des lignes en double.</span><span class="sxs-lookup"><span data-stu-id="fca82-233">As you can see, grouping on vector properties returns duplicate rows.</span></span> <span data-ttu-id="fca82-234">Lorem.docx apparaît deux fois parce qu’il a deux auteurs.</span><span class="sxs-lookup"><span data-stu-id="fca82-234">Lorem.docx appears twice because it has two authors.</span></span>

 

## <a name="more-examples"></a><span data-ttu-id="fca82-235">Plus d'exemples</span><span class="sxs-lookup"><span data-stu-id="fca82-235">More Examples</span></span>


```
GROUP ON System.Photo.ISOSpeed [0,10,100] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.DateCreated['2005/01/01 00:00:00', '2005/12/30 23:00:00'] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.Author ORDER BY System.Author DESC 
      OVER (GROUP ON System.DateCreated ORDER BY System.DateCreated ASC 
                  OVER (SELECT System.FileName, System.DateCreated, System.Size FROM SystemIndex 
                        WHERE CONTAINS(*, 'text')))

GROUP ON System.ItemName [before('a'), 'a', before ('c'), 'd', after('d')] 
      OVER (SELECT System.ItemName, System.ItemUrl FROM SystemIndex ORDER BY System.ItemName)                        
                        
GROUP ON System.ItemNameDisplay ['a' / 'col_a','c' / 'col_c'] 
      OVER (SELECT System.ItemNameDisplay FROM SystemIndex 
            ORDER BY System.ItemNameDisplay)

GROUP ON System.Size[1,2] 
      OVER (GROUP ON System.Author['a','f','mc','x'] 
                  OVER (GROUP ON System.DateCreated['2005/07/25 07:00:00', '2005/08/25 07:00:00']
                        ORDER BY System.DateCreated DESC 
                              OVER (SELECT System.FileName FROM SystemIndex 
                                    WHERE CONTAINS('text'))))   
```



## <a name="related-topics"></a><span data-ttu-id="fca82-236">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fca82-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fca82-237">Fonctions d’agrégation</span><span class="sxs-lookup"><span data-stu-id="fca82-237">Aggregate Functions</span></span>](-search-sql-aggregates.md)
</dt> <dt>

[<span data-ttu-id="fca82-238">Clause ORDER BY</span><span class="sxs-lookup"><span data-stu-id="fca82-238">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> <dt>

[<span data-ttu-id="fca82-239">COMMANDE dans la clause GROUP</span><span class="sxs-lookup"><span data-stu-id="fca82-239">ORDER IN GROUP Clause</span></span>](-search-sql-orderingroup.md)
</dt> </dl>

 

 
