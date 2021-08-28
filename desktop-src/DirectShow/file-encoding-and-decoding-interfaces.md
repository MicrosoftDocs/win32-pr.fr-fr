---
description: Interfaces d’encodage et de décodage de fichier
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Interfaces d’encodage et de décodage de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6654497b0d2407666b286fb74f06a91e66834cfb963b62b7e22eb5755fa30b0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639659"
---
# <a name="file-encoding-and-decoding-interfaces"></a>Interfaces d’encodage et de décodage de fichier

Ces interfaces prennent en charge l’encodage et le décodage de fichier.



| Interface                                                    | Description                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | Récupérez les métadonnées d’un flux de données, telles que l’auteur et le titre.                                              |
| [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | Déterminer la progression d’une opération d’ouverture de fichier.                                                             |
| [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | Interroge et définit l’heure d’analyse de la position actuelle dans un flux MPEG.                                     |
| [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | Contrôlez les flux logiques lus et récupérez les informations les concernant.                               |
| [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | Affiche les boîtes de dialogue fournies par les codecs VFW.                                                                 |
| [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | Définissez les paramètres de compression vidéo.                                                                            |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | Contrôler la façon dont le filtre de l' [enregistreur ASF WM](wm-asf-writer-filter.md) écrit des fichiers ASF (Advanced Systems Format). |
| [**IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | Contrôler la façon dont le filtre de [multiplexeur](avi-mux-filter.md) de fichier AVI écrit des fichiers AVI.                                       |
| [**IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | Configurez l’entrelacement lorsque le filtre multiplex MUX écrit des fichiers AVI.                                             |
| [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | Définissez la résolution d’encodage sur le filtre d' [encodeur vidéo DV](dv-video-encoder-filter.md) .                   |
| [**IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | Rétrograder la fréquence d’images sur un flux vidéo numérique (DV)                                                      |
| [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | Définissez la résolution du décodage sur le filtre de décodage [vidéo DV](dv-video-decoder-filter.md) .                   |
| [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | Définissez et récupérez des blocs d’informations et d’extraction dans des flux AVI.                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 



