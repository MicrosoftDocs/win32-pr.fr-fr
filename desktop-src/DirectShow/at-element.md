---
description: L’élément at définit la valeur d’un élément param à un moment donné, par rapport au début de la transition ou de l’effet qui contient le paramètre.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Élément at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5822f82a349f31f0d4c8de3f522f7f4f3346a08
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909827"
---
# <a name="at-element"></a><span data-ttu-id="b8ad5-103">Élément at</span><span class="sxs-lookup"><span data-stu-id="b8ad5-103">at Element</span></span>

> [!Note]  
> <span data-ttu-id="b8ad5-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-104">\[Deprecated.</span></span> <span data-ttu-id="b8ad5-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b8ad5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b8ad5-106">L' `at` élément définit la valeur d’un élément [**param**](param-element.md) à un moment donné, par rapport au début de la transition ou de l’effet qui contient le paramètre.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-106">The `at` element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the parameter.</span></span> <span data-ttu-id="b8ad5-107">L' `at` élément amène le paramètre à passer brusquement à la nouvelle valeur à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-107">The `at` element causes the parameter to jump abruptly to the new value at the given time.</span></span> <span data-ttu-id="b8ad5-108">Pour une progression fluide vers une nouvelle valeur, utilisez l’élément [**linéaire**](linear-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b8ad5-108">For a smooth progression to a new value, use the [**linear**](linear-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="b8ad5-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="b8ad5-109">Attributes</span></span>

<span data-ttu-id="b8ad5-110">[**heure**](time-attribute.md), [ **valeur**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="b8ad5-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="b8ad5-111">Informations parent/enfant</span><span class="sxs-lookup"><span data-stu-id="b8ad5-111">Parent/Child Information</span></span>



| <span data-ttu-id="b8ad5-112">Étiquette</span><span class="sxs-lookup"><span data-stu-id="b8ad5-112">Label</span></span> | <span data-ttu-id="b8ad5-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8ad5-113">Value</span></span> |
|----------|--------------------------------|
| <span data-ttu-id="b8ad5-114">Parent</span><span class="sxs-lookup"><span data-stu-id="b8ad5-114">Parent</span></span>   | [<span data-ttu-id="b8ad5-115">**envoyés**</span><span class="sxs-lookup"><span data-stu-id="b8ad5-115">**param**</span></span>](param-element.md) |
| <span data-ttu-id="b8ad5-116">Children</span><span class="sxs-lookup"><span data-stu-id="b8ad5-116">Children</span></span> | <span data-ttu-id="b8ad5-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="b8ad5-117">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="b8ad5-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="b8ad5-118">Examples</span></span>


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a><span data-ttu-id="b8ad5-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8ad5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ad5-120">Éléments XTL</span><span class="sxs-lookup"><span data-stu-id="b8ad5-120">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



