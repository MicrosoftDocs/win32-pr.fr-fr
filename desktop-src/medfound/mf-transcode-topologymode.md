---
description: Spécifie pour une topologie de transcodage si le chargeur de topologie charge des transformations matérielles.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: Attribut MF_TRANSCODE_TOPOLOGYMODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e8715c135e074956af2280b8474172e94e69e1cca20cd01b020fc6dc79076c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663839"
---
# <a name="mf_transcode_topologymode-attribute"></a>\_Attribut TOPOLOGYMODE de transcodage MF \_

Spécifie pour une topologie de transcodage si le chargeur de topologie charge des transformations matérielles.

Le mode de topologie spécifie si les transformations matérielles (telles que les codecs matériels) peuvent être utilisées dans la topologie de transcodage. L’application peut stocker cet attribut dans un profil de transcodage en appelant [**IMFTranscodeProfile :: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).

## <a name="data-type"></a>Type de données

**[**MF \_ Transcodage \_ TOPOLOGYMODE \_ indicateurs**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarques

Cet attribut est facultatif. Elle doit avoir l’une des valeurs suivantes.



| Valeur                                              | Description                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_matériel TOPOLOGYMODE de transcodage MF \_ \_ \_ autorisé** | Le chargeur de topologie chargera les MFTs matériels, tels que les décodeurs matériels, lorsqu’ils sont disponibles.<br/> Le chargeur de topologie revient automatiquement au décodage logiciel si aucun décodeur matériel n’est trouvé, ou si un décodeur matériel ne parvient pas à se connecter pour une raison quelconque.<br/> |
| **MF \_ transcodage \_ TOPOLOGYMODE \_ logiciel \_ uniquement**    | Le chargeur de topologie chargera uniquement les MFTss logicielles, y compris les décodeurs logiciels.                                                                                                                                                                                                    |



 

La valeur par défaut est **MF \_ transcodage \_ TOPOLOGYMODE \_ Software \_ uniquement**.

Si le chargeur de topologie insère une table MFT matérielle dans la topologie, il définit l’attribut d' [ \_ attribut d' \_ \_ URL matériel \_ de l’énumération MFT](mft-enum-hardware-url-attribute.md) sur le nœud de topologie. Pour vérifier si une table MFT matérielle est présente, énumérez les nœuds dans la topologie résolue et vérifiez si cet attribut est présent.

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

[API de transcodage](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




