---
description: La propriété AudioEndpoint de la valeur de la valeur de la propriété GUID de la propriété de la \_ \_ valeur de fichier
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357531a76316381e9ae39f867a5b6cfa0a055a04f41b0cba5fab95fcccbcc7fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104359"
---
# <a name="pkey_audioendpoint_guid"></a>GUID de AudioEndpoint de la \_ \_

La **propriété \_ AudioEndpoint \_** de la valeur de la valeur de la propriété GUID de la propriété de la valeur de fichier La valeur de la propriété est un GUID que le client peut fournir comme identificateur d’appareil à la fonction **DirectSoundCreate** ou **DIRECTSOUNDCAPTURECREATE** dans l’API DirectSound. Cette valeur identifie de façon unique l’appareil de point de terminaison audio sur tous les périphériques de point de terminaison audio du système. Pour plus d’informations sur DirectSound, consultez la documentation du kit de développement logiciel (SDK) DirectX.

Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ LPWStr.

Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient un GUID qui identifie l’appareil de point de terminaison audio dans DirectSound.

Comme expliqué précédemment, l' [API MMDevice](mmdevice-api.md) prend en charge les [rôles d’appareil](device-roles.md). Bien que DirectSound ne prenne pas directement en charge les rôles d’appareil, un client DirectSound peut utiliser la \_ \_ propriété GUID AudioEndpoint de type de périphérique pour sélectionner un appareil de rendu ou de capture DirectSound en fonction de son rôle d’appareil.

Par exemple, une application DirectSound effectue les étapes suivantes pour créer un appareil DirectSound qui correspond à l’appareil de point de terminaison de rendu auquel l’utilisateur a affecté le rôle eMultimedia :

1.  Appelez la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) pour accéder à l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de l’appareil de point de terminaison de rendu qui a le rôle eMultimedia.
2.  Appelez la méthode [**IMMDevice :: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) pour obtenir l’interface **IPropertyStore** de l’appareil eMultimedia. pour plus d’informations sur **IPropertyStore**, consultez la documentation SDK Windows.
3.  Appelez la méthode **IPropertyStore :: GetValue** pour obtenir la valeur de la \_ \_ propriété GUID AudioEndpoint GUID.
4.  Convertit la valeur de propriété d’un GUID sous forme de chaîne en une structure GUID de 16 octets.
5.  Appelez la fonction **DirectSoundCreate** avec le GUID pour créer l’appareil avec le rôle eMultimedia.

> [!Note]  
> A-la **\_ AudioEndpoint \_ GUID** est une propriété en lecture seule, quel que soit le mode d’accès au stockage demandé par l’application dans [**IMMDevice :: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore). Si une application tente de définir une valeur à l’aide de **IPropertyStore :: SetValue**, cet appel échoue avec le \_ code d’erreur E ACCESSDENIED.

 

Notez que le GUID de 16 octets généré à l’étape 4 correspond au GUID de l’appareil qui identifie l’appareil lors de l’énumération de l’appareil DirectSound. La fonction **DirectSoundEnumerate** énumère les appareils de point de terminaison de rendu et la fonction **DirectSoundCaptureEnumerate** énumère les appareils de point de terminaison de capture. Dans les deux cas, le GUID du périphérique est le premier paramètre passé à la fonction de rappel d’énumération. Pour plus d’informations sur l’énumération DirectSound, consultez la documentation du kit de développement logiciel (SDK) DirectX.

Pour obtenir un exemple de code qui utilise \_ la \_ propriété GUID AudioEndpoint de la page de codes, consultez [rôles d’appareil pour les applications DirectSound](device-roles-for-directsound-applications.md).

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

 

 




