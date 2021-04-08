---
description: Spécifie le rôle d’appareil pour un périphérique de capture audio.
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: Attribut MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148ae6697151698eef58d3c0148de3ed81822a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034212"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a>Attribut \_ de \_ \_ \_ \_ rôle AUDCAP du type de source de l’attribut DEVSOURCE \_ MF

Spécifie le rôle d’appareil pour un périphérique de capture audio.

## <a name="data-type"></a>Type de données

**ERole** stocké en tant que **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Le type d’énumération **eRole** est documenté dans la documentation de l’API audio principale.

La valeur de l’attribut spécifie un rôle d’appareil. Cet attribut est utilisé avec les fonctions suivantes.

Cet attribut peut être utilisé comme entrée pour les fonctions [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) et [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . Si l’attribut est spécifié, la fonction crée une source de média qui utilise le périphérique de capture audio par défaut pour le rôle d’appareil spécifié.

Cet attribut peut également être utilisé comme entrée de la fonction [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) . Si l’attribut est spécifié, l’énumération est limitée au rôle d’appareil spécifié. En outre, chaque objet d’activation retourné par la fonction **MFEnumDeviceSources** contient cet attribut. L’attribut est ensuite utilisé en interne par l’objet d’activation lorsqu’il crée la source du média.

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

[Capture audio/vidéo](audio-video-capture.md)
</dt> <dt>

[Capturer les attributs de l’appareil](capture-device-attributes.md)
</dt> </dl>

 

 




