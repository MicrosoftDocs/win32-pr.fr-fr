---
description: Une fonction d’agrégation effectue un calcul sur un ensemble de valeurs et retourne une valeur. Cela permet de générer des statistiques de synthèse pour les groupes à plusieurs niveaux avec une faible surcharge.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Fonctions d’agrégation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da68ad1104c93e8ae04f7ec37cbbde5020109336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560054"
---
# <a name="aggregate-functions"></a><span data-ttu-id="af477-104">Fonctions d’agrégation</span><span class="sxs-lookup"><span data-stu-id="af477-104">Aggregate Functions</span></span>

<span data-ttu-id="af477-105">Une fonction d’agrégation effectue un calcul sur un ensemble de valeurs et retourne une valeur.</span><span class="sxs-lookup"><span data-stu-id="af477-105">An aggregate function performs a calculation on a set of values and returns a value.</span></span> <span data-ttu-id="af477-106">Cela permet de générer des statistiques de synthèse pour les groupes à plusieurs niveaux avec une faible surcharge.</span><span class="sxs-lookup"><span data-stu-id="af477-106">Doing so makes it possible to generate summary statistics for multi-level groups with little overhead.</span></span>

## <a name="about-aggregate-functions"></a><span data-ttu-id="af477-107">À propos des fonctions d’agrégation</span><span class="sxs-lookup"><span data-stu-id="af477-107">About Aggregate Functions</span></span>

<span data-ttu-id="af477-108">Les fonctions d’agrégation des langage SQL de recherche Windows (SQL) ont la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="af477-108">Aggregate functions in Windows Search Structured Query Language (SQL) have the following syntax:</span></span>


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



<span data-ttu-id="af477-109">La partie fonction peut inclure l’une des fonctions et la syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="af477-109">The function portion can include any of the following functions and syntax:</span></span>



