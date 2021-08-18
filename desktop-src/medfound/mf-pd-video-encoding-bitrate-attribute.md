---
description: Spécifie la vitesse de transmission de l’encodage vidéo pour la présentation, en bits par seconde. Cet attribut s’applique aux descripteurs de présentation.
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: Attribut MF_PD_VIDEO_ENCODING_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de8c7e250ab446714a3d9afb2c7d07e0d3ac76a671bb50dcd46785368a77cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102905"
---
# <a name="mf_pd_video_encoding_bitrate-attribute"></a>\_Attribut de \_ \_ \_ débit binaire d’encodage vidéo MF PD

Spécifie la vitesse de transmission de l’encodage vidéo pour la présentation, en bits par seconde. Cet attribut s’applique aux descripteurs de présentation.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cet attribut est facultatif. Certains formats ont des schémas d’encodage plus complexes qui ne peuvent pas être résumés à l’aide de cet attribut. Pour les fichiers ASF (Advanced Systems Format), les attributs suivants décrivent collectivement la vitesse de transmission du codage :

-   [**\_vitesse de \_ \_ \_ \_ transmission maximale MF PD ASF FichierPropriétés**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [**\_vitesse de \_ \_ \_ transmission moyenne des \_ données EXTSTRMPROP \_ MF SD ASF**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [**\_vitesse de \_ \_ transmission de \_ \_ données Max \_ . ASF EXTSTRMPROP ASF**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [**\_vitesse de \_ \_ transmission de STREAMBITRATES MF SD ASF \_**](mf-sd-asf-streambitrates-bitrate-attribute.md)

Les formats tiers peuvent utiliser d’autres attributs personnalisés.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




