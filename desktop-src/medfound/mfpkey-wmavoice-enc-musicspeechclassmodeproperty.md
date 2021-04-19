---
description: Spécifie le mode du codec vocal.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9776c76f2a8863afe73626f5a2940de2c0ccb7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531833"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a>MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode, propriété

Spécifie le mode du codec vocal.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMACMusicSpeechClassMode g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

1

## <a name="remarks"></a>Notes

La valeur 1 indique au codec que le contenu est uniquement vocal, la valeur 2 le codec détermine le mode automatiquement et toute autre valeur informe le codec pour qu’il utilise le mode musique.

Si le mode automatique n’encode pas correctement la voix mixte et la musique, vous pouvez spécifier l’encodage pour des sections individuelles du fichier à l’aide de la propriété [ \_ \_ \_ EDL MFPKEY WMAVOICE enc](mfpkey-wmavoice-enc-edlproperty.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




