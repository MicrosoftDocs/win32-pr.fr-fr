---
title: Méthode IBasicDevice CanWakeDevices
description: Récupère une valeur qui indique si l’appareil peut sortir de veille.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- API de diffusion multimédia en continu de méthode CanWakeDevices
- API de diffusion multimédia en continu de méthode CanWakeDevices, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode CanWakeDevices
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08a893ac880a426f604f2dc1c73173585e507cc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196763"
---
# <a name="ibasicdevicecanwakedevices-method"></a>IBasicDevice :: CanWakeDevices, méthode

Récupère une valeur qui indique si l’appareil peut sortir de veille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers une valeur booléenne qui est **true** si l’appareil peut sortir de veille.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





