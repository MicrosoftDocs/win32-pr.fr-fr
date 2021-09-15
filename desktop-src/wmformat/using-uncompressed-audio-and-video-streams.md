---
title: Utilisation de l’audio et de la vidéo non compressés Flux
description: Utilisation de l’audio et de la vidéo non compressés Flux
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- flux, configuration de flux audio et vidéo non compressés
- codecs, configuration des flux audio et vidéo non compressés
- flux vidéo, non compressés
- flux audio, non compressés
- flux audio et vidéo non compressés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525152"
---
# <a name="using-uncompressed-audio-and-video-streams"></a>Utilisation de l’audio et de la vidéo non compressés Flux

Dans la plupart des cas, le support non compressé présente des exigences de stockage et de remise excessives, mais pour certains scénarios de lecture locale, le niveau de qualité est suffisamment important pour ne pas utiliser la compression.

Les paramètres d’un flux multimédia non compressé doivent refléter les paramètres du média source. Lors de la configuration d’un flux non compressé, vous devez calculer la vitesse de transmission du média et définir le flux de manière appropriée en appelant [**IWMStreamConfig :: SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate). Étant donné que les flux non compressés ne sont pas viables pour la diffusion en continu, vous devez toujours définir la fenêtre de mémoire tampon pour les flux de média non compressés sur zéro en appelant [**IWMStreamConfig :: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).

Les formats de pixels suivants sont pris en charge pour les flux vidéo non compressés :

-   WMMEDIASUBTYPE \_ RGB555
-   WMMEDIASUBTYPE \_ Rgb24
-   WMMEDIASUBTYPE \_ RGB32
-   WMMEDIASUBTYPE \_ I420
-   WMMEDIASUBTYPE \_ IYUV
-   WMMEDIASUBTYPE \_ YV12
-   WMMEDIASUBTYPE \_ YUY2
-   WMMEDIASUBTYPE \_ UYVY
-   WMMEDIASUBTYPE \_ YVYU

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration commune à tous les Flux**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuration de l’Flux audio**](configuring-audio-streams.md)
</dt> <dt>

[**Configuration de Flux**](configuring-streams.md)
</dt> <dt>

[**Configuration de la vidéo Flux**](configuring-video-streams.md)
</dt> </dl>

 

 




