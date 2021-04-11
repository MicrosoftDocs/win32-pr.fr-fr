---
description: L’attribut mlength spécifie la durée d’un fichier source. Cette valeur doit être la durée réelle ou des erreurs de rendu peuvent se produire.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: Attribut mlength
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eadc288e29d99df0e6af7f06e1404d86f6a938
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103949944"
---
# <a name="mlength-attribute"></a><span data-ttu-id="ed32e-104">Attribut mlength</span><span class="sxs-lookup"><span data-stu-id="ed32e-104">mlength Attribute</span></span>

> [!Note]  
> <span data-ttu-id="ed32e-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="ed32e-105">\[Deprecated.</span></span> <span data-ttu-id="ed32e-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ed32e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ed32e-107">L' `mlength` attribut spécifie la durée d’un fichier source.</span><span class="sxs-lookup"><span data-stu-id="ed32e-107">The `mlength` attribute specifies the duration of a source file.</span></span> <span data-ttu-id="ed32e-108">Cette valeur doit être la durée réelle ou des erreurs de rendu peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="ed32e-108">This value must be the actual duration, or rendering errors may occur.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ed32e-109">S'applique à</span><span class="sxs-lookup"><span data-stu-id="ed32e-109">Applies To</span></span>

[<span data-ttu-id="ed32e-110">**clip**</span><span class="sxs-lookup"><span data-stu-id="ed32e-110">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="ed32e-111">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="ed32e-111">Possible Values</span></span>

<span data-ttu-id="ed32e-112">Doit être une chaîne au format *hh : mm : SS. FF* , où *hh* = heures, *mm* = minutes, *SS* = secondes et *FF* = fractions de secondes.</span><span class="sxs-lookup"><span data-stu-id="ed32e-112">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="ed32e-113">Exemple : 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="ed32e-113">Example: 1:04:30.512.</span></span> <span data-ttu-id="ed32e-114">Les unités de début peuvent être omises.</span><span class="sxs-lookup"><span data-stu-id="ed32e-114">Leading units can be omitted.</span></span> <span data-ttu-id="ed32e-115">Par exemple, 3:00 (trois minutes) et 45 (45 secondes) sont valides.</span><span class="sxs-lookup"><span data-stu-id="ed32e-115">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed32e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed32e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed32e-117">Attributs XTL</span><span class="sxs-lookup"><span data-stu-id="ed32e-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="ed32e-118">**IAMTimelineSrc::SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="ed32e-118">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



