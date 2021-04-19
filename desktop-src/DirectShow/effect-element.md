---
description: L’élément Effect définit un objet d’effet audio ou vidéo. Un effet est appliqué à un seul flux (par exemple, une composition, une piste ou une source).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Effect, élément (Gdipluseffects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd31e85407b99c3dffd4417a051be168f7c6d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537851"
---
# <a name="effect-element"></a><span data-ttu-id="ad17d-104">Effect, élément</span><span class="sxs-lookup"><span data-stu-id="ad17d-104">effect Element</span></span>

> [!Note]  
> <span data-ttu-id="ad17d-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="ad17d-105">\[Deprecated.</span></span> <span data-ttu-id="ad17d-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ad17d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ad17d-107">L' `effect` élément définit un objet d’effet audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="ad17d-107">The `effect` element defines an audio or video effect object.</span></span> <span data-ttu-id="ad17d-108">Un effet est appliqué à un seul flux (par exemple, une composition, une piste ou une source).</span><span class="sxs-lookup"><span data-stu-id="ad17d-108">An effect is applied to a single stream (such as a composition, track, or source).</span></span>

## <a name="attributes"></a><span data-ttu-id="ad17d-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="ad17d-109">Attributes</span></span>

<span data-ttu-id="ad17d-110">[**CLSID**](clsid-attribute.md), [**Lock**](lock-attribute.md), [**muet**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="ad17d-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="ad17d-111">Informations parent/enfant</span><span class="sxs-lookup"><span data-stu-id="ad17d-111">Parent/Child Information</span></span>



|          |                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad17d-112">Parent</span><span class="sxs-lookup"><span data-stu-id="ad17d-112">Parent</span></span>   | <span data-ttu-id="ad17d-113">[**composite**](composite-element.md), [**Group**](group-element.md), [**clip**](clip-element.md), [**Track**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="ad17d-113">[**composite**](composite-element.md), [**group**](group-element.md), [**clip**](clip-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="ad17d-114">Children</span><span class="sxs-lookup"><span data-stu-id="ad17d-114">Children</span></span> | [<span data-ttu-id="ad17d-115">**envoyés**</span><span class="sxs-lookup"><span data-stu-id="ad17d-115">**param**</span></span>](param-element.md)                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="ad17d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ad17d-116">Remarks</span></span>

<span data-ttu-id="ad17d-117">L’attribut **CLSID** spécifie le sous-objet qui crée l’effet.</span><span class="sxs-lookup"><span data-stu-id="ad17d-117">The **clsid** attribute specifies the subobject that creates the effect.</span></span>

## <a name="examples"></a><span data-ttu-id="ad17d-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="ad17d-118">Examples</span></span>


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a><span data-ttu-id="ad17d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad17d-119">Requirements</span></span>



| <span data-ttu-id="ad17d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad17d-120">Requirement</span></span> | <span data-ttu-id="ad17d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad17d-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad17d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad17d-122">Header</span></span><br/> | <dl> <span data-ttu-id="ad17d-123"><dt>Gdipluseffects. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad17d-123"><dt>Gdipluseffects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad17d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad17d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad17d-125">Éléments XTL</span><span class="sxs-lookup"><span data-stu-id="ad17d-125">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




