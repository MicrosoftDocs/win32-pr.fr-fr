---
description: Les fonctions suivantes se rapportent aux objets de type de média.
ms.assetid: 7d4f3581-8cb9-4d31-b2f7-c8fbde24cf2a
title: Fonctions d’assistance du type de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b488eb706338926aaffd3c3c4e13a5da4d1d004bd21dbbd1f5871c6d4818dae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827359"
---
# <a name="media-type-helper-functions"></a>Fonctions d’assistance du type de média

Les fonctions suivantes se rapportent aux objets de type de média.



| Fonction                                                                     | Description                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | Calcule la fréquence d’images à partir de la durée moyenne d’une image vidéo. |
| [**MFCalculateImageSize**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | Récupère la taille de l’image pour un format vidéo non compressé.            |
| [**MFCompareFullToPartialMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcomparefulltopartialmediatype)   | Compare un type de média complet à un type de média partiel.                   |
| [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype)                               | Crée un type de média vide.                                          |
| [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | Convertit une fréquence d’images vidéo en une durée de trame.                    |
| [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | Récupère le Stride de surface minimal pour un format vidéo.              |
| [**MFIsFormatYUV**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | Interroge si un code FOURCC ou une valeur **D3DFORMAT** est un format YUV. |
| [**MFValidateMediaTypeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfvalidatemediatypesize)                   | Valide la taille d’une mémoire tampon pour un bloc de format vidéo.              |
| [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)                                   | Crée un type de média qui encapsule un autre type de média.                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Conversions de type de média](media-type-conversions.md)
</dt> <dt>

[Types de médias](media-types.md)
</dt> </dl>

 

 



