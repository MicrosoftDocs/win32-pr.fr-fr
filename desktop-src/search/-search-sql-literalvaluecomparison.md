---
description: La comparaison de valeurs littérales utilise des opérateurs de comparaison standard pour faire correspondre une colonne à valeur unique à une valeur littérale.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Comparaison de valeurs littérales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8577e5a97dcc92131658c325f175efa1d0c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514586"
---
# <a name="literal-value-comparison"></a><span data-ttu-id="e0b16-103">Comparaison de valeurs littérales</span><span class="sxs-lookup"><span data-stu-id="e0b16-103">Literal Value Comparison</span></span>

<span data-ttu-id="e0b16-104">La comparaison de valeurs littérales utilise des opérateurs de comparaison standard pour faire correspondre une colonne à valeur unique à une valeur [littérale](-search-sql-literals.md) .</span><span class="sxs-lookup"><span data-stu-id="e0b16-104">The literal value comparison uses standard comparison operators for matching a single-valued column to a [literal](-search-sql-literals.md) value.</span></span> <span data-ttu-id="e0b16-105">Pour plus d’informations sur la comparaison de colonnes à valeurs multiples, consultez [comparaisons à valeurs multiples (tableau)](-search-sql-multivaluedcomparisons.md).</span><span class="sxs-lookup"><span data-stu-id="e0b16-105">For information about comparing multivalued columns, see [Multi-Valued (ARRAY) Comparisons](-search-sql-multivaluedcomparisons.md).</span></span>

<span data-ttu-id="e0b16-106">Le prédicat de comparaison de valeur littérale a la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="e0b16-106">The literal value comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> <span data-ttu-id="e0b16-107">La partie droite de la comparaison doit être un littéral.</span><span class="sxs-lookup"><span data-stu-id="e0b16-107">The right side of the comparison must be a literal.</span></span> <span data-ttu-id="e0b16-108">Vous ne pouvez pas comparer une colonne à une valeur calculée et vous ne pouvez pas comparer une colonne à une autre colonne.</span><span class="sxs-lookup"><span data-stu-id="e0b16-108">You cannot compare a column against a computed value, and you cannot compare a column against another column.</span></span>

 

<span data-ttu-id="e0b16-109">La partie colonne est une colonne de propriété valide et peut être convertie en un autre type si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e0b16-109">The column part is any valid property column and can be cast to another type if necessary.</span></span> <span data-ttu-id="e0b16-110">Si vous le souhaitez, vous pouvez placer le nom de colonne entre guillemets doubles pour une meilleure lisibilité sans affecter les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="e0b16-110">Optionally, you can enclose the column name in double quotes for readability without affecting functionality.</span></span> <span data-ttu-id="e0b16-111">Pour plus d’informations, consultez [cast du type de données d’une colonne](-search-sql-castingdatacolumntype.md).</span><span class="sxs-lookup"><span data-stu-id="e0b16-111">For more information, see [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

<span data-ttu-id="e0b16-112">Le littéral peut être n’importe quel littéral de chaîne, numérique, hexadécimal, booléen ou de date, placé entre guillemets simples.</span><span class="sxs-lookup"><span data-stu-id="e0b16-112">The literal can be any string, numeric, hexadecimal, Boolean, or date literal, enclosed in single quotation marks.</span></span> <span data-ttu-id="e0b16-113">Seules les correspondances exactes sont reconnues, et les caractères génériques sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="e0b16-113">Only exact matches are recognized, and wildcard characters are ignored.</span></span> <span data-ttu-id="e0b16-114">Le littéral peut également être converti en un autre type.</span><span class="sxs-lookup"><span data-stu-id="e0b16-114">The literal can also be cast to another type.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="e0b16-115">Opérateurs de comparaison</span><span class="sxs-lookup"><span data-stu-id="e0b16-115">Comparison Operators</span></span>

<span data-ttu-id="e0b16-116">Le tableau suivant décrit les opérateurs de comparaison pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e0b16-116">The following table describes the supported comparison operators.</span></span>



| <span data-ttu-id="e0b16-117">Opérateur de comparaison</span><span class="sxs-lookup"><span data-stu-id="e0b16-117">Comparison operator</span></span> | <span data-ttu-id="e0b16-118">Description</span><span class="sxs-lookup"><span data-stu-id="e0b16-118">Description</span></span>              |
|---------------------|--------------------------|
| =                   | <span data-ttu-id="e0b16-119">Égal à</span><span class="sxs-lookup"><span data-stu-id="e0b16-119">Equal to</span></span>                 |
| <span data-ttu-id="e0b16-120">! = ou <></span><span class="sxs-lookup"><span data-stu-id="e0b16-120">!= or <></span></span>      | <span data-ttu-id="e0b16-121">Différent de</span><span class="sxs-lookup"><span data-stu-id="e0b16-121">Not equal to</span></span>             |
| >                | <span data-ttu-id="e0b16-122">Supérieur à</span><span class="sxs-lookup"><span data-stu-id="e0b16-122">Greater than</span></span>             |
| >=               | <span data-ttu-id="e0b16-123">Supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="e0b16-123">Greater than or equal to</span></span> |
| <                | <span data-ttu-id="e0b16-124">Inférieur à</span><span class="sxs-lookup"><span data-stu-id="e0b16-124">Less than</span></span>                |
| <=               | <span data-ttu-id="e0b16-125">Inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="e0b16-125">Less than or equal to</span></span>    |



 

 

<span data-ttu-id="e0b16-126">Conjointement avec l’opérateur « = », la langage SQL de recherche Windows (SQL) prend en charge l’utilisation de mots clés BEFORe et AFTER, qui spécifient si la requête doit comparer des valeurs de colonne avant ou après une valeur spécifiée, dans un ordre de tri du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="e0b16-126">In conjunction with the "=" operator, Windows Search Structured Query Language (SQL) supports the use of BEFORE and AFTER keywords, which specify whether the query should compare column values before or after a specified value, in dictionary sort ordering.</span></span>


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a><span data-ttu-id="e0b16-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="e0b16-127">Examples</span></span>

<span data-ttu-id="e0b16-128">Voici des exemples de prédicats de comparaison de valeurs littérales.</span><span class="sxs-lookup"><span data-stu-id="e0b16-128">The following are examples of the literal value comparison predicate.</span></span>


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a><span data-ttu-id="e0b16-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e0b16-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e0b16-130">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="e0b16-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e0b16-131">Prédicat LIKE</span><span class="sxs-lookup"><span data-stu-id="e0b16-131">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="e0b16-132">DATEADD, fonction</span><span class="sxs-lookup"><span data-stu-id="e0b16-132">DATEADD Function</span></span>](-search-sql-dateadd.md)
</dt> <dt>

[<span data-ttu-id="e0b16-133">Comparaisons à valeurs multiples (tableau)</span><span class="sxs-lookup"><span data-stu-id="e0b16-133">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="e0b16-134">Prédicat NULL</span><span class="sxs-lookup"><span data-stu-id="e0b16-134">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="e0b16-135">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="e0b16-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e0b16-136">Prédicats de texte intégral</span><span class="sxs-lookup"><span data-stu-id="e0b16-136">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="e0b16-137">Prédicats de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="e0b16-137">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



