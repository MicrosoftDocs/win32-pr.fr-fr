---
description: La méthode PlayBackwards démarre la lecture vers l’arrière à partir de l’emplacement actuel à la vitesse spécifiée.
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: Méthode PlayBackwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b396c3829569d3f3ad25f0c0e8718dfd23f268
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480593"
---
# <a name="playbackwards-method"></a><span data-ttu-id="1564d-103">Méthode PlayBackwards</span><span class="sxs-lookup"><span data-stu-id="1564d-103">PlayBackwards Method</span></span>

> [!Note]  
> <span data-ttu-id="1564d-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1564d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1564d-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1564d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1564d-106">La `PlayBackwards` méthode démarre la lecture vers l’arrière à partir de l’emplacement actuel à la vitesse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1564d-106">The `PlayBackwards` method starts backward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="1564d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1564d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1564d-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span><span class="sxs-lookup"><span data-stu-id="1564d-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="1564d-109">Spécifie la vitesse à laquelle jouer en tant que nombre.</span><span class="sxs-lookup"><span data-stu-id="1564d-109">Specifies the speed at which to play as a number.</span></span> <span data-ttu-id="1564d-110">Ce nombre est un multiplicateur : 1.0 est une vitesse de lecture normale ; 2,0 est à double vitesse, 0,5 à mi-vitesse, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="1564d-110">This number is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="1564d-111">Quand **nSpeed** n’est pas égal à 1,0, l’audio est muet et la sous-image est désactivée.</span><span class="sxs-lookup"><span data-stu-id="1564d-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1564d-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1564d-112">Return Value</span></span>

<span data-ttu-id="1564d-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="1564d-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="1564d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1564d-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1564d-115">**PlayForwards**</span><span class="sxs-lookup"><span data-stu-id="1564d-115">**PlayForwards**</span></span>](playforwards-method.md)
</dt> </dl>

 

 



