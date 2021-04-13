---
title: Obtention d’informations sur les compresseurs et les décompresseurs
description: Obtention d’informations sur les compresseurs et les décompresseurs
ms.assetid: 2f1edfd0-dd30-42ea-a5ae-24265d3f8af3
keywords:
- Video Compression Manager (VCM), obtention d’informations sur les compresseurs
- VCM (Video Compression Manager), obtention d’informations sur les compresseurs
- ICGetInfo fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874793233ef0aec4de5b372573fb8dcd79f5d875
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379723"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a><span data-ttu-id="b02e6-106">Obtention d’informations sur les compresseurs et les décompresseurs</span><span class="sxs-lookup"><span data-stu-id="b02e6-106">Obtaining Information About Compressors and Decompressors</span></span>

<span data-ttu-id="b02e6-107">L’exemple suivant utilise la fonction [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) pour obtenir des informations sur un compresseur ou un décompresseur.</span><span class="sxs-lookup"><span data-stu-id="b02e6-107">The following example uses the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function to obtain information about a compressor or decompressor.</span></span>


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



<span data-ttu-id="b02e6-108">L’exemple suivant utilise les macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) et [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) pour obtenir les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="b02e6-108">The following example uses the [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) and [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macros to obtain the default values.</span></span>


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



<span data-ttu-id="b02e6-109">L’exemple suivant utilise les macros [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) et [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) pour afficher une boîte de dialogue à propos de pour le compresseur ou le décompresseur, si la boîte de dialogue existe.</span><span class="sxs-lookup"><span data-stu-id="b02e6-109">The following example uses the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) and [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macros to display an About dialog box for the compressor or decompressor, if the dialog box exists.</span></span>


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




