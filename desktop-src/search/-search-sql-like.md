---
description: Le prédicat LIKE effectue une comparaison de critères spéciaux sur la colonne spécifiée.
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: Prédicat LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba042fb2fe3005e062e7961a048a81a64c0c144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516426"
---
# <a name="like-predicate"></a><span data-ttu-id="f3404-103">Prédicat LIKE</span><span class="sxs-lookup"><span data-stu-id="f3404-103">LIKE Predicate</span></span>

<span data-ttu-id="f3404-104">Le prédicat LIKE effectue une comparaison de critères spéciaux sur la colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f3404-104">The LIKE predicate performs pattern-matching comparison on the specified column.</span></span> <span data-ttu-id="f3404-105">Il utilise la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f3404-105">It uses the following syntax:</span></span>


```
...WHERE <column> LIKE '<wildcard_literal>'
```



<span data-ttu-id="f3404-106"><column>Peut être un [identificateur](-search-sql-identifiers.md)standard ou délimité.</span><span class="sxs-lookup"><span data-stu-id="f3404-106">The <column> can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span> <span data-ttu-id="f3404-107">La colonne est limitée aux propriétés dans la Banque de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f3404-107">The column is limited to the properties in the property store.</span></span>

<span data-ttu-id="f3404-108">Le <littéral de caractère générique \_> est un littéral de chaîne.</span><span class="sxs-lookup"><span data-stu-id="f3404-108">The <wildcard\_literal> is a string literal.</span></span> <span data-ttu-id="f3404-109">Elle est placée entre guillemets et peut éventuellement contenir des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="f3404-109">It is enclosed in quotation marks and optionally can contain wildcard characters.</span></span> <span data-ttu-id="f3404-110">La chaîne de correspondance peut contenir plusieurs caractères génériques si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f3404-110">The match string can contain multiple wildcard characters if needed.</span></span> <span data-ttu-id="f3404-111">Le tableau suivant décrit les caractères génériques reconnus par le prédicat LIKE.</span><span class="sxs-lookup"><span data-stu-id="f3404-111">The following table describes the wildcard characters that the LIKE predicate recognizes.</span></span>



