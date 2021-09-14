---
description: Interfaces de capture vidéo
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Interfaces de capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c88ab86833a3570789dee311b36d49f382c9cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240564"
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

 

 



