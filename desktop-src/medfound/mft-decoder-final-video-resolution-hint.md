---
description: Spécifie la résolution de sortie finale de l’image décodée, après le traitement vidéo.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: Attribut MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847a2925f2249c741e9a45a1dcc4826a1cbe3d6bb12cda4d8017ee0fb5de0069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973138"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a>\_ \_ Attribut d' \_ indicateur de résolution vidéo \_ final \_ du décodeur MFT

Spécifie la résolution de sortie finale de l’image décodée, après le traitement vidéo.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Remarques

Cet attribut est pris en charge par certains décodeurs vidéo. Une application peut définir cet attribut pour indiquer la largeur et la hauteur de l’image après le traitement vidéo. Le décodeur peut utiliser ces informations pour optimiser le processus de décodage, en particulier si la taille de l’image finale est bien inférieure à la taille de l’image native. Par exemple, le décodeur peut ignorer un filtre hors boucle.

Les 32 bits de poids fort contiennent la largeur et les 32 inférieurs contiennent la hauteur.

Pour définir cet attribut :

1.  Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le décodeur pour recevoir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Appelez [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) pour ajouter l’attribut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




