---
description: La propriété CurrentVolume récupère le numéro de volume du répertoire racine actuel.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Propriété CurrentVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b91c394be620dfc3f00b8793222848131355f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516335"
---
# <a name="currentvolume-property"></a><span data-ttu-id="9b2bd-103">Propriété CurrentVolume</span><span class="sxs-lookup"><span data-stu-id="9b2bd-103">CurrentVolume Property</span></span>

> [!Note]  
> <span data-ttu-id="9b2bd-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9b2bd-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9b2bd-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9b2bd-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9b2bd-106">La `CurrentVolume` propriété récupère le numéro de volume pour le répertoire racine actuel.</span><span class="sxs-lookup"><span data-stu-id="9b2bd-106">The `CurrentVolume` property retrieves the volume number for the current root directory.</span></span>

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a><span data-ttu-id="9b2bd-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9b2bd-107">Return Value</span></span>

<span data-ttu-id="9b2bd-108">Retourne une valeur entière représentant le volume DVD actuel.</span><span class="sxs-lookup"><span data-stu-id="9b2bd-108">Returns an integer value representing the current DVD volume.</span></span> <span data-ttu-id="9b2bd-109">Si un disque fait partie d’un ensemble de plusieurs volumes, la valeur entière doit être supérieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="9b2bd-109">If a disc is part of a multi-volume set, then the integer value should be greater than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b2bd-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9b2bd-110">Remarks</span></span>

<span data-ttu-id="9b2bd-111">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9b2bd-111">This property is read-only with no default value.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b2bd-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b2bd-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b2bd-113">**VolumesAvailable**</span><span class="sxs-lookup"><span data-stu-id="9b2bd-113">**VolumesAvailable**</span></span>](volumesavailable-property.md)
</dt> </dl>

 

 



