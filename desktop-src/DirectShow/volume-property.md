---
description: La propriété volume définit ou récupère le volume du haut-parleur pour la sortie du flux audio.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Volume, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9c85bc2d20a613e61d454f75b9663284188c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527807"
---
# <a name="volume-property"></a><span data-ttu-id="78a98-103">Volume, propriété</span><span class="sxs-lookup"><span data-stu-id="78a98-103">Volume Property</span></span>

> [!Note]  
> <span data-ttu-id="78a98-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="78a98-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="78a98-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="78a98-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="78a98-106">La `Volume` propriété définit ou récupère le volume du haut-parleur pour la sortie du flux audio.</span><span class="sxs-lookup"><span data-stu-id="78a98-106">The `Volume` property sets or retrieves the speaker volume for the audio stream output.</span></span>

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a><span data-ttu-id="78a98-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="78a98-107">Return Value</span></span>

<span data-ttu-id="78a98-108">Retourne le niveau de volume en tant qu’atténuation en décibels sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="78a98-108">Returns the volume level as attenuation in decibels as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="78a98-109">Notes</span><span class="sxs-lookup"><span data-stu-id="78a98-109">Remarks</span></span>

<span data-ttu-id="78a98-110">Cette propriété est en lecture/écriture avec 0 comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="78a98-110">This property is read/write with a default value of 0.</span></span> <span data-ttu-id="78a98-111">Le volume complet est 0, et 10 000 est un silence ; l’échelle est logarithmique.</span><span class="sxs-lookup"><span data-stu-id="78a98-111">Full volume is 0, and 10,000 is silence; the scale is logarithmic.</span></span> <span data-ttu-id="78a98-112">Multipliez le niveau de décibel souhaité par 100 (par exemple 10 000 = 100 dB).</span><span class="sxs-lookup"><span data-stu-id="78a98-112">Multiply the desired decibel level by 100 (for example 10,000 = 100 dB).</span></span>

 

 



