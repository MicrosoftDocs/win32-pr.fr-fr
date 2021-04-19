---
description: L’élément composite définit une composition, un objet conteneur pour les pistes et d’autres compositions imbriquées.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Élément composite
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c81bf445769c049287bdfa7d23f4ab82bb0f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517149"
---
# <a name="composite-element"></a><span data-ttu-id="9ce1a-103">Élément composite</span><span class="sxs-lookup"><span data-stu-id="9ce1a-103">composite Element</span></span>

> [!Note]  
> <span data-ttu-id="9ce1a-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="9ce1a-104">\[Deprecated.</span></span> <span data-ttu-id="9ce1a-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9ce1a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9ce1a-106">L' `composite` élément définit une composition, un objet conteneur pour les pistes et d’autres compositions imbriquées.</span><span class="sxs-lookup"><span data-stu-id="9ce1a-106">The `composite` element defines a composition, a container object for tracks and other nested compositions.</span></span>

## <a name="attributes"></a><span data-ttu-id="9ce1a-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="9ce1a-107">Attributes</span></span>

<span data-ttu-id="9ce1a-108">[**Lock**](lock-attribute.md), [**muet**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="9ce1a-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="9ce1a-109">Informations parent/enfant</span><span class="sxs-lookup"><span data-stu-id="9ce1a-109">Parent/Child Information</span></span>



|          |                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce1a-110">Parent</span><span class="sxs-lookup"><span data-stu-id="9ce1a-110">Parent</span></span>   | <span data-ttu-id="9ce1a-111">`composite`, [ **groupe**](group-element.md)</span><span class="sxs-lookup"><span data-stu-id="9ce1a-111">`composite`, [**group**](group-element.md)</span></span>                                                                             |
| <span data-ttu-id="9ce1a-112">Children</span><span class="sxs-lookup"><span data-stu-id="9ce1a-112">Children</span></span> | <span data-ttu-id="9ce1a-113">`composite`, [**Effect**](effect-element.md), [**Track**](track-element.md), [**transition**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="9ce1a-113">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9ce1a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9ce1a-114">Remarks</span></span>

<span data-ttu-id="9ce1a-115">Dans un `composite` élément, la priorité des couches imbriquées est déterminée implicitement par l’ordre dans lequel elles apparaissent dans l’élément.</span><span class="sxs-lookup"><span data-stu-id="9ce1a-115">Within a `composite` element, the priority of nested layers is determined implicitly by the order in which they appear within the element.</span></span> <span data-ttu-id="9ce1a-116">La première couche a la priorité 0 et les couches suivantes comportent des valeurs de priorité accrues.</span><span class="sxs-lookup"><span data-stu-id="9ce1a-116">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="9ce1a-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="9ce1a-117">Examples</span></span>


```XML
<composite> </composite>
```



## <a name="see-also"></a><span data-ttu-id="9ce1a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ce1a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce1a-119">Éléments XTL</span><span class="sxs-lookup"><span data-stu-id="9ce1a-119">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



