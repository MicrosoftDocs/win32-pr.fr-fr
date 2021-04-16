---
description: Spécifie le format de sortie du décodeur.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Propriété AVDecCommonOutputFormat (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b69c536b3c9f1bf75e2a5741d0cdd16569b3dd8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522479"
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
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




