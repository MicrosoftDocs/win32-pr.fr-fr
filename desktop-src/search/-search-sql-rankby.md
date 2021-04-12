---
description: Les résultats d’une requête incluent à la fois les lignes retournées par la requête et une valeur de classement pour chaque ligne si la colonne Rank est incluse dans la clause SELECT.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: RANK BY, clause
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de7f7a63e33f43ba6387cbcea44a5f5b5ae8f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201295"
---
# <a name="rank-by-clause"></a><span data-ttu-id="b0e31-103">RANK BY, clause</span><span class="sxs-lookup"><span data-stu-id="b0e31-103">RANK BY Clause</span></span>

<span data-ttu-id="b0e31-104">Les résultats d’une requête incluent à la fois les lignes retournées par la requête et une valeur de classement pour chaque ligne si la colonne Rank est incluse dans la clause SELECT.</span><span class="sxs-lookup"><span data-stu-id="b0e31-104">The results from a query include both the rows returned by the query and a rank value for each row if the rank column is included in the SELECT clause.</span></span> <span data-ttu-id="b0e31-105">Les valeurs de classement sont calculées par le moteur de recherche et sont retournées sous forme d’entiers dans la plage de zéro à 1000.</span><span class="sxs-lookup"><span data-stu-id="b0e31-105">The rank values are calculated by the Search engine and are returned as integers in the range zero to 1000.</span></span> <span data-ttu-id="b0e31-106">Pour que les résultats de classement soient plus significatifs, la requête peut contrôler la façon dont les valeurs de classement brutes sont calculées dans la clause RANK BY.</span><span class="sxs-lookup"><span data-stu-id="b0e31-106">To make the rank results more meaningful, the query can control how raw rank values are calculated in the RANK BY clause.</span></span>

