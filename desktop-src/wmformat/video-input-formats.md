---
title: Formats d’entrée vidéo
description: Formats d’entrée vidéo
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- Windows Media Format SDK, formats d’entrée vidéo
- ASF (Advanced Systems Format), formats d’entrée vidéo
- ASF (format des systèmes avancés), formats d’entrée vidéo
- formats d’entrée vidéo
- Windows Media Format SDK, formats vidéo
- ASF (Advanced Systems Format), formats vidéo
- ASF (format des systèmes avancés), formats vidéo
- formats vidéo
- Windows Codec vidéo 9 Media, formats d’entrée vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225809"
---
# <a name="video-input-formats"></a>Formats d’entrée vidéo

l’enregistreur accepte les formats vidéo suivants comme entrée à compresser à l’aide du codec Windows Media Video 9 :

-   WMMEDIASUBTYPE \_ IYUV
-   WMMEDIASUBTYPE \_ I420
-   WMMEDIASUBTYPE \_ YV12
-   WMMEDIASUBTYPE \_ YUY2
-   WMMEDIASUBTYPE \_ UYVY
-   WMMEDIASUBTYPE \_ YVYU
-   WMMEDIASUBTYPE \_ YVU9
-   WMMEDIASUBTYPE \_ RGB32
-   WMMEDIASUBTYPE \_ Rgb24
-   WMMEDIASUBTYPE \_ RGB565
-   WMMEDIASUBTYPE \_ RGB555
-   WMMEDIASUBTYPE \_ RGB8

Vous devez toujours utiliser [**IWMWriter :: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) et [**IWMWriter :: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) pour énumérer les formats d’entrée disponibles et pour obtenir l’objet de propriétés de média d’entrée pour le format souhaité. Les objets de propriétés de média d’entrée vidéo doivent être modifiés pour refléter la taille de trame et la fréquence d’images de votre média d’entrée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Identificateurs de type de média**](media-type-identifiers.md)
</dt> <dt>

[**Types de médias**](media-types.md)
</dt> </dl>

 

 




