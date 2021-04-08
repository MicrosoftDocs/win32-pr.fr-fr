---
description: Pour obtenir un niveau de confiance pour chaque résultat de reconnaissance, vous pouvez obtenir la propriété Confidence de l’objet RecognitionAlternate ou la propriété Confidence de l’objet geste.
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: Propriété confidence [à propos de la reconnaissance]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f436d17d5cb83901c7d19ef4beb6dfb7ce6199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861917"
---
# <a name="confidence-property-about-recognition"></a><span data-ttu-id="67d6d-103">Propriété \[ de confiance sur la reconnaissance\]</span><span class="sxs-lookup"><span data-stu-id="67d6d-103">Confidence Property \[About Recognition\]</span></span>

<span data-ttu-id="67d6d-104">Pour obtenir un niveau de confiance pour chaque résultat de reconnaissance, vous pouvez obtenir la propriété [**confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) de l’objet [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) ou la propriété [**confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) de l’objet [**geste**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) .</span><span class="sxs-lookup"><span data-stu-id="67d6d-104">To obtain a level of confidence for each recognition result, you can get either the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) property of the [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object or the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) property of the [**Gesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object.</span></span> <span data-ttu-id="67d6d-105">Le niveau de confiance est un nombre qui indique le degré de confiance de chaque autre résultat de reconnaissance que le module de reconnaissance renvoie pour un segment de reconnaissance correspondant.</span><span class="sxs-lookup"><span data-stu-id="67d6d-105">The confidence level is a number that indicates the degree of confidence for each alternate recognition result that the recognizer returns for a corresponding recognition segment.</span></span>

<span data-ttu-id="67d6d-106">La confiance est retournée comme faible, moyenne ou élevée.</span><span class="sxs-lookup"><span data-stu-id="67d6d-106">Confidence is returned as low, average, or high.</span></span> <span data-ttu-id="67d6d-107">L’application utilise ces résultats pour :</span><span class="sxs-lookup"><span data-stu-id="67d6d-107">The application uses these results to:</span></span>

-   <span data-ttu-id="67d6d-108">Indiquez à l’utilisateur que plusieurs possibilités existent.</span><span class="sxs-lookup"><span data-stu-id="67d6d-108">Indicate to the user that multiple possibilities exist.</span></span>
-   <span data-ttu-id="67d6d-109">Classez les remplacements par niveau de confiance.</span><span class="sxs-lookup"><span data-stu-id="67d6d-109">Rank the alternates by confidence level.</span></span>

## <a name="what-affects-confidence"></a><span data-ttu-id="67d6d-110">Ce qui affecte la confiance</span><span class="sxs-lookup"><span data-stu-id="67d6d-110">What Affects Confidence</span></span>

<span data-ttu-id="67d6d-111">Certains éléments qui rendent la reconnaissance de l’écriture manuscrite difficile et affectent la confiance sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="67d6d-111">Some of the things that make handwriting recognition difficult and affect confidence include:</span></span>

-   <span data-ttu-id="67d6d-112">Difficulté à déterminer la segmentation des mots</span><span class="sxs-lookup"><span data-stu-id="67d6d-112">Difficulty determining word segmentation</span></span>

![image indiquant une écriture trop proche](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   <span data-ttu-id="67d6d-114">Difficultés de cas</span><span class="sxs-lookup"><span data-stu-id="67d6d-114">Case difficulties</span></span>

![image présentant des difficultés avec les versions manuscrites du mot « case »](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   <span data-ttu-id="67d6d-116">Styles d’écriture rares</span><span class="sxs-lookup"><span data-stu-id="67d6d-116">Uncommon writing styles</span></span>
-   <span data-ttu-id="67d6d-117">Ponctuation isolée</span><span class="sxs-lookup"><span data-stu-id="67d6d-117">Isolated punctuation</span></span>

![image indiquant des guillemets trop éloignés du texte](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   <span data-ttu-id="67d6d-119">Caractères accentués en anglais</span><span class="sxs-lookup"><span data-stu-id="67d6d-119">Accented characters in English recognizers</span></span>

> [!Note]  
> <span data-ttu-id="67d6d-120">L’évaluation de la confiance est disponible uniquement pour États-Unis anglais et tous les module de reconnaissance de mouvement dans cette version.</span><span class="sxs-lookup"><span data-stu-id="67d6d-120">Confidence evaluation is available only for United States English and all gesture recognizers in this release.</span></span> <span data-ttu-id="67d6d-121">Les méthodes qui fournissent la propriété confidence pour tout autre module de reconnaissance retournent **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="67d6d-121">Methods that provide the confidence property for any other recognizer will return **E\_NOTIMPL**.</span></span>

 

 

 



