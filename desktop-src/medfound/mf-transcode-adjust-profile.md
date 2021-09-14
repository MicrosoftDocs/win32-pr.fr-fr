---
description: Indicateurs de profil qui définissent les paramètres de flux pour la topologie de transcodage. Les indicateurs sont définis dans l' \_ \_ énumération de l' \_ énumération des indicateurs de profil de transcodage MF \_ .
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: Attribut MF_TRANSCODE_ADJUST_PROFILE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd492cfc7981ca1a36a1cb54a440bec4783fe1b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313865"
---
# <a name="mf_transcode_adjust_profile-attribute"></a>\_Attribut de \_ profil d’ajustement de TRANScodage MF \_

Indicateurs de profil qui définissent les paramètres de flux pour la topologie de transcodage. Les indicateurs sont définis dans l’énumération de l’énumération des [**\_ \_ \_ \_ indicateurs de profil de transcodage MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) .

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Une application peut définir cet attribut au niveau du conteneur sur le profil de transcodage. Si cet attribut est défini, la fonction [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) modifie les attributs de flux lors de la génération de la topologie, en fonction de l’indicateur spécifié. Par exemple, si l’application spécifie l’indicateur d' **\_ \_ ajustement \_ \_ par défaut du profil de transcodage MF** , les paramètres de flux spécifiés par l’application sont utilisés pour créer le profil.

Pour le flux vidéo, la fréquence d’images est mise à jour en fonction de la source du média. Si l’application ne spécifie pas le mode entrelacé, le profil est mis à jour pour utiliser les trames progressives par défaut.

Si l’application spécifie l’indicateur de **modification de profil d' \_ ajustement de transcodage \_ \_ \_ \_ \_ MF** , les attributs de flux manquants sont copiés de la source du média d’entrée vers les paramètres de flux du profil de transcodage.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



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

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




