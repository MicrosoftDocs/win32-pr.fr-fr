---
description: La \_ \_ propriété DeviceFormat AudioEngine spécifie le format de l’appareil, qui est le format que l’utilisateur a sélectionné pour le flux de données qui circule entre le moteur audio et l’appareil de point de terminaison audio lorsque l’appareil fonctionne en mode partagé.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13245d23095c25173a894a7a4c7cc11b2cdc534f6ae7198508b725d0fd1cf0b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018327"
---
# <a name="pkey_audioengine_deviceformat"></a>\_AudioEngine \_ DeviceFormat

La **propriété \_ \_ DeviceFormat AudioEngine** spécifie le format de l’appareil, qui est le format que l’utilisateur a sélectionné pour le flux de données qui circule entre le moteur audio et l’appareil de point de terminaison audio lorsque l’appareil fonctionne en mode partagé. Ce format peut ne pas être le meilleur format par défaut qu’une application en mode exclusif utilise. En règle générale, une application en mode exclusif détecte un format d’appareil approprié en effectuant un certain nombre d’appels à la méthode [**IAudioClient :: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) . Pour plus d’informations, consultez [formats de périphérique](device-formats.md).

Le membre **VT** de la structure **PROPVARIANT** est défini sur l' \_ objet BLOB VT.

Le membre **BLOB** de la structure **PROPVARIANT** est une structure de type **BLOB** qui contient deux membres. BLOB de membre **. cbSize** est une **valeur DWORD** qui spécifie le nombre d’octets dans la description de format. BLOB de membre **. pBlobData** pointe vers une structure **WAVEFORMATEX** qui contient la description de format. pour plus d’informations sur les **objets BLOB**, consultez la documentation SDK Windows. pour plus d’informations sur **WAVEFORMATEX**, consultez la documentation Windows DDK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés du point de terminaison audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriétés audio principales](core-audio-properties.md)
</dt> </dl>

 

 




