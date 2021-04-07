---
description: La \_ \_ propriété DeviceFormat AudioEngine spécifie le format de l’appareil, qui est le format que l’utilisateur a sélectionné pour le flux de données qui circule entre le moteur audio et l’appareil de point de terminaison audio lorsque l’appareil fonctionne en mode partagé.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb80fefd59fbc4067ce4a075d27b88de3d96c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748901"
---
# <a name="pkey_audioengine_deviceformat"></a>\_AudioEngine \_ DeviceFormat

La **propriété \_ \_ DeviceFormat AudioEngine** spécifie le format de l’appareil, qui est le format que l’utilisateur a sélectionné pour le flux de données qui circule entre le moteur audio et l’appareil de point de terminaison audio lorsque l’appareil fonctionne en mode partagé. Ce format peut ne pas être le meilleur format par défaut qu’une application en mode exclusif utilise. En règle générale, une application en mode exclusif détecte un format d’appareil approprié en effectuant un certain nombre d’appels à la méthode [**IAudioClient :: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) . Pour plus d’informations, consultez [formats de périphérique](device-formats.md).

Le membre **VT** de la structure **PROPVARIANT** est défini sur l' \_ objet BLOB VT.

Le membre **BLOB** de la structure **PROPVARIANT** est une structure de type **BLOB** qui contient deux membres. BLOB de membre **. cbSize** est une **valeur DWORD** qui spécifie le nombre d’octets dans la description de format. BLOB de membre **. pBlobData** pointe vers une structure **WAVEFORMATEX** qui contient la description de format. Pour plus d’informations sur les **objets BLOB**, consultez la documentation SDK Windows. Pour plus d’informations sur **WAVEFORMATEX**, consultez la documentation de Windows DDK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés du point de terminaison audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriétés audio principales](core-audio-properties.md)
</dt> </dl>

 

 




