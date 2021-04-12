---
description: Spécifie le schéma d’encodage.
ms.assetid: a26951d6-67fb-43fb-849f-331416e9d7c2
title: Propriété AVEncCodecType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8643c0624b7d82381e2008f2adbd6804e9af9881
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317774"
---
# <a name="avenccodectype-property"></a>Propriété AVEncCodecType

Spécifie le schéma d’encodage.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCodecType**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un **BSTR** qui contient la représentation sous forme de chaîne d’un GUID. Les GUID suivants sont définis.



| GUID                                      | Description                                        |
|-------------------------------------------|----------------------------------------------------|
| \_GUID CODECAPI \_ AVEncDolbyDigitalConsumer | Audio Dolby Digital Consumer                       |
| \_GUID CODECAPI \_ AVEncDolbyDigitalPlus     | Audio Dolby Digital plus                           |
| \_GUID CODECAPI \_ AVEncDolbyDigitalPro      | Audio Dolby Digital Pro                            |
| \_GUID CODECAPI \_ AVEncDTS                  | Fichier audio DTS                                          |
| \_GUID CODECAPI \_ AVEncDTSHD                | DTS-HD Audio                                       |
| \_GUID CODECAPI \_ AVEncDV                   | Vidéo DV                                           |
| \_GUID CODECAPI \_ AVEncH264Video            | Vidéo H. 264                                        |
| \_GUID CODECAPI \_ AVEncMLP                  | Remplissage du MLP (méridien de perte de données)              |
| \_GUID CODECAPI \_ AVEncMPEG1Audio           | MPEG-1 audio                                       |
| \_GUID CODECAPI \_ AVEncMPEG1Video           | Vidéo MPEG-1                                       |
| \_GUID CODECAPI \_ AVEncMPEG2Audio           | Audio MPEG-2                                       |
| \_GUID CODECAPI \_ AVEncMPEG2Video           | Vidéo MPEG-2                                       |
| \_GUID CODECAPI \_ AVEncPCM                  | Audio PCM                                          |
| \_GUID CODECAPI \_ AVEncSDDS                 | Audio Sony Digital Digital Sound (SDD)            |
| \_GUID CODECAPI \_ AVEncWMALossless          | Audio Windows Media Audio 9 sans perte               |
| \_GUID CODECAPI \_ AVEncWMAPro               | Audio Windows Media Audio 9 professionnel (WMA Pro) |
| \_GUID CODECAPI \_ AVEncWMAVoice             | Audio vocal Windows Media Audio 9                  |
| \_GUID CODECAPI \_ AVEncWMV                  | Windows Media Video                                |
| \_GUID CODECAPI \_ AVEndMPEG4Video           | Vidéo MPEG-4                                       |



 

## <a name="remarks"></a>Notes

Les applications peuvent définir cette propriété pour spécifier le schéma d’encodage à utiliser. Les codecs peuvent également retourner cette propriété en tant que fonctionnalité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




