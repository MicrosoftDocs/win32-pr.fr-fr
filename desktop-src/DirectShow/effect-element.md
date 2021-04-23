---
description: L’élément Effect définit un objet d’effet audio ou vidéo. Un effet est appliqué à un seul flux (par exemple, une composition, une piste ou une source).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Effect, élément (Gdipluseffects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c925e61578857415bb22248a9ad2b1df27cdac
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908657"
---
# <a name="effect-element"></a><span data-ttu-id="14a73-104">Effect, élément</span><span class="sxs-lookup"><span data-stu-id="14a73-104">effect Element</span></span>

> [!Note]  
> <span data-ttu-id="14a73-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="14a73-105">\[Deprecated.</span></span> <span data-ttu-id="14a73-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="14a73-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="14a73-107">L' `effect` élément définit un objet d’effet audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="14a73-107">The `effect` element defines an audio or video effect object.</span></span> <span data-ttu-id="14a73-108">Un effet est appliqué à un seul flux (par exemple, une composition, une piste ou une source).</span><span class="sxs-lookup"><span data-stu-id="14a73-108">An effect is applied to a single stream (such as a composition, track, or source).</span></span>

## <a name="attributes"></a><span data-ttu-id="14a73-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="14a73-109">Attributes</span></span>

<span data-ttu-id="14a73-110">[**CLSID**](clsid-attribute.md), [**Lock**](lock-attribute.md), [**muet**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="14a73-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="14a73-111">Informations parent/enfant</span><span class="sxs-lookup"><span data-stu-id="14a73-111">Parent/Child Information</span></span>



| <span data-ttu-id="14a73-112">Étiquette</span><span class="sxs-lookup"><span data-stu-id="14a73-112">Label</span></span> | <span data-ttu-id="14a73-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="14a73-113">Value</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a73-114">Parent</span><span class="sxs-lookup"><span data-stu-id="14a73-114">Parent</span></span>   | <span data-ttu-id="14a73-115">[**composite**](composite-element.md), [**Group**](group-element.md), [**clip**](clip-element.md), [**Track**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="14a73-115">[**composite**](composite-element.md), [**group**](group-element.md), [**clip**](clip-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="14a73-116">Children</span><span class="sxs-lookup"><span data-stu-id="14a73-116">Children</span></span> | [<span data-ttu-id="14a73-117">**envoyés**</span><span class="sxs-lookup"><span data-stu-id="14a73-117">**param**</span></span>](param-element.md)                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="14a73-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="14a73-118">Remarks</span></span>

<span data-ttu-id="14a73-119">L’attribut **CLSID** spécifie le sous-objet qui crée l’effet.</span><span class="sxs-lookup"><span data-stu-id="14a73-119">The **clsid** attribute specifies the subobject that creates the effect.</span></span>

## <a name="examples"></a><span data-ttu-id="14a73-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="14a73-120">Examples</span></span>


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a><span data-ttu-id="14a73-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14a73-121">Requirements</span></span>



| <span data-ttu-id="14a73-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14a73-122">Requirement</span></span> | <span data-ttu-id="14a73-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="14a73-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a73-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="14a73-124">Header</span></span><br/> | <dl> <span data-ttu-id="14a73-125"><dt>Gdipluseffects. h</dt></span><span class="sxs-lookup"><span data-stu-id="14a73-125"><dt>Gdipluseffects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14a73-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14a73-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a73-127">Éléments XTL</span><span class="sxs-lookup"><span data-stu-id="14a73-127">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