| <span data-ttu-id="af477-110">Fonction</span><span class="sxs-lookup"><span data-stu-id="af477-110">Function</span></span>                                                              | <span data-ttu-id="af477-111">Description</span><span class="sxs-lookup"><span data-stu-id="af477-111">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af477-112">Moy ( <column> )</span><span class="sxs-lookup"><span data-stu-id="af477-112">AVG(<column>)</span></span>                                                   | <span data-ttu-id="af477-113">Renvoie la moyenne des valeurs d'un groupe.</span><span class="sxs-lookup"><span data-stu-id="af477-113">Returns the average of the values in a group.</span></span> <span data-ttu-id="af477-114">S’applique uniquement aux nombres.</span><span class="sxs-lookup"><span data-stu-id="af477-114">Applies only to numbers.</span></span>                                                                                                                                      |
| <span data-ttu-id="af477-115">BYFREQUENCY ( <column> , <N> )</span><span class="sxs-lookup"><span data-stu-id="af477-115">BYFREQUENCY(<column>, <N>)</span></span>                                | <span data-ttu-id="af477-116">Retourne les N valeurs de colonne les plus fréquentes des résultats dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="af477-116">Returns the most frequent N column values from the results in the group.</span></span> <span data-ttu-id="af477-117">Comprend également le nombre de fois où chaque valeur s’est produite et les identificateurs de document pour les résultats qui contiennent chaque valeur retournée.</span><span class="sxs-lookup"><span data-stu-id="af477-117">Also includes a count of how many times each value occurred and document identifiers for results that contain each returned value.</span></span> |
| <span data-ttu-id="af477-118">CHILDCOUNT ()</span><span class="sxs-lookup"><span data-stu-id="af477-118">CHILDCOUNT()</span></span>                                                          | <span data-ttu-id="af477-119">Retourne le nombre d’éléments d’un groupe (à l’exception des sous-groupes).</span><span class="sxs-lookup"><span data-stu-id="af477-119">Returns the number of items in a group (excluding subgroups).</span></span> <span data-ttu-id="af477-120">S’il existe plusieurs niveaux de regroupement, retourne le nombre de groupes enfants immédiats.</span><span class="sxs-lookup"><span data-stu-id="af477-120">If there are multiple levels of grouping, this returns the number of immediate child groups.</span></span>                                                  |
| <span data-ttu-id="af477-121">COUNT ()</span><span class="sxs-lookup"><span data-stu-id="af477-121">COUNT()</span></span>                                                               | <span data-ttu-id="af477-122">Retourne le nombre d’éléments dans un groupe et tous les sous-groupes.</span><span class="sxs-lookup"><span data-stu-id="af477-122">Returns the number of items in a group and all subgroups.</span></span>                                                                                                                                                   |
| <span data-ttu-id="af477-123">DATERANGE ( <column> )</span><span class="sxs-lookup"><span data-stu-id="af477-123">DATERANGE(<column>)</span></span>                                             | <span data-ttu-id="af477-124">Retourne les limites inférieure et supérieure des valeurs de colonne trouvées dans le groupe de résultats de groupe.</span><span class="sxs-lookup"><span data-stu-id="af477-124">Returns the lower and upper bounds of the column values found in the group results group.</span></span> <span data-ttu-id="af477-125">Valide uniquement pour les propriétés FILETIME.</span><span class="sxs-lookup"><span data-stu-id="af477-125">Valid only for filetime properties.</span></span>                                                                               |
| <span data-ttu-id="af477-126">PREMIER ( <column> , <N> )</span><span class="sxs-lookup"><span data-stu-id="af477-126">FIRST(<column>, <N>)</span></span>                                      | <span data-ttu-id="af477-127">Retourne les N premières valeurs de colonne des résultats feuille trouvés dans un groupe.</span><span class="sxs-lookup"><span data-stu-id="af477-127">Returns the first N column values from leaf results found in a group.</span></span>                                                                                                                                       |
| <span data-ttu-id="af477-128">MAX ( <column> )</span><span class="sxs-lookup"><span data-stu-id="af477-128">MAX(<column>)</span></span>                                                   | <span data-ttu-id="af477-129">Retourne la valeur maximale de l'expression.</span><span class="sxs-lookup"><span data-stu-id="af477-129">Returns the maximum value in the expression.</span></span> <span data-ttu-id="af477-130">S’applique uniquement aux nombres ou aux dates.</span><span class="sxs-lookup"><span data-stu-id="af477-130">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="af477-131">MIN ( <column> )</span><span class="sxs-lookup"><span data-stu-id="af477-131">MIN(<column>)</span></span>                                                   | <span data-ttu-id="af477-132">Retourne la valeur minimale de l'expression.</span><span class="sxs-lookup"><span data-stu-id="af477-132">Returns the minimum value in the expression.</span></span> <span data-ttu-id="af477-133">S’applique uniquement aux nombres ou aux dates.</span><span class="sxs-lookup"><span data-stu-id="af477-133">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="af477-134">REPRESENTATIVEOF ( <column> , <idRepresentative> , <N> )</span><span class="sxs-lookup"><span data-stu-id="af477-134">REPRESENTATIVEOF(<column>, <idRepresentative>, <N>)</span></span> | <span data-ttu-id="af477-135">Retourne N valeurs idRepresentative, chacune sélectionnée à partir de l’un des sous-ensembles de résultats qui a une valeur de colonne unique.</span><span class="sxs-lookup"><span data-stu-id="af477-135">Returns N idRepresentative values, each selected from one of the result subsets that has a unique column value.</span></span> <span data-ttu-id="af477-136">Chaque valeur est également retournée avec un identificateur de document qui a la valeur idRepresentative.</span><span class="sxs-lookup"><span data-stu-id="af477-136">Each value is also returned with a document identifier that has the idRepresentative value.</span></span> |
| <span data-ttu-id="af477-137">SUM ( <column> )</span><span class="sxs-lookup"><span data-stu-id="af477-137">SUM(<column>)</span></span>                                                   | <span data-ttu-id="af477-138">Retourne la somme des valeurs d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="af477-138">Returns the sum of the values in a group.</span></span> <span data-ttu-id="af477-139">S’applique uniquement aux nombres.</span><span class="sxs-lookup"><span data-stu-id="af477-139">Applies only to numbers.</span></span>                                                                                                                                          |



 

 

> [!Note]  
> <span data-ttu-id="af477-140">Les agrégats sont retournés en tant que colonnes individuelles.</span><span class="sxs-lookup"><span data-stu-id="af477-140">Aggregates are returned as individual columns.</span></span> <span data-ttu-id="af477-141">Il s’agit essentiellement de types simples, à l’exception de ByFrequency, First, DateRange et RepresentativeOf, qui sont retournés en tant que types composés.</span><span class="sxs-lookup"><span data-stu-id="af477-141">They are mostly simple types except for ByFrequency, First, DateRange, and RepresentativeOf which are returned as compound types.</span></span>

 

<span data-ttu-id="af477-142">Vous pouvez utiliser n’importe quelle colonne numérique ou de date pour les agrégations, et pas seulement celles qui se trouvent dans la clause SELECT.</span><span class="sxs-lookup"><span data-stu-id="af477-142">You can use any numeric or date column for aggregations, and not only those that are in the SELECT clause.</span></span> <span data-ttu-id="af477-143">Toutefois, vous ne pouvez pas regrouper sur des agrégats.</span><span class="sxs-lookup"><span data-stu-id="af477-143">However, you cannot group on aggregates.</span></span> <span data-ttu-id="af477-144">Une erreur de syntaxe est retournée si l’argument de colonne passé n’est pas un type numérique ou de date.</span><span class="sxs-lookup"><span data-stu-id="af477-144">A syntax error is returned if the column argument passed in is not either a numeric or date type.</span></span>