| <span data-ttu-id="f3404-112">Caractère générique</span><span class="sxs-lookup"><span data-stu-id="f3404-112">Wildcard</span></span>                | <span data-ttu-id="f3404-113">Description</span><span class="sxs-lookup"><span data-stu-id="f3404-113">Description</span></span>                                                                                                                                                                                     | <span data-ttu-id="f3404-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="f3404-114">Example</span></span>                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3404-115">% (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="f3404-115">% (percent)</span></span>             | <span data-ttu-id="f3404-116">Représente zéro, un ou plusieurs caractères.</span><span class="sxs-lookup"><span data-stu-id="f3404-116">Matches zero or more of any characters.</span></span>                                                                                                                                                         | <span data-ttu-id="f3404-117">« COMP% r » correspond à « COMP » suivi de zéro, un ou plusieurs caractères, se terminant par r.</span><span class="sxs-lookup"><span data-stu-id="f3404-117">'comp%r' matches 'comp' followed by zero or more of any characters, ending in an r.</span></span>                                                                                                                                  |
| <span data-ttu-id="f3404-118">\_ (trait de soulignement)</span><span class="sxs-lookup"><span data-stu-id="f3404-118">\_ (underscore)</span></span>         | <span data-ttu-id="f3404-119">Représente n'importe quel caractère unique.</span><span class="sxs-lookup"><span data-stu-id="f3404-119">Matches any single character.</span></span>                                                                                                                                                                   | <span data-ttu-id="f3404-120">« COMP \_ RET » correspond à « COMP » suivi de exactement un caractère quelconque, suivi de « ter ».</span><span class="sxs-lookup"><span data-stu-id="f3404-120">'comp\_ter' matches 'comp' followed by exactly one of any character, followed by 'ter'.</span></span>                                                                                                                              |
| <span data-ttu-id="f3404-121">\[\](crochets)</span><span class="sxs-lookup"><span data-stu-id="f3404-121">\[ \] (square brackets)</span></span> | <span data-ttu-id="f3404-122">Correspond à n’importe quel caractère unique dans la plage ou l’ensemble spécifié.</span><span class="sxs-lookup"><span data-stu-id="f3404-122">Matches any single character within the specified range or set.</span></span> <span data-ttu-id="f3404-123">Par exemple, \[ a-z \] spécifie une plage ; \[ AEIOU \] spécifie le jeu de voyelles.</span><span class="sxs-lookup"><span data-stu-id="f3404-123">For example, \[a-z\] specifies a range; \[aeiou\] specifies the set of vowels.</span></span>                                                  | <span data-ttu-id="f3404-124">« COMP \[ a-z \] re » correspond à « COMP » suivi d’un caractère unique dans la plage de a à z, suivi de « is ».</span><span class="sxs-lookup"><span data-stu-id="f3404-124">'comp\[a-z\]re' matches 'comp' followed by a single character in the range of a through z, followed by 're'.</span></span> <span data-ttu-id="f3404-125">« COMP \[ AO \] » correspond à « COMP » suivi d’un caractère unique qui doit être un ou un o.</span><span class="sxs-lookup"><span data-stu-id="f3404-125">'comp\[ao\]' matches 'comp' followed by a single character that must be either an a or an o.</span></span><br/> |
| <span data-ttu-id="f3404-126">\[^ \] signe insertion</span><span class="sxs-lookup"><span data-stu-id="f3404-126">\[^ \] (caret)</span></span>          | <span data-ttu-id="f3404-127">Correspond à n’importe quel caractère unique qui ne se trouve pas dans la plage ou l’ensemble spécifié.</span><span class="sxs-lookup"><span data-stu-id="f3404-127">Matches any single character that is not within the specified range or set.</span></span> <span data-ttu-id="f3404-128">Par exemple, \[ ^ a-z \] spécifie une plage qui exclut de a à z ; \[ ^ AEIOU \] spécifie un jeu qui exclut les voyelles.</span><span class="sxs-lookup"><span data-stu-id="f3404-128">For example, \[^a-z\] specifies a range that excludes a through z; \[^aeiou\] specifies a set that excludes vowels.</span></span> | <span data-ttu-id="f3404-129">« COMP \[ ^ u \] » correspond à « COMP » suivi d’un caractère unique qui n’est pas un u.</span><span class="sxs-lookup"><span data-stu-id="f3404-129">'comp\[^u\]' matches 'comp' followed by any single character that is not a u.</span></span>                                                                                                                                        |



 

<span data-ttu-id="f3404-130">Si vous créez des prédicats avec plusieurs plages, les plages doivent être dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="f3404-130">If you create predicates with multiple ranges, the ranges must be in order.</span></span>

> [!Note]  
> <span data-ttu-id="f3404-131">Pour mettre en correspondance les caractères génériques comme des caractères littéraux pour la correspondance et non comme des caractères génériques, placez le caractère entre crochets.</span><span class="sxs-lookup"><span data-stu-id="f3404-131">To match the wildcard characters as literal characters for matching and not as wildcard characters, place the character inside square brackets.</span></span> <span data-ttu-id="f3404-132">Par exemple, pour faire correspondre le signe de pourcentage, utilisez' \[ % \] '</span><span class="sxs-lookup"><span data-stu-id="f3404-132">For example, to match the percent sign, use '\[%\]'</span></span>

 

## <a name="examples"></a><span data-ttu-id="f3404-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="f3404-133">Examples</span></span>


```
...WHERE System.ItemNameDisplay LIKE 'financ%'
```



## <a name="related-topics"></a><span data-ttu-id="f3404-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3404-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f3404-135">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="f3404-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f3404-136">Comparaison de valeurs littérales</span><span class="sxs-lookup"><span data-stu-id="f3404-136">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="f3404-137">Comparaisons à valeurs multiples (tableau)</span><span class="sxs-lookup"><span data-stu-id="f3404-137">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="f3404-138">Prédicat NULL</span><span class="sxs-lookup"><span data-stu-id="f3404-138">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="f3404-139">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f3404-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f3404-140">Prédicats de texte intégral</span><span class="sxs-lookup"><span data-stu-id="f3404-140">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="f3404-141">Prédicats de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="f3404-141">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




