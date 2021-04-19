---
description: Spécifie la vitesse de transmission de l’encodage vidéo pour la présentation, en bits par seconde. Cet attribut s’applique aux descripteurs de présentation.
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: Attribut MF_PD_VIDEO_ENCODING_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477d0954b4db8fa11c1540153c096e42f6d255b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544322"
---
# <a name="mf_pd_video_encoding_bitrate-attribute"></a>\_Attribut de \_ \_ \_ débit binaire d’encodage vidéo MF PD

Spécifie la vitesse de transmission de l’encodage vidéo pour la présentation, en bits par seconde. Cet attribut s’applique aux descripteurs de présentation.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

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
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                        |
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

 

 