<span data-ttu-id="af477-145">La partie étiquette est facultative et fournit un alias plus lisible pour l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="af477-145">The label portion is optional and provides a more readable alias for the label.</span></span> <span data-ttu-id="af477-146">Si vous n’incluez pas d’étiquette d’alias, Windows Search transforme la fonction et le nom de colonne en une étiquette.</span><span class="sxs-lookup"><span data-stu-id="af477-146">If you do not include an alias label, then Windows Search transforms the function and column name into a label.</span></span> <span data-ttu-id="af477-147">Par exemple, MAX (System.Document. WordCount) devient MAX \_ SystemDocumentWordCount.</span><span class="sxs-lookup"><span data-stu-id="af477-147">For example, MAX(System.Document.WordCount) becomes MAX\_SystemDocumentWordCount.</span></span>

## <a name="multi-level-groups-and-counting"></a><span data-ttu-id="af477-148">Groupes et décomptes à plusieurs niveaux</span><span class="sxs-lookup"><span data-stu-id="af477-148">Multi-level Groups and Counting</span></span>

<span data-ttu-id="af477-149">Les agrégats sont définis à travers les feuilles et sont dupliqués.</span><span class="sxs-lookup"><span data-stu-id="af477-149">Aggregates are defined over leaves and are duplicated.</span></span> <span data-ttu-id="af477-150">Un agrégat prend comme entrée les feuilles du groupe qui le définit (documents), plutôt que les sous-groupes de ses enfants.</span><span class="sxs-lookup"><span data-stu-id="af477-150">An aggregate takes as input the leaves of the group that defines it (documents), rather than the subgroups of its children.</span></span> <span data-ttu-id="af477-151">Cette fonctionnalité est appelée regroupement à plusieurs niveaux.</span><span class="sxs-lookup"><span data-stu-id="af477-151">This functionality is referred to as multi-level grouping.</span></span>

<span data-ttu-id="af477-152">En plus des agrégats définis sur les feuilles et dupliqués, ils ne sont comptés qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="af477-152">In addition to aggregates being defined over leaves and duplicated, they are counted only once.</span></span> <span data-ttu-id="af477-153">Même si le même document peut être représenté plusieurs fois dans un groupe, les agrégats ne le considèrent qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="af477-153">While the same document might be represented multiple times under one group, aggregates would only consider it once.</span></span> <span data-ttu-id="af477-154">Le graphique suivant illustre ce concept.</span><span class="sxs-lookup"><span data-stu-id="af477-154">The following graphic illustrates this concept.</span></span>

![Diagramme montrant que les agrégats sont définis au-dessus des feuilles et dupliqués, et ne sont comptés qu’une seule fois](images/aggregates.png)

## <a name="aggregate-examples"></a><span data-ttu-id="af477-156">Exemples d’agrégats</span><span class="sxs-lookup"><span data-stu-id="af477-156">Aggregate Examples</span></span>

<span data-ttu-id="af477-157">Voici des exemples de fonctions d’agrégation dans la clause GROUP ON :</span><span class="sxs-lookup"><span data-stu-id="af477-157">The following are examples of aggregate functions within the GROUP ON clause:</span></span>


```
GROUP ON System.Sender ['d','m','r'] 
    AGGREGATE COUNT() as 'Total',
              MAX(System.Size) as 'Max Size',
              MIN(System.Size) as 'Min Size'
    OVER (SELECT System.Subject FROM systemindex)
              
GROUP ON System.Sender ['d', 'm', 'r']
      AGGREGATE MAX(System.Search.Rank) as 'MaxRank', 
                MIN(System.Search.Rank) as 'MinRank'
      OVER (GROUP ON system.conversationID
                  OVER (SELECT workid, System.ItemUrl FROM systemindex
                        WHERE CONTAINS (*, 'sometext')
                        ORDER BY System.DateCreated))
               
GROUP ON System.FileName [before('a'),before('z')] 
      AGGREGATE MAX(System.Size) as 'maxsize', MIN(System.Size) as 'MinSize' 
      OVER (SELECT System.FileName FROM systemindex
            ORDER BY System.FileName)      
            
GROUP ON System.author 
      AGGREGATE MAX(System.size) as 'maxsize' 
      ORDER BY min(System.Size) 
      OVER (GROUP ON System.DateCreated 
                  AGGREGATE Count() 
                  ORDER BY MAX(System.size) 
                  OVER (SELECT filename, System.DateCreated, System.Size FROM systemindex
                        WHERE CONTAINS('text')))
```



## <a name="return-value"></a><span data-ttu-id="af477-158">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="af477-158">Return Value</span></span>

<span data-ttu-id="af477-159">La valeur de retour est une variante trouvée sur l’ensemble de lignes en tant que propriété personnalisée, en tant qu’alias spécifié ou en tant qu’agrégats si aucune étiquette d’alias n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="af477-159">The return value is a variant found on the rowset as a custom property, either as the specified aliases or as "Aggregates" if no alias label is specified.</span></span>

 

 



