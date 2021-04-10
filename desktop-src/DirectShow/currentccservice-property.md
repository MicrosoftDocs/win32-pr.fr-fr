---
description: La propriété CurrentCCService définit ou récupère le service de sous-titrage en cours.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Propriété CurrentCCService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5c1ddf243b0ec943be1f22930a8802d28d1bda
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846477"
---
# <a name="currentccservice-property"></a><span data-ttu-id="e8bda-103">Propriété CurrentCCService</span><span class="sxs-lookup"><span data-stu-id="e8bda-103">CurrentCCService Property</span></span>

> [!Note]  
> <span data-ttu-id="e8bda-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e8bda-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e8bda-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e8bda-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e8bda-106">La `CurrentCCService` propriété définit ou récupère le service de sous-titrage en cours.</span><span class="sxs-lookup"><span data-stu-id="e8bda-106">The `CurrentCCService` property sets or retrieves the current closed captioning service.</span></span>

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a><span data-ttu-id="e8bda-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e8bda-107">Return Value</span></span>

<span data-ttu-id="e8bda-108">Retourne une valeur entière indiquant le type de service de sous-titrage activé.</span><span class="sxs-lookup"><span data-stu-id="e8bda-108">Returns an integer value indicating the type of closed captioning service enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8bda-109">Notes</span><span class="sxs-lookup"><span data-stu-id="e8bda-109">Remarks</span></span>

<span data-ttu-id="e8bda-110">Les valeurs possibles de cette propriété sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8bda-110">The possible values of this property are:</span></span>



| <span data-ttu-id="e8bda-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8bda-111">Value</span></span> | <span data-ttu-id="e8bda-112">Description</span><span class="sxs-lookup"><span data-stu-id="e8bda-112">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="e8bda-113">0x0</span><span class="sxs-lookup"><span data-stu-id="e8bda-113">0x0</span></span>   | <span data-ttu-id="e8bda-114">Aucun service en cours.</span><span class="sxs-lookup"><span data-stu-id="e8bda-114">No current service.</span></span> <span data-ttu-id="e8bda-115">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e8bda-115">This is the default value.</span></span>                       |
| <span data-ttu-id="e8bda-116">0x1</span><span class="sxs-lookup"><span data-stu-id="e8bda-116">0x1</span></span>   | <span data-ttu-id="e8bda-117">True Captioning, premier champ.</span><span class="sxs-lookup"><span data-stu-id="e8bda-117">True captioning, first field.</span></span> <span data-ttu-id="e8bda-118">Service par défaut.</span><span class="sxs-lookup"><span data-stu-id="e8bda-118">Default service.</span></span>                       |
| <span data-ttu-id="e8bda-119">0x2</span><span class="sxs-lookup"><span data-stu-id="e8bda-119">0x2</span></span>   | <span data-ttu-id="e8bda-120">Sous-titrage pour la langue secondaire, deuxième champ.</span><span class="sxs-lookup"><span data-stu-id="e8bda-120">Captioning for secondary language, second field.</span></span> <span data-ttu-id="e8bda-121">Généralement non utilisé.</span><span class="sxs-lookup"><span data-stu-id="e8bda-121">Generally not used.</span></span> |



 

<span data-ttu-id="e8bda-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e8bda-122">This property is read/write.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8bda-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8bda-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8bda-124">**CCActive**</span><span class="sxs-lookup"><span data-stu-id="e8bda-124">**CCActive**</span></span>](ccactive-property.md)
</dt> </dl>

 

 



