---
description: L’élément Linear définit la valeur d’un élément param à un moment donné, par rapport au début de la transition ou de l’effet qui contient l’élément param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Élément linéaire (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27080d08a1bbec98d5fa34b2739c63958e5d170a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530390"
---
# <a name="linear-element"></a><span data-ttu-id="64b25-103">Élément linéaire</span><span class="sxs-lookup"><span data-stu-id="64b25-103">linear Element</span></span>

> [!Note]  
> <span data-ttu-id="64b25-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="64b25-104">\[Deprecated.</span></span> <span data-ttu-id="64b25-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="64b25-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="64b25-106">L’élément Linear définit la valeur d’un élément [**param**](param-element.md) à un moment donné, par rapport au début de la transition ou de l’effet qui contient l’élément **param** .</span><span class="sxs-lookup"><span data-stu-id="64b25-106">The linear element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the **param** element.</span></span> <span data-ttu-id="64b25-107">L' `linear` élément fait en sorte que le paramètre effectue une transition en douceur de sa valeur précédente à la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="64b25-107">The `linear` element causes the parameter to make a smooth transition from its previous value to the new value.</span></span> <span data-ttu-id="64b25-108">Pour obtenir un saut instantané vers une nouvelle valeur, utilisez l’élément [**at**](at-element.md) .</span><span class="sxs-lookup"><span data-stu-id="64b25-108">For an instantaneous jump to a new value, use the [**at**](at-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="64b25-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="64b25-109">Attributes</span></span>

<span data-ttu-id="64b25-110">[**heure**](time-attribute.md), [ **valeur**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="64b25-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="64b25-111">Informations parent/enfant</span><span class="sxs-lookup"><span data-stu-id="64b25-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="64b25-112">Parent</span><span class="sxs-lookup"><span data-stu-id="64b25-112">Parent</span></span>   | [<span data-ttu-id="64b25-113">**envoyés**</span><span class="sxs-lookup"><span data-stu-id="64b25-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="64b25-114">Children</span><span class="sxs-lookup"><span data-stu-id="64b25-114">Children</span></span> | <span data-ttu-id="64b25-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="64b25-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="64b25-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="64b25-116">Examples</span></span>


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a><span data-ttu-id="64b25-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64b25-117">Requirements</span></span>



| <span data-ttu-id="64b25-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64b25-118">Requirement</span></span> | <span data-ttu-id="64b25-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="64b25-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="64b25-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="64b25-120">Header</span></span><br/> | <dl> <span data-ttu-id="64b25-121"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="64b25-121"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64b25-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64b25-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64b25-123">Éléments XTL</span><span class="sxs-lookup"><span data-stu-id="64b25-123">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




