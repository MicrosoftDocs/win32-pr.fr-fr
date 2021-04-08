---
description: La méthode PlayForwards démarre la lecture en avant à partir de l’emplacement actuel à la vitesse spécifiée.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Méthode PlayForwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d49d8d6d80613c4dd5b2b8a374002b37d9baa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746796"
---
# <a name="playforwards-method"></a><span data-ttu-id="936d2-103">Méthode PlayForwards</span><span class="sxs-lookup"><span data-stu-id="936d2-103">PlayForwards Method</span></span>

> [!Note]  
> <span data-ttu-id="936d2-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="936d2-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="936d2-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="936d2-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="936d2-106">La `PlayForwards` méthode commence la lecture en avant à partir de l’emplacement actuel à la vitesse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="936d2-106">The `PlayForwards` method starts forward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="936d2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="936d2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="936d2-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span><span class="sxs-lookup"><span data-stu-id="936d2-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="936d2-109">Spécifie la vitesse à laquelle jouer en tant que valeur entière.</span><span class="sxs-lookup"><span data-stu-id="936d2-109">Specifies the speed at which to play as an Integer value.</span></span> <span data-ttu-id="936d2-110">Cette valeur est un multiplicateur — 1.0 est une vitesse de lecture normale ; 2,0 est à double vitesse, 0,5 à mi-vitesse, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="936d2-110">This value is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="936d2-111">Quand **nSpeed** n’est pas égal à 1,0, l’audio est muet et la sous-image est désactivée.</span><span class="sxs-lookup"><span data-stu-id="936d2-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="936d2-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="936d2-112">Return Value</span></span>

<span data-ttu-id="936d2-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="936d2-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="936d2-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="936d2-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936d2-115">**PlayBackwards**</span><span class="sxs-lookup"><span data-stu-id="936d2-115">**PlayBackwards**</span></span>](playbackwards-method.md)
</dt> </dl>

 

 



