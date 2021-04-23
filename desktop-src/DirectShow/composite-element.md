---
description: L’élément composite définit une composition, un objet conteneur pour les pistes et d’autres compositions imbriquées.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Élément composite
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5eff3e0c16040f837e4c8a792ebac3124d723d1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908837"
---
# <a name="composite-element"></a><span data-ttu-id="7f93f-103">Élément composite</span><span class="sxs-lookup"><span data-stu-id="7f93f-103">composite Element</span></span>

> [!Note]  
> <span data-ttu-id="7f93f-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7f93f-104">\[Deprecated.</span></span> <span data-ttu-id="7f93f-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7f93f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7f93f-106">L' `composite` élément définit une composition, un objet conteneur pour les pistes et d’autres compositions imbriquées.</span><span class="sxs-lookup"><span data-stu-id="7f93f-106">The `composite` element defines a composition, a container object for tracks and other nested compositions.</span></span>

## <a name="attributes"></a><span data-ttu-id="7f93f-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="7f93f-107">Attributes</span></span>

<span data-ttu-id="7f93f-108">[**Lock**](lock-attribute.md), [**muet**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="7f93f-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="7f93f-109">Informations parent/enfant</span><span class="sxs-lookup"><span data-stu-id="7f93f-109">Parent/Child Information</span></span>



| <span data-ttu-id="7f93f-110">Étiquette</span><span class="sxs-lookup"><span data-stu-id="7f93f-110">Label</span></span> | <span data-ttu-id="7f93f-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f93f-111">Value</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f93f-112">Parent</span><span class="sxs-lookup"><span data-stu-id="7f93f-112">Parent</span></span>   | <span data-ttu-id="7f93f-113">`composite`, [ **groupe**](group-element.md)</span><span class="sxs-lookup"><span data-stu-id="7f93f-113">`composite`, [**group**](group-element.md)</span></span>                                                                             |
| <span data-ttu-id="7f93f-114">Children</span><span class="sxs-lookup"><span data-stu-id="7f93f-114">Children</span></span> | <span data-ttu-id="7f93f-115">`composite`, [**Effect**](effect-element.md), [**Track**](track-element.md), [**transition**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="7f93f-115">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7f93f-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f93f-116">Remarks</span></span>

<span data-ttu-id="7f93f-117">Dans un `composite` élément, la priorité des couches imbriquées est déterminée implicitement par l’ordre dans lequel elles apparaissent dans l’élément.</span><span class="sxs-lookup"><span data-stu-id="7f93f-117">Within a `composite` element, the priority of nested layers is determined implicitly by the order in which they appear within the element.</span></span> <span data-ttu-id="7f93f-118">La première couche a la priorité 0 et les couches suivantes comportent des valeurs de priorité accrues.</span><span class="sxs-lookup"><span data-stu-id="7f93f-118">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="7f93f-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="7f93f-119">Examples</span></span>


```XML
<composite> </composite>
```



## <a name="see-also"></a><span data-ttu-id="7f93f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f93f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f93f-121">Éléments XTL</span><span class="sxs-lookup"><span data-stu-id="7f93f-121">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