<span data-ttu-id="b0e31-107">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="b0e31-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="b0e31-108">RANK BY, clause</span><span class="sxs-lookup"><span data-stu-id="b0e31-108">RANK BY Clause</span></span>](#rank-by-clause)
-   [<span data-ttu-id="b0e31-109">Fonction WEIGHT</span><span class="sxs-lookup"><span data-stu-id="b0e31-109">WEIGHT Function</span></span>](#weight-function)
-   [<span data-ttu-id="b0e31-110">Fonction de contrainte</span><span class="sxs-lookup"><span data-stu-id="b0e31-110">COERCION Function</span></span>](#coercion-function)

## <a name="rank-by-clause"></a><span data-ttu-id="b0e31-111">RANK BY, clause</span><span class="sxs-lookup"><span data-stu-id="b0e31-111">RANK BY Clause</span></span>

<span data-ttu-id="b0e31-112">La syntaxe de la clause RANK BY est la suivante :</span><span class="sxs-lookup"><span data-stu-id="b0e31-112">The syntax for the RANK BY clause is as follows:</span></span>


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



<span data-ttu-id="b0e31-113">La clause RANK BY est appliquée à la condition de recherche qui la \_ précède immédiatement, en spécifiant en fait un rang inférieur ou supérieur pour les lignes retournées par cette condition de recherche que les lignes retournées par une autre condition de recherche.</span><span class="sxs-lookup"><span data-stu-id="b0e31-113">The RANK BY clause is applied to the search\_condition immediately preceding it, effectively specifying a lower or higher rank for rows returned by that search condition than rows returned by another search condition.</span></span> <span data-ttu-id="b0e31-114">Les parenthèses entourant la condition de recherche \_ sont requises.</span><span class="sxs-lookup"><span data-stu-id="b0e31-114">The parentheses surrounding the search\_condition are required.</span></span> <span data-ttu-id="b0e31-115">Les parenthèses entourant la spécification de classement sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="b0e31-115">The parentheses surrounding the rank specification are optional.</span></span>

<span data-ttu-id="b0e31-116">Plusieurs clauses RANK BY peuvent être appliquées à une seule condition.</span><span class="sxs-lookup"><span data-stu-id="b0e31-116">More than one RANK BY clause can be applied to a single condition.</span></span> <span data-ttu-id="b0e31-117">Vous pouvez inclure des clauses rang BY supplémentaires une après l’autre en utilisant des parenthèses.</span><span class="sxs-lookup"><span data-stu-id="b0e31-117">You can include additional RANK BY clauses one after the other using parentheses.</span></span>

> [!Note]  
> <span data-ttu-id="b0e31-118">Les prédicats de texte intégral retournent des valeurs de classement comprises dans la plage 0 à 1000.</span><span class="sxs-lookup"><span data-stu-id="b0e31-118">Full-text predicates return rank values in the range 0 to 1000.</span></span> <span data-ttu-id="b0e31-119">Les valeurs de classement de tous les documents correspondant à un prédicat de texte non intégral sont 1000.</span><span class="sxs-lookup"><span data-stu-id="b0e31-119">Rank values for all documents matched by a non-full-text predicate are 1000.</span></span> <span data-ttu-id="b0e31-120">Les modifications apportées aux valeurs de classement doivent tenir compte de ces informations.</span><span class="sxs-lookup"><span data-stu-id="b0e31-120">Modifications to the rank values should take this information into account.</span></span>

 

<span data-ttu-id="b0e31-121">La \_ partie spécification de classement de la clause RANKBY identifie une ou plusieurs fonctions à appliquer aux valeurs de classement.</span><span class="sxs-lookup"><span data-stu-id="b0e31-121">The rank\_specification portion of the RANKBY clause identifies one or more functions to apply to the rank values.</span></span> <span data-ttu-id="b0e31-122">La fonction WEIGHT applique un multiplicateur à la valeur de classement brute d’une ligne retournée.</span><span class="sxs-lookup"><span data-stu-id="b0e31-122">The WEIGHT function applies a multiplier to the raw rank value for a returned row.</span></span> <span data-ttu-id="b0e31-123">Plus le multiplicateur est petit, plus la valeur de classement qui en résulte est faible.</span><span class="sxs-lookup"><span data-stu-id="b0e31-123">The smaller the multiplier, the lower the resulting rank value.</span></span> <span data-ttu-id="b0e31-124">La fonction de forçage peut être utilisée pour multiplier, ajouter ou définir une valeur de classement spécifique pour une ligne retournée.</span><span class="sxs-lookup"><span data-stu-id="b0e31-124">The COERCION function can be used to multiply, add to, or set a specific rank value for a returned row.</span></span> <span data-ttu-id="b0e31-125">Chaque spécification de classement peut inclure zéro ou une fonction de pondération et zéro ou plusieurs fonctions de forçage de type.</span><span class="sxs-lookup"><span data-stu-id="b0e31-125">Each rank specification can include either zero or one WEIGHT function and zero or more COERCION functions.</span></span> <span data-ttu-id="b0e31-126">Si les fonctions de pondération et de contrainte sont incluses dans une clause RANK BY, la fonction WEIGHT doit être la première.</span><span class="sxs-lookup"><span data-stu-id="b0e31-126">If both WEIGHT and COERCION functions are included in a RANK BY clause, the WEIGHT function must be first.</span></span>

## <a name="weight-function"></a><span data-ttu-id="b0e31-127">Fonction WEIGHT</span><span class="sxs-lookup"><span data-stu-id="b0e31-127">WEIGHT Function</span></span>

<span data-ttu-id="b0e31-128">La syntaxe de la fonction WEIGHT est la suivante :</span><span class="sxs-lookup"><span data-stu-id="b0e31-128">The syntax of the WEIGHT function is:</span></span>


```
WEIGHT ( <weight_multipler> ) 
```



<span data-ttu-id="b0e31-129">Le multiplicateur doit être un nombre décimal compris entre 0,001 et 1,000.</span><span class="sxs-lookup"><span data-stu-id="b0e31-129">The multiplier must be a decimal from 0.001 to 1.000.</span></span> <span data-ttu-id="b0e31-130">La valeur de classement brute retournée par le prédicat de condition de recherche est multipliée par le multiplicateur de pondération pour définir une nouvelle valeur de classement.</span><span class="sxs-lookup"><span data-stu-id="b0e31-130">The raw rank value returned by the search condition predicate is multiplied by the weight multiplier to set a new rank value.</span></span>

<span data-ttu-id="b0e31-131">Dans l’exemple suivant, la fonction WEIGHT donne des documents avec le mot « Theresa » dans le ument System.Doc. Champ LastAuthor de la moitié de la valeur de classement des documents avec « Theresa » dans le champ System. Author :</span><span class="sxs-lookup"><span data-stu-id="b0e31-131">In the following example, the WEIGHT function gives documents with the word "Theresa" in the System.Document.LastAuthor field half the rank value of documents with "Theresa" in the System.Author field:</span></span>


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> <span data-ttu-id="b0e31-132">Les fonctionnalités de pondération de colonne de prédicat CONTAINs et FREETEXT prennent en charge un format abrégé à l’aide d’un signe deux-points entre le terme de recherche et le multiplicateur (« Software » : 0.25).</span><span class="sxs-lookup"><span data-stu-id="b0e31-132">The CONTAINS and FREETEXT predicate column weighting features support a shorthand format using a colon between the search term and the multiplier ("software":0.25).</span></span> <span data-ttu-id="b0e31-133">La clause RANK BY ne prend pas en charge la forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="b0e31-133">The RANK BY clause does not support the shortened form.</span></span>

 

<span data-ttu-id="b0e31-134">Il existe une limitation lors de l’utilisation du classement par poids : il ne fonctionne pas avec les clauses CONTAINs qui utilisent des conditions booléennes ; par exemple, l’exemple suivant n’est pas autorisé :</span><span class="sxs-lookup"><span data-stu-id="b0e31-134">There is a limitation when using RANK BY WEIGHT: it does not work with CONTAINS clauses that use Boolean conditions; for example, the following example is not permitted:</span></span>


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a><span data-ttu-id="b0e31-135">Fonction de contrainte</span><span class="sxs-lookup"><span data-stu-id="b0e31-135">COERCION Function</span></span>

<span data-ttu-id="b0e31-136">La fonction de forçage de rang peut être utilisée pour modifier la valeur de classement retournée par addition ou multiplication ou en lui assignant une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="b0e31-136">The rank coercion function can be used to change the returned rank value by addition or multiplication or by assigning it a specific value.</span></span>

<span data-ttu-id="b0e31-137">La syntaxe de la fonction de forçage est la suivante :</span><span class="sxs-lookup"><span data-stu-id="b0e31-137">The syntax of the COERCION function is:</span></span>


```
COERCION ( <coercion_operation> , <coercion_value> )
```



<span data-ttu-id="b0e31-138">La valeur de forçage de type est une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="b0e31-138">The coercion value is an integer value.</span></span>

<span data-ttu-id="b0e31-139">Le tableau suivant décrit les paramètres d’opération de forçage disponibles.</span><span class="sxs-lookup"><span data-stu-id="b0e31-139">The following table describes the available coercion operation settings.</span></span>



| <span data-ttu-id="b0e31-140">Opération de contrainte</span><span class="sxs-lookup"><span data-stu-id="b0e31-140">Coercion operation</span></span> | <span data-ttu-id="b0e31-141">Description</span><span class="sxs-lookup"><span data-stu-id="b0e31-141">Description</span></span>                                                                                    | <span data-ttu-id="b0e31-142">Plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="b0e31-142">Value range</span></span>  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="b0e31-143">ABSOLUTE</span><span class="sxs-lookup"><span data-stu-id="b0e31-143">ABSOLUTE</span></span>           | <span data-ttu-id="b0e31-144">La valeur de classement retournée est la valeur spécifiée dans la valeur de forçage de la valeur.</span><span class="sxs-lookup"><span data-stu-id="b0e31-144">The rank value returned is the value specified in the coercion value.</span></span>                          | <span data-ttu-id="b0e31-145">0 à 1000</span><span class="sxs-lookup"><span data-stu-id="b0e31-145">0 to 1000</span></span>    |
| <span data-ttu-id="b0e31-146">ADD</span><span class="sxs-lookup"><span data-stu-id="b0e31-146">ADD</span></span>                | <span data-ttu-id="b0e31-147">La valeur de classement retournée est la somme de la valeur de classement brute et de la valeur de forçage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b0e31-147">The rank value returned is the sum of the raw rank value and the specified coercion value.</span></span>     | <span data-ttu-id="b0e31-148">0,001 à 1,0</span><span class="sxs-lookup"><span data-stu-id="b0e31-148">0.001 to 1.0</span></span> |
| <span data-ttu-id="b0e31-149">MULTIPLY</span><span class="sxs-lookup"><span data-stu-id="b0e31-149">MULTIPLY</span></span>           | <span data-ttu-id="b0e31-150">La valeur de classement retournée est le produit de la valeur de classement brute et la valeur de forçage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b0e31-150">The rank value returned is the product of the raw rank value and the specified coercion value.</span></span> | <span data-ttu-id="b0e31-151">0,001 à 1,0</span><span class="sxs-lookup"><span data-stu-id="b0e31-151">0.001 to 1.0</span></span> |



 

 

> [!IMPORTANT]
> <span data-ttu-id="b0e31-152">La recherche peut retourner des valeurs de classement uniquement dans la plage comprise entre 0 et 1000.</span><span class="sxs-lookup"><span data-stu-id="b0e31-152">Search can return rank values only in the range of 0 to 1000.</span></span>

 

 

<span data-ttu-id="b0e31-153">L’exemple suivant utilise la fonction de forçage pour définir tous les documents dont le titre contient « Computer » pour avoir un rang de 1000, tout en réduisant d’un quart le rang des documents contenant à la fois « Computer » et « Software » dans le titre.</span><span class="sxs-lookup"><span data-stu-id="b0e31-153">The following example uses the COERCION function to set all documents with "computer" in the title to have a rank of 1000, while reducing by one-quarter the rank of documents containing both "computer" and "software" in the title.</span></span>


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



