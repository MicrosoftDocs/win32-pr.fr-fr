---
description: 'En savoir plus sur : clause ORDER BY'
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: Clause ORDER BY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eaa3c834ca2fe04222ef2ae452a0119bf391b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112419"
---
# <a name="order-by-clause"></a><span data-ttu-id="5627e-103">Clause ORDER BY</span><span class="sxs-lookup"><span data-stu-id="5627e-103">ORDER BY Clause</span></span>

<span data-ttu-id="5627e-104">La clause ORDER BY trie les résultats en fonction de la valeur d’une ou plusieurs colonnes que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="5627e-104">The ORDER BY clause sorts the results based on the value of one or more columns you specify.</span></span> <span data-ttu-id="5627e-105">Voici la syntaxe de la clause ORDER BY :</span><span class="sxs-lookup"><span data-stu-id="5627e-105">Following is the syntax of the ORDER BY clause:</span></span>


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



<span data-ttu-id="5627e-106">Le spécificateur de colonne doit être une colonne valide.</span><span class="sxs-lookup"><span data-stu-id="5627e-106">The column specifier must be a valid column.</span></span> <span data-ttu-id="5627e-107">Vous pouvez utiliser le spécificateur de colonne pour faire référence aux colonnes dans l’ordre dans lequel elles apparaissent dans la requête.</span><span class="sxs-lookup"><span data-stu-id="5627e-107">You can use the column specifier to refer to columns by the order that they appear in the query.</span></span> <span data-ttu-id="5627e-108">La première colonne de la requête est numérotée 1.</span><span class="sxs-lookup"><span data-stu-id="5627e-108">The first column in the query is numbered 1.</span></span> <span data-ttu-id="5627e-109">Vous pouvez inclure plusieurs colonnes dans la clause ORDER BY, séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="5627e-109">You can include more than one column in the ORDER BY clause, separated by commas.</span></span>

<span data-ttu-id="5627e-110">Le spécificateur de direction facultatif peut être « ASC » pour l’ordre croissant (de faible à élevé) ou « DESC » pour l’ordre décroissant (de haut en bas).</span><span class="sxs-lookup"><span data-stu-id="5627e-110">The optional direction specifier can be either "ASC" for ascending (low to high) or "DESC" for descending (high to low).</span></span> <span data-ttu-id="5627e-111">Si vous ne fournissez pas de spécificateur de direction, la valeur par défaut, par ordre croissant, est utilisée.</span><span class="sxs-lookup"><span data-stu-id="5627e-111">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="5627e-112">Si vous spécifiez plusieurs colonnes, mais que vous ne spécifiez pas toutes les directions, la direction que vous spécifiez en dernier est appliquée à chaque colonne jusqu’à ce que vous modifiiez explicitement la direction.</span><span class="sxs-lookup"><span data-stu-id="5627e-112">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each column until you explicitly change the direction.</span></span>

<span data-ttu-id="5627e-113">Par exemple, dans la clause ORDER BY suivante, les colonnes A, B, C et G sont triées dans l’ordre croissant, tandis que les colonnes D, E et F sont triées dans l’ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="5627e-113">For example, in the following ORDER BY clause, the columns A, B, C, and G are sorted in ascending order, while columns D, E, and F are sorted in descending order.</span></span>


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a><span data-ttu-id="5627e-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5627e-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5627e-115">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="5627e-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5627e-116">FROM, clause</span><span class="sxs-lookup"><span data-stu-id="5627e-116">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="5627e-117">RANK BY, clause</span><span class="sxs-lookup"><span data-stu-id="5627e-117">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

[<span data-ttu-id="5627e-118">Instruction SELECT</span><span class="sxs-lookup"><span data-stu-id="5627e-118">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

<span data-ttu-id="5627e-119">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5627e-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5627e-120">Prédicats de texte intégral</span><span class="sxs-lookup"><span data-stu-id="5627e-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="5627e-121">Prédicats de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="5627e-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



