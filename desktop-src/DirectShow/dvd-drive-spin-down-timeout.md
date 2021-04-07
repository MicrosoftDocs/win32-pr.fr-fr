---
description: Délai d’attente de Spin Down du lecteur DVD
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: Délai d’attente de Spin Down du lecteur DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda6853830ee7289e529d029c78fe4e56e4a0e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846606"
---
# <a name="dvd-drive-spin-down-timeout"></a><span data-ttu-id="9b0ab-103">Délai d’attente de Spin Down du lecteur DVD</span><span class="sxs-lookup"><span data-stu-id="9b0ab-103">DVD Drive Spin Down Timeout</span></span>

<span data-ttu-id="9b0ab-104">Sur les ordinateurs portables, pour économiser la batterie, il peut être souhaitable de réduire la durée pendant laquelle un lecteur de DVD continue de tourner une fois que l’utilisateur a suspendu la lecture.</span><span class="sxs-lookup"><span data-stu-id="9b0ab-104">On laptop computers, to conserve battery life it may be desirable to reduce the length of time that a DVD drive will continue to spin after the user has paused playback.</span></span> <span data-ttu-id="9b0ab-105">Par défaut, le navigateur DVD garde le disque tourner pendant deux minutes.</span><span class="sxs-lookup"><span data-stu-id="9b0ab-105">By default, the DVD Navigator keeps the disc spinning for two minutes.</span></span> <span data-ttu-id="9b0ab-106">Cette valeur peut être modifiée dans le Registre Windows sous cette clé :</span><span class="sxs-lookup"><span data-stu-id="9b0ab-106">This value can be modified in the Windows Registry under this key:</span></span>


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



<span data-ttu-id="9b0ab-107">where</span><span class="sxs-lookup"><span data-stu-id="9b0ab-107">where</span></span>


```
Sec
```



<span data-ttu-id="9b0ab-108">durée de Spin Down en secondes.</span><span class="sxs-lookup"><span data-stu-id="9b0ab-108">is the spin down time in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b0ab-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b0ab-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b0ab-110">Annexes</span><span class="sxs-lookup"><span data-stu-id="9b0ab-110">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 



