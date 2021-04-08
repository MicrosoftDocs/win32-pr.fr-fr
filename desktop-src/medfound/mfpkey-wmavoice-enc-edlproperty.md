---
description: Spécifie les portions de contenu à encoder en musique par le codec vocal.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: MFPKEY_WMAVOICE_ENC_EDL, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f3ac85ebd3a0542fbcf6554205d0b2f2623957c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755308"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a>\_ \_ Propriété EDL MFPKEY WMAVOICE enc \_

Spécifie les portions de contenu à encoder en musique par le codec vocal.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMACVoiceBuffer g

## <a name="data-type"></a>Type de données

VT \_ BSTR

## <a name="default-value"></a>Valeur par défaut

Pas de valeur par défaut. Si cette propriété n’est pas définie, le codec utilise la valeur de la propriété [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) pour déterminer le mode d’encodage du contenu.

## <a name="remarks"></a>Notes

Vous pouvez utiliser cette propriété si le mode automatique du codec ne donne pas de résultats satisfaisants.

Cette valeur est une chaîne délimitée par des virgules contenant au moins quatre entiers. Le premier entier est le numéro de version ; Utilisez toujours 1 pour cette valeur. Le deuxième entier est le nombre de sections qui doivent être encodées en tant que musique. Le deuxième entier est un nombre de paires de valeurs représentant des plages en millisecondes, une paire pour chaque section de contenu qui doit être encodée en musique.

Par exemple, « 1, 2100200500600 » indique à l’encodeur d’utiliser la version 1 avec 2 sections de musique. La première section musicale commence à 100 ms et se termine à 200 ms. La deuxième section musique commence à 500 ms et se termine à 600 ms.

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

 

 




