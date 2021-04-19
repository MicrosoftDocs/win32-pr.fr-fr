---
description: La méthode GetRange récupère la plage de valeurs valides pour une propriété de périphérique audio donnée.
ms.assetid: df8985f4-8153-4f32-a90c-a5eb7c76b3c7
title: 'ITAudioDeviceControl :: GetRange, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbf5bf36d4ec754440e1612f2e228c495d165c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532768"
---
# <a name="itaudiodevicecontrolgetrange-method"></a>ITAudioDeviceControl :: GetRange, méthode

\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **GetRange** récupère la plage de valeurs valides pour une [**propriété de périphérique audio**](audiodeviceproperty.md)donnée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Propriété* \[ dans\]
</dt> <dd>

Membre de l’énumération [**AudioDeviceProperty**](audiodeviceproperty.md) .

</dd> <dt>

*plMin* \[ à\]
</dt> <dd>

Valeur minimale valide pour la propriété d’entrée.

</dd> <dt>

*plMax* \[ à\]
</dt> <dd>

Valeur maximale valide pour la propriété d’entrée.

</dd> <dt>

*plSteppingDelta* \[ à\]
</dt> <dd>

Incrément par lequel la valeur de la propriété peut être augmentée ou diminuée.

</dd> <dt>

*plDefault* \[ à\]
</dt> <dd>

Valeur par défaut du paramètre de *propriété* .

</dd> <dt>

*plFlags* \[ à\]
</dt> <dd>

Valeur de l’énumération [**TAPIControlFlags**](tapicontrolflags.md) indiquant comment la valeur de la *propriété* est contrôlée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                         |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITAudioDeviceControl**](itaudiodevicecontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**AudioDeviceProperty**](audiodeviceproperty.md)
</dt> </dl>

 

 




