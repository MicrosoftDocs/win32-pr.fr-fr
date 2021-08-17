---
description: 'L’énumération AudioDeviceProperty est utilisée par les méthodes ITAudioDeviceControl :: GetRange, ITAudioDeviceControl :: obten et ITAudioDeviceControl :: Set pour indiquer la propriété qui est adressée.'
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: Énumération AudioDeviceProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a634caa627f5d518e8783ce056e89a69931aa981466754a9d320f36787186f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948791"
---
# <a name="audiodeviceproperty-enumeration"></a>Énumération AudioDeviceProperty

\[cette énumération n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’énumération **AudioDeviceProperty** est utilisée par les méthodes [**ITAudioDeviceControl :: GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl :: obten**](itaudiodevicecontrol-get.md)et [**ITAudioDeviceControl :: Set**](itaudiodevicecontrol-set.md) pour indiquer la propriété qui est adressée.

## <a name="syntax"></a>Syntaxe


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice \_ DuplexMode**
</dt> <dd>

Indique que le mode duplex de l’appareil est en cours de définition ou de récupération.

</dd> <dt>

<span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice \_ AutomaticGainControl**
</dt> <dd>

Indique que le contrôle du gain automatique de l’appareil est en cours de définition ou de récupération.

</dd> <dt>

<span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice \_ AcousticEchoCancellation**
</dt> <dd>

Indique que les propriétés d’annulation de l’écho acoustique de l’appareil sont en cours de définition ou de récupération.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                       |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITAudioDeviceControl :: GetRange**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**ITAudioDeviceControl :: obtient**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**ITAudioDeviceControl :: Set**](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




