---
description: La méthode Play lit le titre du DVD actuel.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Play, méthode (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521295"
---
# <a name="play-method-directshow"></a><span data-ttu-id="646a4-103">Play, méthode (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="646a4-103">Play Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="646a4-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="646a4-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="646a4-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="646a4-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="646a4-106">La `Play` méthode lit le titre du DVD actuel.</span><span class="sxs-lookup"><span data-stu-id="646a4-106">The `Play` method plays the current DVD title.</span></span>

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a><span data-ttu-id="646a4-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="646a4-107">Return Value</span></span>

<span data-ttu-id="646a4-108">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="646a4-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="646a4-109">Notes</span><span class="sxs-lookup"><span data-stu-id="646a4-109">Remarks</span></span>

<span data-ttu-id="646a4-110">Si la lecture est suspendue ou arrêtée et que [**EnableResetOnStop**](enableresetonstop-property.md) a la valeur true, l’appel de **Play** reprendra la lecture à la vitesse normale à l’emplacement actuel.</span><span class="sxs-lookup"><span data-stu-id="646a4-110">If playback is paused or stopped and [**EnableResetOnStop**](enableresetonstop-property.md) is true, then calling **Play** will resume playback at normal speed at the current location.</span></span> <span data-ttu-id="646a4-111">Si la lecture est arrêtée et que **EnableResetOnStop** a la valeur false, l’appel de **Play** entraîne la lecture du disque au début du premier titre.</span><span class="sxs-lookup"><span data-stu-id="646a4-111">If playback is stopped and **EnableResetOnStop** is false, then calling **Play** will cause the disc to start playing at the beginning of the first title.</span></span>

## <a name="see-also"></a><span data-ttu-id="646a4-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="646a4-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="646a4-113">**Sort**</span><span class="sxs-lookup"><span data-stu-id="646a4-113">**Resume**</span></span>](resume-method.md)
</dt> </dl>

 

 



