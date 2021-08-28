---
description: Spécifie le profil et le niveau audio d’un flux de codage audio avancé (AAC).
ms.assetid: 87fa1127-46ca-4b83-a3b5-99253af22ba0
title: Attribut MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89934c55ff07124c28952c621513ddd4fd8db504c6e9df7cc6094f8ba7b875ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104565"
---
# <a name="mf_mt_aac_audio_profile_level_indication-attribute"></a>\_Attribut d' \_ \_ indication du \_ niveau de profil audio \_ MF MT AAC \_

Spécifie le profil et le niveau audio d’un flux de codage audio avancé (AAC).

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S'applique à

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Remarques

Cet attribut contient la valeur du champ **audioProfileLevelIndication** , tel que défini par la norme ISO/IEC 14496-3.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




