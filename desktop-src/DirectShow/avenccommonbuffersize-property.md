---
description: Spécifie la taille de la mémoire tampon utilisée pendant l’encodage. Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Propriété AVEncCommonBufferSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c677c483c320c9dceef391f45c5d8bf163eece0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111981"
---
# <a name="avenccommonbuffersize-property"></a>Propriété AVEncCommonBufferSize

Spécifie la taille de la mémoire tampon utilisée pendant l’encodage. Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonBufferSize**

## <a name="property-value"></a>Valeur de la propriété

Cette propriété a une plage de valeurs linéaire. Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange). Les plages de paramètres ne sont pas prises en charge pour les encodeurs de caméra H. 264 UVC 1,5.

## <a name="remarks"></a>Notes

Pour certains formats vidéo, la taille de la mémoire tampon est spécifiée en bits et, pour d’autres, elle est spécifiée en octets. Consultez les remarques ci-dessous pour obtenir des informations spécifiques.

Pour la vidéo MPEG, cette propriété définit la taille de la mémoire tampon du vérificateur de mémoire tampon vidéo (VBV). La taille de la mémoire tampon est en bits.

pour la vidéo H. 264 et Windows Media Video, la propriété définit la taille du décodeur de référence hypothétique (découverte du domaine). La taille de la mémoire tampon est en octets.

Pour les caméras de codage UVC 1,5 H264 –, la valeur CPB envoyée à l’encodeur de l’appareil photo doit être alignée sur 16 bits. La taille de la mémoire tampon est en octets.

Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

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

 

