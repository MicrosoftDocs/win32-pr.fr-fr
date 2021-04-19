---
description: La propriété VolumesAvailable récupère le nombre de volumes dans un ensemble multivolume.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Propriété VolumesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccdcf32ba8b7bea3958ef469bc0f90f9d41ecc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523286"
---
# <a name="volumesavailable-property"></a><span data-ttu-id="84760-103">Propriété VolumesAvailable</span><span class="sxs-lookup"><span data-stu-id="84760-103">VolumesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="84760-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="84760-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="84760-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="84760-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="84760-106">La `VolumesAvailable` propriété récupère le nombre de volumes dans un ensemble multivolume.</span><span class="sxs-lookup"><span data-stu-id="84760-106">The `VolumesAvailable` property retrieves the number of volumes in a multivolume set.</span></span>

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a><span data-ttu-id="84760-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="84760-107">Return Value</span></span>

<span data-ttu-id="84760-108">Retourne le nombre de volumes dans le jeu sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="84760-108">Returns the number of volumes in the set as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="84760-109">Notes</span><span class="sxs-lookup"><span data-stu-id="84760-109">Remarks</span></span>

<span data-ttu-id="84760-110">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="84760-110">This property is read-only with no default value.</span></span> <span data-ttu-id="84760-111">Certains titres de DVD peuvent être publiés sous la forme d’un jeu ou d’une série à plusieurs disques.</span><span class="sxs-lookup"><span data-stu-id="84760-111">Some DVD titles might be released as a multidisc set or series.</span></span> <span data-ttu-id="84760-112">Utilisez cette méthode pour déterminer le numéro de volume du disque actuel.</span><span class="sxs-lookup"><span data-stu-id="84760-112">Use this method to determine the volume number for the current disc.</span></span>

 

 



