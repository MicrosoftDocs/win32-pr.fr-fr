---
description: L’élément at définit la valeur d’un élément param à un moment donné, par rapport au début de la transition ou de l’effet qui contient le paramètre.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Élément at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb539331519fb23b6b8aa45b374457229f807a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747261"
---
# <a name="at-element"></a><span data-ttu-id="3f2dc-103">Élément at</span><span class="sxs-lookup"><span data-stu-id="3f2dc-103">at Element</span></span>

> [!Note]  
> <span data-ttu-id="3f2dc-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3f2dc-104">\[Deprecated.</span></span> <span data-ttu-id="3f2dc-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3f2dc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3f2dc-106">L' `at` élément définit la valeur d’un élément [**param**](param-element.md) à un moment donné, par rapport au début de la transition ou de l’effet qui contient le paramètre.</span><span class="sxs-lookup"><span data-stu-id="3f2dc-106">The `at` element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the parameter.</span></span> <span data-ttu-id="3f2dc-107">L' `at` élément amène le paramètre à passer brusquement à la nouvelle valeur à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3f2dc-107">The `at` element causes the parameter to jump abruptly to the new value at the given time.</span></span> <span data-ttu-id="3f2dc-108">Pour une progression fluide vers une nouvelle valeur, utilisez l’élément [**linéaire**](linear-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3f2dc-108">For a smooth progression to a new value, use the [**linear**](linear-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="3f2dc-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="3f2dc-109">Attributes</span></span>

<span data-ttu-id="3f2dc-110">[**heure**](time-attribute.md), [ **valeur**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="3f2dc-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="3f2dc-111">Informations parent/enfant</span><span class="sxs-lookup"><span data-stu-id="3f2dc-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="3f2dc-112">Parent</span><span class="sxs-lookup"><span data-stu-id="3f2dc-112">Parent</span></span>   | [<span data-ttu-id="3f2dc-113">**envoyés**</span><span class="sxs-lookup"><span data-stu-id="3f2dc-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="3f2dc-114">Children</span><span class="sxs-lookup"><span data-stu-id="3f2dc-114">Children</span></span> | <span data-ttu-id="3f2dc-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="3f2dc-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="3f2dc-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="3f2dc-116">Examples</span></span>


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a><span data-ttu-id="3f2dc-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f2dc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f2dc-118">Éléments XTL</span><span class="sxs-lookup"><span data-stu-id="3f2dc-118">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



