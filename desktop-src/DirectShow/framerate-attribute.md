---
description: L’attribut pafréquence spécifie un cadence, en images par seconde.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: Attribut de fréquence (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1af5deb8ae2a851b328fcd6d9ffa3923328708
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950152"
---
# <a name="framerate-attribute-directshow"></a><span data-ttu-id="f04e1-103">Attribut de fréquence (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="f04e1-103">framerate Attribute (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="f04e1-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f04e1-104">\[Deprecated.</span></span> <span data-ttu-id="f04e1-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f04e1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f04e1-106">L' `framerate` attribut spécifie une cadence, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="f04e1-106">The `framerate` attribute specifies a framerate, in frames per second.</span></span>

## <a name="possible-values"></a><span data-ttu-id="f04e1-107">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="f04e1-107">Possible Values</span></span>

<span data-ttu-id="f04e1-108">Valeur à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="f04e1-108">Floating-point value.</span></span> <span data-ttu-id="f04e1-109">La valeur doit inclure le zéro non significatif avant la décimale.</span><span class="sxs-lookup"><span data-stu-id="f04e1-109">The value must include the leading zero before the decimal place.</span></span> <span data-ttu-id="f04e1-110">Par exemple, 0,3, pas. 3.</span><span class="sxs-lookup"><span data-stu-id="f04e1-110">For example, 0.3, not .3.</span></span> <span data-ttu-id="f04e1-111">N’utilisez pas plus de sept chiffres décimaux.</span><span class="sxs-lookup"><span data-stu-id="f04e1-111">Do not use more than seven decimal digits.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f04e1-112">S'applique à</span><span class="sxs-lookup"><span data-stu-id="f04e1-112">Applies To</span></span>

<span data-ttu-id="f04e1-113">[**clip**](clip-element.md), [**groupe**](group-element.md), [**chronologie**](timeline-element.md)</span><span class="sxs-lookup"><span data-stu-id="f04e1-113">[**clip**](clip-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md)</span></span>

## <a name="remarks"></a><span data-ttu-id="f04e1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f04e1-114">Remarks</span></span>

<span data-ttu-id="f04e1-115">Pour l’élément **clip** , cet attribut spécifie la fréquence d’images par défaut de la source.</span><span class="sxs-lookup"><span data-stu-id="f04e1-115">For the **clip** element, this attribute specifies the default frame rate of the source.</span></span> <span data-ttu-id="f04e1-116">Spécifiez l’attribut pour les séquences andDIB d’images fixes.</span><span class="sxs-lookup"><span data-stu-id="f04e1-116">Specify the attribute for still images andDIB sequences.</span></span> <span data-ttu-id="f04e1-117">Pour une image continue, définissez la valeur sur zéro.</span><span class="sxs-lookup"><span data-stu-id="f04e1-117">For a still image, set the value to zero.</span></span> <span data-ttu-id="f04e1-118">Pour une séquence DIB, utilisez une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="f04e1-118">For a DIB sequence, use a nonzero value.</span></span> <span data-ttu-id="f04e1-119">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="f04e1-119">The default value is zero.</span></span>

<span data-ttu-id="f04e1-120">Pour l’élément **Group** , cet attribut spécifie la fréquence d’images de sortie pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="f04e1-120">For the **group** element, this attribute specifies the output frame rate for the group.</span></span>

<span data-ttu-id="f04e1-121">Pour l’élément **Timeline** , cet attribut spécifie la fréquence d’images par défaut pour tous les groupes.</span><span class="sxs-lookup"><span data-stu-id="f04e1-121">For the **timeline** element, this attribute specifies the default frame rate for all groups.</span></span>

## <a name="see-also"></a><span data-ttu-id="f04e1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f04e1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f04e1-123">Attributs XTL</span><span class="sxs-lookup"><span data-stu-id="f04e1-123">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="f04e1-124">**IAMTimelineSrc::SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="f04e1-124">**IAMTimelineSrc::SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[<span data-ttu-id="f04e1-125">**IAMTimelineGroup::SetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="f04e1-125">**IAMTimelineGroup::SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[<span data-ttu-id="f04e1-126">**IAMTimeline::SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="f04e1-126">**IAMTimeline::SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 



