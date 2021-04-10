---
description: L’attribut muet spécifie l’État muet de l’objet.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: Attribut muet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109434"
---
# <a name="mute-attribute"></a><span data-ttu-id="30c1f-103">Attribut muet</span><span class="sxs-lookup"><span data-stu-id="30c1f-103">mute Attribute</span></span>

> [!Note]  
> <span data-ttu-id="30c1f-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="30c1f-104">\[Deprecated.</span></span> <span data-ttu-id="30c1f-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="30c1f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="30c1f-106">L' `mute` attribut spécifie l’État muet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="30c1f-106">The `mute` attribute specifies the object's mute state.</span></span> <span data-ttu-id="30c1f-107">Si la valeur est **true**, l’objet et ses enfants ne sont pas rendus.</span><span class="sxs-lookup"><span data-stu-id="30c1f-107">If the value is **TRUE**, neither the object nor its children are rendered.</span></span> <span data-ttu-id="30c1f-108">Si la valeur est **false**, l’objet est rendu et ses enfants sont rendus en fonction de leur propre État muet.</span><span class="sxs-lookup"><span data-stu-id="30c1f-108">If the value is **FALSE**, the object is rendered, and its children are rendered according to their own mute state.</span></span> <span data-ttu-id="30c1f-109">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="30c1f-109">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="30c1f-110">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="30c1f-110">Possible Values</span></span>

<span data-ttu-id="30c1f-111">Les valeurs suivantes sont définies sur TRUE : y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="30c1f-111">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="30c1f-112">Les valeurs suivantes sont définies avec la valeur FALSe : n, N, f, F, 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="30c1f-112">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="30c1f-113">S'applique à</span><span class="sxs-lookup"><span data-stu-id="30c1f-113">Applies To</span></span>

<span data-ttu-id="30c1f-114">[**clip**](clip-element.md), [**composite**](composite-element.md), [**Effect**](effect-element.md), [**Group**](group-element.md), [**Timeline**](timeline-element.md), [**transition**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="30c1f-114">[**clip**](clip-element.md), [**composite**](composite-element.md), [**effect**](effect-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="30c1f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30c1f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c1f-116">Attributs XTL</span><span class="sxs-lookup"><span data-stu-id="30c1f-116">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="30c1f-117">**IAMTimelineObj::SetMuted**</span><span class="sxs-lookup"><span data-stu-id="30c1f-117">**IAMTimelineObj::SetMuted**</span></span>](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



