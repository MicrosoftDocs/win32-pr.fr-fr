---
description: La propriété FramesPerSecond récupère la fréquence d’images vidéo pour le titre du DVD actuel.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: Propriété FramesPerSecond
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00ec3281d88a2901f630c9231edbf1e76a89c23
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515129"
---
# <a name="framespersecond-property"></a><span data-ttu-id="9f5d0-103">Propriété FramesPerSecond</span><span class="sxs-lookup"><span data-stu-id="9f5d0-103">FramesPerSecond Property</span></span>

> [!Note]  
> <span data-ttu-id="9f5d0-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9f5d0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9f5d0-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9f5d0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9f5d0-106">La `FramesPerSecond` propriété récupère la fréquence d’images vidéo pour le titre du DVD actuel.</span><span class="sxs-lookup"><span data-stu-id="9f5d0-106">The `FramesPerSecond` property retrieves the video frame rate for the current DVD title.</span></span>

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a><span data-ttu-id="9f5d0-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9f5d0-107">Return Value</span></span>

<span data-ttu-id="9f5d0-108">Retourne une valeur entière représentant la fréquence d’images vidéo ; 25 ou 30 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="9f5d0-108">Returns an integer value representing the video frame rate; either 25 or 30 frames per second.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f5d0-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9f5d0-109">Remarks</span></span>

<span data-ttu-id="9f5d0-110">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9f5d0-110">This property is read-only with no default value.</span></span> <span data-ttu-id="9f5d0-111">Les signaux vidéo NTSC sont affichés à 30 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="9f5d0-111">NTSC video signals are displayed at 30 frames per second.</span></span> <span data-ttu-id="9f5d0-112">La PAL est affichée à 25 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="9f5d0-112">PAL is displayed at 25 frames per second.</span></span> <span data-ttu-id="9f5d0-113">Un disque est encodé pour être lu sur NTSC ou PAL, mais ne peut pas être lu sur les deux.</span><span class="sxs-lookup"><span data-stu-id="9f5d0-113">A disc is encoded to play on either NTSC or PAL, but cannot play on both.</span></span>

 

 



