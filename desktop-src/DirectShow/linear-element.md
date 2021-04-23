---
description: L’élément Linear définit la valeur d’un élément param à un moment donné, par rapport au début de la transition ou de l’effet qui contient l’élément param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Élément linéaire (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e722dcbc68d24d76f34c80bdd17a91ad44423aa
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910087"
---
# <a name="linear-element"></a><span data-ttu-id="02509-103">Élément linéaire</span><span class="sxs-lookup"><span data-stu-id="02509-103">linear Element</span></span>

> [!Note]  
> <span data-ttu-id="02509-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="02509-104">\[Deprecated.</span></span> <span data-ttu-id="02509-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="02509-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="02509-106">L’élément Linear définit la valeur d’un élément [**param**](param-element.md) à un moment donné, par rapport au début de la transition ou de l’effet qui contient l’élément **param** .</span><span class="sxs-lookup"><span data-stu-id="02509-106">The linear element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the **param** element.</span></span> <span data-ttu-id="02509-107">L' `linear` élément fait en sorte que le paramètre effectue une transition en douceur de sa valeur précédente à la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="02509-107">The `linear` element causes the parameter to make a smooth transition from its previous value to the new value.</span></span> <span data-ttu-id="02509-108">Pour obtenir un saut instantané vers une nouvelle valeur, utilisez l’élément [**at**](at-element.md) .</span><span class="sxs-lookup"><span data-stu-id="02509-108">For an instantaneous jump to a new value, use the [**at**](at-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="02509-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="02509-109">Attributes</span></span>

<span data-ttu-id="02509-110">[**heure**](time-attribute.md), [ **valeur**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="02509-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="02509-111">Informations parent/enfant</span><span class="sxs-lookup"><span data-stu-id="02509-111">Parent/Child Information</span></span>



| <span data-ttu-id="02509-112">Étiquette</span><span class="sxs-lookup"><span data-stu-id="02509-112">Label</span></span> | <span data-ttu-id="02509-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="02509-113">Value</span></span> |
|----------|--------------------------------|
| <span data-ttu-id="02509-114">Parent</span><span class="sxs-lookup"><span data-stu-id="02509-114">Parent</span></span>   | [<span data-ttu-id="02509-115">**envoyés**</span><span class="sxs-lookup"><span data-stu-id="02509-115">**param**</span></span>](param-element.md) |
| <span data-ttu-id="02509-116">Children</span><span class="sxs-lookup"><span data-stu-id="02509-116">Children</span></span> | <span data-ttu-id="02509-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="02509-117">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="02509-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="02509-118">Examples</span></span>


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a><span data-ttu-id="02509-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02509-119">Requirements</span></span>



| <span data-ttu-id="02509-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02509-120">Requirement</span></span> | <span data-ttu-id="02509-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="02509-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="02509-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="02509-122">Header</span></span><br/> | <dl> <span data-ttu-id="02509-123"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="02509-123"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02509-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02509-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02509-125">Éléments XTL</span><span class="sxs-lookup"><span data-stu-id="02509-125">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




