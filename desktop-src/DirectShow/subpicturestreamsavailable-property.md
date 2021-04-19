---
description: La propriété SubpictureStreamsAvailable récupère le nombre de flux de sous-image disponibles dans le titre actuel.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Propriété SubpictureStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530743"
---
# <a name="subpicturestreamsavailable-property"></a><span data-ttu-id="a6cff-103">Propriété SubpictureStreamsAvailable</span><span class="sxs-lookup"><span data-stu-id="a6cff-103">SubpictureStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="a6cff-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a6cff-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a6cff-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a6cff-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a6cff-106">La `SubpictureStreamsAvailable` propriété récupère le nombre de flux de sous-image disponibles dans le titre actuel.</span><span class="sxs-lookup"><span data-stu-id="a6cff-106">The `SubpictureStreamsAvailable` property retrieves the number of subpicture streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="a6cff-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a6cff-107">Return Value</span></span>

<span data-ttu-id="a6cff-108">Retourne le nombre de flux disponibles sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="a6cff-108">Returns the number of available streams as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6cff-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a6cff-109">Remarks</span></span>

<span data-ttu-id="a6cff-110">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a6cff-110">This property is read-only with no default value.</span></span> <span data-ttu-id="a6cff-111">Pour interroger chaque flux pour son attribut Language, appelez d’abord cette méthode pour obtenir la limite supérieure.</span><span class="sxs-lookup"><span data-stu-id="a6cff-111">To query each stream for its language attribute, first call this method to get the upper bound.</span></span>

<span data-ttu-id="a6cff-112">La numérotation des flux est de base zéro.</span><span class="sxs-lookup"><span data-stu-id="a6cff-112">Stream numbering is zero-based.</span></span>

 

 



