---
description: Spécifie si les métadonnées sont écrites dans le fichier transcodé.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: Attribut MF_TRANSCODE_SKIP_METADATA_TRANSFER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7874d7d8cc20bbf5222cd8fd2fa0ca938c0b597dbc42914ab809dad926968306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739421"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a>\_Attribut de \_ \_ transfert de métadonnées Skip de transcodage MF \_

Spécifie si les métadonnées sont écrites dans le fichier transcodé. Cet attribut de conteneur est stocké dans le profil de transcodage.

## <a name="data-type"></a>Type de données

**UINT32**

Les valeurs possibles pour l' \_ attribut de transfert de métadonnées d’omission de transcodage MF \_ \_ \_ sont décrites dans le tableau suivant.



| Valeur                                                                        | Signification                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Transfère automatiquement les métadonnées au niveau du fichier à partir du fichier source vers le fichier encodé.<br/> |
| <dl> <dt>1</dt> </dl> | Les métadonnées du fichier source ne sont pas écrites dans le fichier transcodé.<br/>                          |



 

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarques

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




