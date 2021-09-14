---
description: Spécifie le format d’entrée actuel pour le décodeur.
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: Propriété AVDecCommonInputFormat (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7432d2a48727ec144d4206d4a11bfe65ce2c5d2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112098"
---
# <a name="avdeccommoninputformat-property"></a>Propriété AVDecCommonInputFormat

Spécifie le format d’entrée actuel pour le décodeur.

Cette propriété est en lecture seule.

## <a name="data-type"></a>Type de données

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecCommonInputFormat**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un **BSTR** qui contient la représentation sous forme de chaîne d’un GUID. Les GUID suivants sont définis.



| **GUID**                                            | Description                                    |
|-----------------------------------------------------|------------------------------------------------|
| **\_GUID CODECAPI \_ AVDecAudioInputAAC**              | Codage audio avancé (AAC)                    |
| **\_GUID CODECAPI \_ AVDecAudioInputDolbyDigitalPlus** | Audio Dolby Digital plus                       |
| **\_GUID CODECAPI \_ AVDecAudioInputDolby**            | Audio Dolby                                    |
| **\_GUID CODECAPI \_ AVDecAudioInputDTS**              | Fichier audio DTS                                      |
| **\_GUID CODECAPI \_ AVDecAudioInputHEAAC**            | High-Efficiency du codage audio avancé (HE-AAC) |
| **\_GUID CODECAPI \_ AVDecAudioInputMPEG**             | Audio MPEG                                     |
| **\_GUID CODECAPI \_ AVDecAudioInputPCM**              | Audio PCM                                      |
| **\_GUID CODECAPI \_ AVDecAudioInputWMA**              | Windows Media Audio                            |
| **\_GUID CODECAPI \_ AVDecAudioInputWMAPro**           | Windows Media Audio 9 Professional (WMA Pro)   |



 

## <a name="requirements"></a>Spécifications



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

 

 




