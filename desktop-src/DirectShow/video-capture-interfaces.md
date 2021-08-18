---
description: Interfaces de capture vidéo
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Interfaces de capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfee9807a94f381fef3a294dcd405de6fe8b67fafef3ace562309fe5e10d2ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633059"
---
# <a name="video-capture-interfaces"></a>Interfaces de capture vidéo

ces interfaces prennent en charge la capture vidéo, à l’aide des périphériques WDM (microsoft® Windows® Driver Model) ou des appareils microsoft® video pour Windows (VFW) hérités.



| Interface                                                        | Description                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMAnalogVideoDecoder**](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | Contrôlez la numérisation vidéo sur une carte de capture vidéo WDM.                                                      |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | Contrôler la façon dont un code confidentiel alloue des mémoires tampons.                                                                         |
| [**IAMCopyCaptureFileProgress**](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | Interface de rappel pour recevoir la progression d’une opération de copie de fichier.                                         |
| [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | Créez une connexion matérielle entre une source WDM Audio ou vidéo et un périphérique de capture WDM.                   |
| [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | Interrogez un filtre de capture sur les performances de capture.                                                            |
| [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | Contrôler les heures de démarrage et d’arrêt des flux individuels.                                                      |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | Interrogez et définissez le format de sortie du filtre de capture.                                                            |
| [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | Affiche les boîtes de dialogue fournies par les pilotes de capture VFW.                                                    |
| [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | Contrôler l’image à partir d’un appareil de capture.                                                                   |
| [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | Ajustez les qualités d’un signal vidéo, telles que la luminosité, le contraste, la teinte, la saturation, la gamma et la netteté. |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | Créer des graphiques de filtre pour la capture vidéo.                                                                       |
| [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | Spécifiez le nom et les attributs d’un fichier de sortie.                                                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces de contrôle de périphérique externe](external-device-control-interfaces.md)
</dt> <dt>

[Capture vidéo](video-capture.md)
</dt> </dl>

 

 



