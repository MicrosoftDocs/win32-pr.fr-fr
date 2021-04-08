---
description: Les colonnes stockées dans l’index de contenu peuvent avoir plusieurs valeurs, et ces colonnes à valeurs multiples peuvent être comparées à l’aide du prédicat de comparaison de tableau.
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: Comparaisons à valeurs multiples (tableau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77710ecdddcf289c9a5c64d0c5f57ca449311097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750373"
---
# <a name="multi-valued-array-comparisons"></a><span data-ttu-id="d3058-103">Comparaisons à valeurs multiples (tableau)</span><span class="sxs-lookup"><span data-stu-id="d3058-103">Multi-Valued (ARRAY) Comparisons</span></span>

<span data-ttu-id="d3058-104">Les colonnes stockées dans l’index de contenu peuvent avoir plusieurs valeurs, et ces colonnes à valeurs multiples peuvent être comparées à l’aide du prédicat de comparaison de tableau.</span><span class="sxs-lookup"><span data-stu-id="d3058-104">Columns stored in the content index can have multiple values, and those multivalued columns can be compared by using the ARRAY comparison predicate.</span></span>

<span data-ttu-id="d3058-105">Le prédicat de comparaison de tableau a la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d3058-105">The ARRAY comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



<span data-ttu-id="d3058-106">Une erreur est retournée si la référence de colonne n’est pas une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="d3058-106">An error is returned if the column reference is not a multivalued column.</span></span> <span data-ttu-id="d3058-107">Le type de données de la colonne doit être compatible avec les éléments de la liste de comparaison.</span><span class="sxs-lookup"><span data-stu-id="d3058-107">The column data type must be compatible with the elements of the comparison list.</span></span> <span data-ttu-id="d3058-108">Si nécessaire, la référence de colonne peut être [convertie](-search-sql-castingdatacolumntype.md) en un autre type de données.</span><span class="sxs-lookup"><span data-stu-id="d3058-108">If necessary, the column reference can be [cast](-search-sql-castingdatacolumntype.md) as another data type.</span></span>

<span data-ttu-id="d3058-109">L’opérateur de comparaison (COMP \_ op) peut être l’un des opérateurs de comparaison normaux.</span><span class="sxs-lookup"><span data-stu-id="d3058-109">The comparison operator (comp\_op) can be any of the normal comparison operators.</span></span> <span data-ttu-id="d3058-110">Dans une comparaison à valeurs multiples, les opérateurs de comparaison ont des significations légèrement différentes selon qu’un quantificateur est utilisé ou non.</span><span class="sxs-lookup"><span data-stu-id="d3058-110">In a multivalued comparison, the comparison operators have slightly different meanings depending on whether a quantifier is used.</span></span> <span data-ttu-id="d3058-111">Les quantificateurs identifient si une comparaison doit être effectuée sur l’ensemble ou une partie des valeurs de la liste de comparaison.</span><span class="sxs-lookup"><span data-stu-id="d3058-111">Quantifiers identify whether a comparison should be made against all or some of the values in the comparison list.</span></span> <span data-ttu-id="d3058-112">Les fonctions des opérateurs de comparaison sont indiquées dans les tableaux décrivant chaque quantificateur (tout ou partie) plus loin dans ce document.</span><span class="sxs-lookup"><span data-stu-id="d3058-112">The functions of the comparison operators are given in the tables describing each quantifier (ALL and SOME) later in this document.</span></span>

<span data-ttu-id="d3058-113">La valeur après l’opérateur spécifie une valeur littérale unique qui est comparée à tous les éléments de la colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="d3058-113">The value after the operator specifies a single literal value that is compared against all elements of the multivalued column.</span></span> <span data-ttu-id="d3058-114">Si un élément correspond à la valeur, le prédicat a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="d3058-114">If any element matches the value, the predicate is true.</span></span>

<span data-ttu-id="d3058-115">La liste de comparaison spécifie un tableau de valeurs littérales comparées à la colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="d3058-115">The comparison list specifies an array of literal values that are compared against the multivalued column.</span></span> <span data-ttu-id="d3058-116">La syntaxe de la liste de comparaison est la suivante :</span><span class="sxs-lookup"><span data-stu-id="d3058-116">The syntax for the comparison list follows:</span></span>


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> <span data-ttu-id="d3058-117">Tenez compte de la syntaxe de la liste de comparaison.</span><span class="sxs-lookup"><span data-stu-id="d3058-117">Be aware of the comparison list syntax.</span></span> <span data-ttu-id="d3058-118">Le groupe de littéraux qui composent la liste de comparaison doit être entouré de crochets.</span><span class="sxs-lookup"><span data-stu-id="d3058-118">The group of literals that make up the comparison list must be surrounded by square brackets.</span></span> <span data-ttu-id="d3058-119">N’entourez pas les éléments individuels de la liste de comparaison par des crochets.</span><span class="sxs-lookup"><span data-stu-id="d3058-119">Do not surround individual elements of the comparison list by square brackets.</span></span> <span data-ttu-id="d3058-120">Par conséquent, le tableau \[ 1 \] et le tableau \[ 1, 2, 3 \] sont valides, mais le tableau \[ 1 \[ , 2 \] \[ , 3 \] \] n’est pas.</span><span class="sxs-lookup"><span data-stu-id="d3058-120">Therefore, ARRAY \[1\] and ARRAY \[1,2,3\] are valid, but ARRAY \[1\[,2\]\[,3\]\] is not.</span></span>

 

<span data-ttu-id="d3058-121">La méthode utilisée pour déterminer si la comparaison à valeurs multiples retourne la valeur true ou false est spécifiée par le quantificateur facultatif.</span><span class="sxs-lookup"><span data-stu-id="d3058-121">The method used to determine whether the multivalued comparison returns true or false is specified by the optional quantifier.</span></span> <span data-ttu-id="d3058-122">Les sections suivantes décrivent chaque quantificateur et le fonctionnement de chaque opérateur de comparaison lorsque le quantificateur est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d3058-122">The following sections describe each quantifier, and how each comparison operator works when the quantifier is used.</span></span>

## <a name="absent-quantifier"></a><span data-ttu-id="d3058-123">Quantificateur absent</span><span class="sxs-lookup"><span data-stu-id="d3058-123">Absent Quantifier</span></span>

<span data-ttu-id="d3058-124">Si aucun quantificateur n’est spécifié, chaque élément du côté gauche de la comparaison est comparé à l’élément situé à la même position sur le côté droit.</span><span class="sxs-lookup"><span data-stu-id="d3058-124">If no quantifier is specified, each element on the left side of the comparison is compared to the element in the same position on the right side.</span></span> <span data-ttu-id="d3058-125">La comparaison commence par le premier élément des tableaux et progresse jusqu’au dernier élément.</span><span class="sxs-lookup"><span data-stu-id="d3058-125">The comparison begins with the first element in the arrays, and progresses through the last element.</span></span> <span data-ttu-id="d3058-126">Si tous les éléments du côté gauche sont équivalents aux éléments correspondants sur le côté droit, le nombre d’éléments de tableau est utilisé pour déterminer le tableau qui est plus grand.</span><span class="sxs-lookup"><span data-stu-id="d3058-126">If all the elements on the left side are equivalent to the corresponding elements on the right side, the number of array elements is used to determine which array is greater.</span></span>

<span data-ttu-id="d3058-127">Le tableau suivant montre l’opération des opérateurs de comparaison quand aucun quantificateur n’est spécifié et fournit une brève description de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="d3058-127">The following table shows the operation of the comparison operators when no quantifier is specified and provides a brief description of each.</span></span>



| <span data-ttu-id="d3058-128">Opérateur</span><span class="sxs-lookup"><span data-stu-id="d3058-128">Operator</span></span>       | <span data-ttu-id="d3058-129">Description</span><span class="sxs-lookup"><span data-stu-id="d3058-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="d3058-130">'Égal à’retourne la valeur true lorsque chaque élément de gauche a la même valeur que l’élément de droite correspondant, et que les deux tableaux ont le même nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="d3058-130">'Equal to' returns true when each left-side element has the same value as the corresponding right-side element, and both arrays have the same number of elements.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="d3058-131">! = ou <></span><span class="sxs-lookup"><span data-stu-id="d3058-131">!= or <></span></span> | <span data-ttu-id="d3058-132">'Différent de’retourne la valeur true lorsqu’un ou plusieurs éléments côté gauche ont des valeurs qui diffèrent des éléments côté droit correspondants, ou lorsque les tableaux de gauche et de droite n’ont pas le même nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="d3058-132">'Not equal to' returns true when one or more left-side elements have values that differ from the corresponding right-side elements, or when the left-side and right-side arrays do not have the same number of elements.</span></span>                                                                                                                                                              |
| >           | <span data-ttu-id="d3058-133">« Supérieur à » retourne la valeur true lorsque la valeur de chaque élément de gauche est supérieure à la valeur de l’élément de droite correspondant.</span><span class="sxs-lookup"><span data-stu-id="d3058-133">'Greater than' returns true when the value of each left-side element is greater than the value of the corresponding right-side element.</span></span> <span data-ttu-id="d3058-134">Si toutes les valeurs d’élément de gauche correspondent exactement aux éléments de droite correspondants et que le tableau de gauche a plus d’éléments que le tableau de droite, « supérieur à » retourne la valeur true.</span><span class="sxs-lookup"><span data-stu-id="d3058-134">If all the left-side element values exactly match the corresponding right-side elements and the left-side array has more elements than the right-side array, 'greater than' returns true.</span></span>                                                     |
| >=          | <span data-ttu-id="d3058-135">'Supérieur ou égal à’retourne la valeur true lorsque la valeur de chaque élément de gauche est supérieure ou égale à la valeur de l’élément de droite correspondant.</span><span class="sxs-lookup"><span data-stu-id="d3058-135">'Greater than or equal to' returns true when the value of every left-side element is greater than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="d3058-136">Si toutes les valeurs d’élément de gauche sont égales ou supérieures aux éléments de droite correspondants et que le tableau de gauche a le même élément ou plus que le tableau de droite, 'supérieur à’retourne la valeur true.</span><span class="sxs-lookup"><span data-stu-id="d3058-136">If all the left-side element values are equal to or greater than the corresponding right-side elements and the left-side array has the same or more elements than the right-side array, 'greater than' returns true.</span></span> |
| <           | <span data-ttu-id="d3058-137">'Inférieur à’retourne la valeur true lorsque la valeur de chaque élément de gauche est inférieure à la valeur de l’élément de droite correspondant.</span><span class="sxs-lookup"><span data-stu-id="d3058-137">'Less than' returns true when the value of each left-side element is less than the value of the corresponding right-side element.</span></span> <span data-ttu-id="d3058-138">'Inférieur à’retourne également true lorsque le côté gauche a moins d’éléments que le côté droit.</span><span class="sxs-lookup"><span data-stu-id="d3058-138">'Less than' also returns true when the left-side side has fewer elements than the right-side side.</span></span>                                                                                                                                                  |
| <=          | <span data-ttu-id="d3058-139">'Inférieur ou égal à’retourne la valeur true lorsque la valeur de chaque élément de gauche est inférieure ou égale à la valeur de l’élément de droite correspondant.</span><span class="sxs-lookup"><span data-stu-id="d3058-139">'Less than or equal to' returns true when the value of every left-side element is less than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="d3058-140">Si toutes les valeurs d’élément de gauche sont égales ou inférieures aux éléments de droite correspondants et que le tableau de gauche a le même ou un moins grand nombre d’éléments que le tableau de droite, 'supérieur à’retourne la valeur true.</span><span class="sxs-lookup"><span data-stu-id="d3058-140">If all the left-side element values are equal to or less than the corresponding right-side elements and the left-side array has the same or fewer elements than the right-side array, 'greater than' returns true.</span></span>         |



 

## <a name="all-quantifier"></a><span data-ttu-id="d3058-141">TOUT quantificateur</span><span class="sxs-lookup"><span data-stu-id="d3058-141">ALL Quantifier</span></span>

<span data-ttu-id="d3058-142">Le quantificateur ALL spécifie que chaque élément du côté gauche est comparé à chaque élément situé à droite.</span><span class="sxs-lookup"><span data-stu-id="d3058-142">The ALL quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="d3058-143">Pour retourner true, la comparaison doit avoir la valeur true pour chaque élément du côté gauche par rapport à chaque élément situé à droite.</span><span class="sxs-lookup"><span data-stu-id="d3058-143">To return true, the comparison must be true for each element on the left side when compared to every element on the right side.</span></span> <span data-ttu-id="d3058-144">Le nombre d’éléments dans les côtés gauche et droit n’a aucun effet sur le résultat.</span><span class="sxs-lookup"><span data-stu-id="d3058-144">The number of elements in the left and right array sides has no effect on the result.</span></span>

<span data-ttu-id="d3058-145">Le tableau suivant montre comment chaque opérateur de comparaison fonctionne avec le quantificateur ALL.</span><span class="sxs-lookup"><span data-stu-id="d3058-145">The following table shows how each comparison operator functions with the ALL quantifier.</span></span>



| <span data-ttu-id="d3058-146">Opérateur</span><span class="sxs-lookup"><span data-stu-id="d3058-146">Operator</span></span>       | <span data-ttu-id="d3058-147">Description</span><span class="sxs-lookup"><span data-stu-id="d3058-147">Description</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="d3058-148">« Égal à » retourne la valeur true lorsque chaque valeur d’élément de gauche est la même que chaque valeur d’élément côté droit.</span><span class="sxs-lookup"><span data-stu-id="d3058-148">'Equal to' returns true when each left-side element value is the same as every right-side element value.</span></span>                              |
| <span data-ttu-id="d3058-149">! = ou <></span><span class="sxs-lookup"><span data-stu-id="d3058-149">!= or <></span></span> | <span data-ttu-id="d3058-150">'Différent de’retourne la valeur true lorsqu’au moins une des valeurs d’élément côté gauche est différente de l’une des valeurs d’élément côté droit.</span><span class="sxs-lookup"><span data-stu-id="d3058-150">'Not equal to' returns true when at least one of the left-side element values is different from any of the right-side element values.</span></span> |
| >           | <span data-ttu-id="d3058-151">« Supérieur à » retourne la valeur true lorsque chaque valeur d’élément de gauche est supérieure à chaque valeur d’élément de droite.</span><span class="sxs-lookup"><span data-stu-id="d3058-151">'Greater than' returns true when each left-side element value is greater than every right-side element value.</span></span>                         |
| >=          | <span data-ttu-id="d3058-152">'Supérieur ou égal à’retourne la valeur true lorsque chaque valeur d’élément de gauche est supérieure ou égale à chaque valeur d’élément de droite.</span><span class="sxs-lookup"><span data-stu-id="d3058-152">'Greater than or equal to' returns true when each left-side element value is greater than or equal to every right-side element value.</span></span> |
| <           | <span data-ttu-id="d3058-153">'Inférieur à’retourne la valeur true lorsque chaque valeur d’élément de gauche est inférieure à toutes les valeurs d’élément côté droit.</span><span class="sxs-lookup"><span data-stu-id="d3058-153">'Less than' returns true when each left-side element value is less than every right-side element value.</span></span>                               |
| <=          | <span data-ttu-id="d3058-154">'Inférieur ou égal à’retourne la valeur true lorsque chaque valeur d’élément de gauche est inférieure ou égale à chaque valeur d’élément de droite.</span><span class="sxs-lookup"><span data-stu-id="d3058-154">'Less than or equal to' returns true when each left-side element value is less than or equal to every right-side element value.</span></span>       |



 

## <a name="some-or-any-quantifier"></a><span data-ttu-id="d3058-155">TOUT (ou un) quantificateur</span><span class="sxs-lookup"><span data-stu-id="d3058-155">SOME (or ANY) Quantifier</span></span>

<span data-ttu-id="d3058-156">Le quantificateur et le quantificateur ANY peuvent être utilisés indifféremment.</span><span class="sxs-lookup"><span data-stu-id="d3058-156">The SOME quantifier and the ANY quantifier can be used interchangeably.</span></span> <span data-ttu-id="d3058-157">À l’instar du quantificateur ALL, le quantificateur SOME spécifie que chaque élément du côté gauche est comparé à chaque élément du côté droit.</span><span class="sxs-lookup"><span data-stu-id="d3058-157">Like the ALL quantifier, the SOME quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="d3058-158">Pour retourner true, la comparaison doit avoir la valeur true pour au moins l’un des éléments du côté gauche par rapport à tout élément situé à droite.</span><span class="sxs-lookup"><span data-stu-id="d3058-158">To return true, the comparison must be true for at least one of the elements on the left side when compared to any element on the right side.</span></span> <span data-ttu-id="d3058-159">Le nombre d’éléments sur les tableaux à gauche et à droite n’a aucun effet sur le résultat.</span><span class="sxs-lookup"><span data-stu-id="d3058-159">The number of elements on the left and right side arrays has no effect on the result.</span></span>

<span data-ttu-id="d3058-160">Le tableau suivant montre comment chaque opérateur de comparaison fonctionne avec le quantificateur SOME.</span><span class="sxs-lookup"><span data-stu-id="d3058-160">The following table shows how each comparison operator functions with the SOME quantifier.</span></span>



| <span data-ttu-id="d3058-161">Opérateur</span><span class="sxs-lookup"><span data-stu-id="d3058-161">Operator</span></span>       | <span data-ttu-id="d3058-162">Description</span><span class="sxs-lookup"><span data-stu-id="d3058-162">Description</span></span>                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="d3058-163">'Égal à’retourne la valeur true lorsqu’au moins une des valeurs d’élément côté gauche est identique à l’une des valeurs d’élément côté droit.</span><span class="sxs-lookup"><span data-stu-id="d3058-163">'Equal to' returns true when at least one of the left-side element values is the same as any of the right-side element values.</span></span>                                  |
| <span data-ttu-id="d3058-164">! = ou <></span><span class="sxs-lookup"><span data-stu-id="d3058-164">!= or <></span></span> | <span data-ttu-id="d3058-165">'Différent de’retourne la valeur true si aucune des valeurs de l’élément de gauche n’est identique à l’une des valeurs d’élément côté droit.</span><span class="sxs-lookup"><span data-stu-id="d3058-165">'Not equal to' returns true when none of the left-side element values is the same as any of the right-side element values.</span></span>                                      |
| >           | <span data-ttu-id="d3058-166">« Supérieur à » retourne la valeur true lorsqu’au moins une des valeurs d’élément côté gauche est supérieure à l’une des valeurs d’élément côté droit.</span><span class="sxs-lookup"><span data-stu-id="d3058-166">'Greater than' returns true when at least one of the left-side element values is greater than any one of the right-side element values.</span></span>                         |
| >=          | <span data-ttu-id="d3058-167">'Supérieur ou égal à’retourne la valeur true lorsqu’au moins une des valeurs d’élément côté gauche est supérieure ou égale à l’une des valeurs d’élément côté droit.</span><span class="sxs-lookup"><span data-stu-id="d3058-167">'Greater than or equal to' returns true when at least one of the left-side element values is greater than or equal to any one of the right-side element values.</span></span> |
| <           | <span data-ttu-id="d3058-168">'Inférieur à’retourne la valeur true lorsqu’au moins une des valeurs d’élément côté gauche est inférieure à l’une des valeurs d’élément côté droit.</span><span class="sxs-lookup"><span data-stu-id="d3058-168">'Less than' returns true when at least one of the left-side element values is less than any one of the right-side element values.</span></span>                               |
| <=          | <span data-ttu-id="d3058-169">'Inférieur ou égal à’retourne la valeur true lorsqu’au moins une des valeurs d’élément côté gauche est inférieure ou égale à l’une des valeurs d’élément de droite.</span><span class="sxs-lookup"><span data-stu-id="d3058-169">'Less than or equal to' returns true when at least one of the left-side element values is less than or equal to any one of the right-side element values.</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="d3058-170">Exemples</span><span class="sxs-lookup"><span data-stu-id="d3058-170">Examples</span></span>

<span data-ttu-id="d3058-171">L’exemple suivant vérifie si les documents sont dans les catégories « finance » ou « Planning » :</span><span class="sxs-lookup"><span data-stu-id="d3058-171">The following example checks whether documents are in the "Finance" or "Planning" categories:</span></span>


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



<span data-ttu-id="d3058-172">Les comparaisons suivantes évaluent toutes la valeur true.</span><span class="sxs-lookup"><span data-stu-id="d3058-172">The following comparisons all evaluate true.</span></span> <span data-ttu-id="d3058-173">N’oubliez pas que, dans l’utilisation réelle, la syntaxe de requête de recherche requiert que le côté gauche soit une propriété, et non une valeur littérale.</span><span class="sxs-lookup"><span data-stu-id="d3058-173">Remember that in actual use, the search query syntax requires the left side to be a property, not a literal value.</span></span>


```
ARRAY [1,2] > ARRAY [1,1]
ARRAY [1,2] > ARRAY [1,1,2]
ARRAY [1,2] < ARRAY [1,2,3]
ARRAY [1,2] = SOME ARRAY [1,12,27,35,2]
ARRAY [1,1] != ALL ARRAY [1,2]
ARRAY [1,20,21,22] < SOME ARRAY [0,40]
ARRAY [1,20,21,22] < ANY ARRAY [0,40]
```



## <a name="related-topics"></a><span data-ttu-id="d3058-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3058-174">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d3058-175">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="d3058-175">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d3058-176">Prédicat LIKE</span><span class="sxs-lookup"><span data-stu-id="d3058-176">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="d3058-177">Comparaison de valeurs littérales</span><span class="sxs-lookup"><span data-stu-id="d3058-177">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="d3058-178">Prédicat NULL</span><span class="sxs-lookup"><span data-stu-id="d3058-178">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="d3058-179">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="d3058-179">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d3058-180">Prédicats de texte intégral</span><span class="sxs-lookup"><span data-stu-id="d3058-180">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="d3058-181">Prédicats de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="d3058-181">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



