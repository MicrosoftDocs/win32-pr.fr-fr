---
description: Le prédicat NULL indique si le document a une valeur pour la colonne indiquée.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Prédicat NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea02a04313ac2b86afe809633bee5ad2cbcf764e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544623"
---
# <a name="null-predicate"></a><span data-ttu-id="75fdc-103">Prédicat NULL</span><span class="sxs-lookup"><span data-stu-id="75fdc-103">NULL Predicate</span></span>

<span data-ttu-id="75fdc-104">Le prédicat **null** indique si le document a une valeur pour la colonne indiquée.</span><span class="sxs-lookup"><span data-stu-id="75fdc-104">The **NULL** predicate indicates whether the document has a value for the indicated column.</span></span>

<span data-ttu-id="75fdc-105">Le prédicat **null** a la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="75fdc-105">The **NULL** predicate has the following syntax:</span></span>


```
...WHERE <column> IS [NOT] NULL
```



<span data-ttu-id="75fdc-106">Le mot clé NOT facultatif inverse le résultat.</span><span class="sxs-lookup"><span data-stu-id="75fdc-106">The optional NOT keyword negates the result.</span></span> <span data-ttu-id="75fdc-107">La colonne peut être un [identificateur](-search-sql-identifiers.md)standard ou délimité.</span><span class="sxs-lookup"><span data-stu-id="75fdc-107">The column can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75fdc-108">Pour déterminer si une colonne a la valeur **null** , vous devez utiliser le prédicat **null** .</span><span class="sxs-lookup"><span data-stu-id="75fdc-108">To test whether a column has the **NULL** value, you must use the **NULL** predicate.</span></span> <span data-ttu-id="75fdc-109">L’utilisation de la valeur **null** dans un prédicat de comparaison n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="75fdc-109">It is not valid to use the **NULL** value in a comparison predicate.</span></span> <span data-ttu-id="75fdc-110">« WHERE Column IS **null**» est correct.</span><span class="sxs-lookup"><span data-stu-id="75fdc-110">"WHERE column IS **NULL**" is correct.</span></span> <span data-ttu-id="75fdc-111">« WHERE column = **null**» n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="75fdc-111">"WHERE column = **NULL**" is not valid.</span></span>

 

## <a name="example"></a><span data-ttu-id="75fdc-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="75fdc-112">Example</span></span>

<span data-ttu-id="75fdc-113">L’exemple suivant retourne des documents qui n’ont pas de valeur System. Video. Director.</span><span class="sxs-lookup"><span data-stu-id="75fdc-113">The following example returns documents that do not have a System.Video.Director value.</span></span>


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a><span data-ttu-id="75fdc-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75fdc-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="75fdc-115">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="75fdc-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="75fdc-116">Prédicat LIKE</span><span class="sxs-lookup"><span data-stu-id="75fdc-116">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="75fdc-117">Comparaison de valeurs littérales</span><span class="sxs-lookup"><span data-stu-id="75fdc-117">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="75fdc-118">Comparaisons à valeurs multiples (tableau)</span><span class="sxs-lookup"><span data-stu-id="75fdc-118">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="75fdc-119">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="75fdc-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="75fdc-120">Prédicats de texte intégral</span><span class="sxs-lookup"><span data-stu-id="75fdc-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="75fdc-121">Prédicats de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="75fdc-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



