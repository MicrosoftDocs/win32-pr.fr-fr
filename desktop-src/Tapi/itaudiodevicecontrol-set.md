---
description: La méthode Set définit la valeur d’une propriété de périphérique audio donnée.
ms.assetid: 701cdfd4-9241-408c-8497-3983018e7da0
title: 'ITAudioDeviceControl :: Set, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25aa3a6013ce79bdcea5345dcc00f52c96c8a8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532774"
---
# <a name="itaudiodevicecontrolset-method"></a>ITAudioDeviceControl :: Set, méthode

\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **Set** définit la valeur d’une [**propriété de périphérique audio**](audiodeviceproperty.md)donnée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Propriété* \[ dans\]
</dt> <dd>

Membre de l’énumération [**AudioDeviceProperty**](audiodeviceproperty.md) .

</dd> <dt>

*lValue* \[ dans\]
</dt> <dd>

Valeur souhaitée pour la propriété.

</dd> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Valeur de l’énumération [**TAPIControlFlags**](tapicontrolflags.md) indiquant comment la valeur de la *propriété* doit être contrôlée.

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

 

 




