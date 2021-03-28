---
description: Une application combine deux régions en appelant la fonction CombineRgn.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Combinaison de régions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51db22daea448acfb02120844ca2859a5ba11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570784"
---
# <a name="combining-regions"></a><span data-ttu-id="c10a9-103">Combinaison de régions</span><span class="sxs-lookup"><span data-stu-id="c10a9-103">Combining Regions</span></span>

<span data-ttu-id="c10a9-104">Une application combine deux régions en appelant la fonction [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) .</span><span class="sxs-lookup"><span data-stu-id="c10a9-104">An application combines two regions by calling the [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) function.</span></span> <span data-ttu-id="c10a9-105">À l’aide de cette fonction, une application peut combiner les parties qui se croisent de deux régions, toutes les parties à l’exception de celles de deux régions, les deux régions d’origine dans leur intégralité, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="c10a9-105">Using this function, an application can combine the intersecting parts of two regions, all but the intersecting parts of two regions, the two original regions in their entirety, and so on.</span></span> <span data-ttu-id="c10a9-106">Vous trouverez ci-dessous cinq valeurs qui définissent les combinaisons de régions.</span><span class="sxs-lookup"><span data-stu-id="c10a9-106">Following are five values that define the region combinations.</span></span>



| <span data-ttu-id="c10a9-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="c10a9-107">Value</span></span>     | <span data-ttu-id="c10a9-108">Signification</span><span class="sxs-lookup"><span data-stu-id="c10a9-108">Meaning</span></span>                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c10a9-109">RGN \_ et</span><span class="sxs-lookup"><span data-stu-id="c10a9-109">RGN\_AND</span></span>  | <span data-ttu-id="c10a9-110">Les parties qui se croisent de deux régions d’origine définissent une nouvelle région.</span><span class="sxs-lookup"><span data-stu-id="c10a9-110">The intersecting parts of two original regions define a new region.</span></span>                   |
| <span data-ttu-id="c10a9-111">\_copie RGN</span><span class="sxs-lookup"><span data-stu-id="c10a9-111">RGN\_COPY</span></span> | <span data-ttu-id="c10a9-112">Une copie de la première (des deux régions d’origine) définit une nouvelle région.</span><span class="sxs-lookup"><span data-stu-id="c10a9-112">A copy of the first (of the two original regions) defines a new region.</span></span>               |
| <span data-ttu-id="c10a9-113">\_diff RGN</span><span class="sxs-lookup"><span data-stu-id="c10a9-113">RGN\_DIFF</span></span> | <span data-ttu-id="c10a9-114">La partie de la première région qui ne croise pas la seconde définit une nouvelle région.</span><span class="sxs-lookup"><span data-stu-id="c10a9-114">The part of the first region that does not intersect the second defines a new region.</span></span> |
| <span data-ttu-id="c10a9-115">RGN \_ ou</span><span class="sxs-lookup"><span data-stu-id="c10a9-115">RGN\_OR</span></span>   | <span data-ttu-id="c10a9-116">Les deux régions d’origine définissent une nouvelle région.</span><span class="sxs-lookup"><span data-stu-id="c10a9-116">The two original regions define a new region.</span></span>                                         |
| <span data-ttu-id="c10a9-117">RGN \_ Xor</span><span class="sxs-lookup"><span data-stu-id="c10a9-117">RGN\_XOR</span></span>  | <span data-ttu-id="c10a9-118">Les parties des deux régions d’origine qui ne se chevauchent pas définissent une nouvelle région.</span><span class="sxs-lookup"><span data-stu-id="c10a9-118">Those parts of the two original regions that do not overlap define a new region.</span></span>      |



 

<span data-ttu-id="c10a9-119">L’illustration suivante montre les cinq combinaisons possibles d’un carré et d’une région circulaire résultant d’un appel à [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).</span><span class="sxs-lookup"><span data-stu-id="c10a9-119">The following illustration shows the five possible combinations of a square and a circular region resulting from a call to [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).</span></span>

![illustration illustrant les résultats décrits dans le tableau précédent](images/csrgn-02.png)

 

 



