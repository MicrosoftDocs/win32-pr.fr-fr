---
description: Spécifie si les métadonnées sont écrites dans le fichier transcodé.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: Attribut MF_TRANSCODE_SKIP_METADATA_TRANSFER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201717"
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

## <a name="remarks"></a>Notes

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




