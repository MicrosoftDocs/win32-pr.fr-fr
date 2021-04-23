---
description: L’élément param spécifie la valeur d’une propriété sur une transition, un effet ou un autre sous-objet.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: param, élément (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a10f902e85066f6cea14023e8cff9250126add0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909037"
---
# <a name="param-element"></a><span data-ttu-id="cf6de-103">Élément param</span><span class="sxs-lookup"><span data-stu-id="cf6de-103">param Element</span></span>

> [!Note]  
> <span data-ttu-id="cf6de-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="cf6de-104">\[Deprecated.</span></span> <span data-ttu-id="cf6de-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cf6de-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cf6de-106">L' `param` élément spécifie la valeur d’une propriété sur une transition, un effet ou un autre sous-objet.</span><span class="sxs-lookup"><span data-stu-id="cf6de-106">The `param` element specifies the value of a property on a transition, effect, or other subobject.</span></span>

## <a name="attributes"></a><span data-ttu-id="cf6de-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="cf6de-107">Attributes</span></span>

<span data-ttu-id="cf6de-108">[**nom**](name-attribute.md), [ **valeur**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="cf6de-108">[**name**](name-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="cf6de-109">Informations parent/enfant</span><span class="sxs-lookup"><span data-stu-id="cf6de-109">Parent/Child Information</span></span>



| <span data-ttu-id="cf6de-110">Étiquette</span><span class="sxs-lookup"><span data-stu-id="cf6de-110">Label</span></span> | <span data-ttu-id="cf6de-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf6de-111">Value</span></span> |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6de-112">Parent</span><span class="sxs-lookup"><span data-stu-id="cf6de-112">Parent</span></span>   | <span data-ttu-id="cf6de-113">[**clip**](clip-element.md), [**effet**](effect-element.md), [**transition**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="cf6de-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span> |
| <span data-ttu-id="cf6de-114">Children</span><span class="sxs-lookup"><span data-stu-id="cf6de-114">Children</span></span> | <span data-ttu-id="cf6de-115">[**at**](at-element.md), [ **linéaire**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="cf6de-115">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>                                               |



 

## <a name="remarks"></a><span data-ttu-id="cf6de-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf6de-116">Remarks</span></span>

<span data-ttu-id="cf6de-117">L’attribut **value** spécifie la valeur de la propriété au début de la transition ou de l’effet.</span><span class="sxs-lookup"><span data-stu-id="cf6de-117">The **value** attribute specifies the value of the property at the start of the transition or effect.</span></span> <span data-ttu-id="cf6de-118">Utilisez l’élément **at** ou **Linear** pour spécifier la modification des valeurs.</span><span class="sxs-lookup"><span data-stu-id="cf6de-118">Use the **at** or **linear** element to specify changing values.</span></span> <span data-ttu-id="cf6de-119">Si l’élément **param** ne contient pas d’éléments **at** ou **Linear** , la valeur reste constante sur la durée de l’effet ou de la transition.</span><span class="sxs-lookup"><span data-stu-id="cf6de-119">If the **param** element contains no **at** or **linear** elements, the value remains constant over the duration of the effect or transition.</span></span>

> [!Note]  
> <span data-ttu-id="cf6de-120">Un élément **param** à l’intérieur d’un élément **clip** ne peut pas contenir d’éléments **au niveau** ou **linéaires** .</span><span class="sxs-lookup"><span data-stu-id="cf6de-120">A **param** element inside a **clip** element cannot contain **at** or **linear** elements.</span></span>

 

<span data-ttu-id="cf6de-121">De nombreuses transitions prennent en charge une propriété de **progression** standard qui varie de 0 à 1,0, indiquant quel pourcentage de la transition est reflété dans la sortie.</span><span class="sxs-lookup"><span data-stu-id="cf6de-121">Many transitions support a standard **Progress** property that ranges from 0 to 1.0, indicating what percentage of the transition is reflected in the output.</span></span> <span data-ttu-id="cf6de-122">À la **progression** = 0,0, la transition se trouve au début de sa séquence (entièrement la première image vidéo).</span><span class="sxs-lookup"><span data-stu-id="cf6de-122">At **Progress** = 0.0, the transition is at the beginning of its sequence (entirely the first video image).</span></span> <span data-ttu-id="cf6de-123">À la **progression** = 0,5, la transition est à moitié terminée.</span><span class="sxs-lookup"><span data-stu-id="cf6de-123">At **Progress** = 0.5, the transition is half complete.</span></span> <span data-ttu-id="cf6de-124">(Par exemple, dans une réinitialisation, à la **progression** = 0,5 la limite de transition se trouve au centre de l’image) À la **progression** = 1,0, la transition est terminée (entièrement la deuxième image).</span><span class="sxs-lookup"><span data-stu-id="cf6de-124">(For example, in a wipe, at **Progress** = 0.5 the transition boundary is in the center of the image) At **Progress** = 1.0, the transition is complete (entirely the second image).</span></span> <span data-ttu-id="cf6de-125">Par défaut, les transitions passent de **Progress** = 0,0 au début de la transition vers **Progress** = 1,0 à la fin.</span><span class="sxs-lookup"><span data-stu-id="cf6de-125">By default, transitions go from **Progress** = 0.0 at the start of the transition to **Progress** = 1.0 at the end.</span></span>

<span data-ttu-id="cf6de-126">D’autres propriétés sont généralement spécifiques à une transition ou un effet particulier.</span><span class="sxs-lookup"><span data-stu-id="cf6de-126">Other properties are usually specific to one particular transition or effect.</span></span> <span data-ttu-id="cf6de-127">Par exemple, la transition de réinitialisation prend en charge une propriété **GradientSize** qui contrôle la largeur de la zone de transition.</span><span class="sxs-lookup"><span data-stu-id="cf6de-127">For example, the wipe transition supports a **GradientSize** property that controls the width of the transition area.</span></span>

<span data-ttu-id="cf6de-128">Pour exécuter une transition vers l’arrière, définissez la propriété **Progress** sur 1,0 au début de la transition et utilisez l’élément **linéaire** pour changer la valeur en 0,0, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="cf6de-128">To run a transition backward, set the **Progress** property to 1.0 at the start of the transition, and use the **linear** element to change the value to 0.0, as shown in the following example:</span></span>


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a><span data-ttu-id="cf6de-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="cf6de-129">Examples</span></span>


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a><span data-ttu-id="cf6de-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf6de-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf6de-131">Éléments XTL</span><span class="sxs-lookup"><span data-stu-id="cf6de-131">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



