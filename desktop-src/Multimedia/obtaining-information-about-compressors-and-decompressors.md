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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119582"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a>Obtention d’informations sur les compresseurs et les décompresseurs

L’exemple suivant utilise la fonction [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) pour obtenir des informations sur un compresseur ou un décompresseur.


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



L’exemple suivant utilise les macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) et [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) pour obtenir les valeurs par défaut.


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



L’exemple suivant utilise les macros [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) et [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) pour afficher une boîte de dialogue à propos de pour le compresseur ou le décompresseur, si la boîte de dialogue existe.


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




