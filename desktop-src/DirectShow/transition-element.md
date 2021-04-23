---
description: L’élément transition définit un objet de transition. Une transition est une transformation à deux entrées qui produit une transition d’un flux (par exemple, composite ou Track) à une autre.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Élément transition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60bf6b915a393ab153f0e94862cb5ed72dd3424c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910037"
---
# <a name="transition-element"></a><span data-ttu-id="38ce4-104">Élément transition</span><span class="sxs-lookup"><span data-stu-id="38ce4-104">transition Element</span></span>

> [!Note]  
> <span data-ttu-id="38ce4-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="38ce4-105">\[Deprecated.</span></span> <span data-ttu-id="38ce4-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="38ce4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="38ce4-107">L' `transition` élément définit un objet de transition.</span><span class="sxs-lookup"><span data-stu-id="38ce4-107">The `transition` element defines a transition object.</span></span> <span data-ttu-id="38ce4-108">Une transition est une transformation à deux entrées qui produit une transition d’un flux (par exemple, composite ou Track) à une autre.</span><span class="sxs-lookup"><span data-stu-id="38ce4-108">A transition is a two-input transform that results in a transition from one stream (such as a composite or track) to another.</span></span>

## <a name="attributes"></a><span data-ttu-id="38ce4-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="38ce4-109">Attributes</span></span>

<span data-ttu-id="38ce4-110">[**CLSID**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**Lock**](lock-attribute.md), [**muet**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="38ce4-110">[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="38ce4-111">Informations parent/enfant</span><span class="sxs-lookup"><span data-stu-id="38ce4-111">Parent/Child Information</span></span>



| <span data-ttu-id="38ce4-112">Étiquette</span><span class="sxs-lookup"><span data-stu-id="38ce4-112">Label</span></span> | <span data-ttu-id="38ce4-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="38ce4-113">Value</span></span> |
|----------|------------------------------------------------------------------------|
| <span data-ttu-id="38ce4-114">Parent</span><span class="sxs-lookup"><span data-stu-id="38ce4-114">Parent</span></span>   | <span data-ttu-id="38ce4-115">[**composite**](composite-element.md), [ **Track**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="38ce4-115">[**composite**](composite-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="38ce4-116">Children</span><span class="sxs-lookup"><span data-stu-id="38ce4-116">Children</span></span> | [<span data-ttu-id="38ce4-117">**envoyés**</span><span class="sxs-lookup"><span data-stu-id="38ce4-117">**param**</span></span>](param-element.md)                                         |



 

## <a name="remarks"></a><span data-ttu-id="38ce4-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="38ce4-118">Remarks</span></span>

<span data-ttu-id="38ce4-119">L’attribut **CLSID** spécifie le sous-objet qui crée la transition.</span><span class="sxs-lookup"><span data-stu-id="38ce4-119">The **clsid** attribute specifies the subobject that creates the transition.</span></span>

## <a name="examples"></a><span data-ttu-id="38ce4-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="38ce4-120">Examples</span></span>


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a><span data-ttu-id="38ce4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38ce4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ce4-122">Éléments XTL</span><span class="sxs-lookup"><span data-stu-id="38ce4-122">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



