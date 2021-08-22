---
description: Spécifie le format de sortie du décodeur.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Propriété AVDecCommonOutputFormat (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 129f9a1171c5870eab243108fc0ed6992be4993b886cbd36d72fe91988f321b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586749"
---
# <a name="avdeccommonoutputformat-property"></a>Propriété AVDecCommonOutputFormat

Spécifie le format de sortie du décodeur.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecCommonOutputFormat**

## <a name="property-value"></a>Valeur de la propriété



| GUID                                                               | Description                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM                        | Audio PCM, utilisant un nombre quelconque de canaux                                                                                                                                                                             |
| \_Casque CODECAPI GUID \_ AVDecAudioOutputFormat \_ PCM \_            | Audio stéréo stéréo, à l’aide de gauche uniquement/droit uniquement (Lo/RO) downmix                                                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ stéréo \_ automatique          | Audio stéréo PCM, en utilisant la sélection automatique du mode stéréo downmix (Lo/RO ou lt/RT). Vous pouvez utiliser cette valeur pour les formats audio dans lesquels le flux d’entrée définit le mode downmix préféré, tel que Dolby AC-3. |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ stéréo \_ MatrixEncoded | Audio stéréo stéréo, utilisant des downmix stéréo encodées en matrice (LT/RT)                                                                                                                                                       |
| \_Binaire CODECAPI GUID \_ AVDecAudioOutputFormat \_ SPDIF \_           | S/PDIF (format de flux binaire compressé Sony/Philips Digital Interface), tel que défini par IEC-60958                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ PCM                 | Stéréo PCM S/PDIF, comme défini par IEC-60958                                                                                                                                                                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications Windows 2000 Professional \[ desktop apps \| UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | applications de bureau Windows 2000 Server apps-applications \[ \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




