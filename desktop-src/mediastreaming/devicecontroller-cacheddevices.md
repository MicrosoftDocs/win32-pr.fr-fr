---
title: Méthode DeviceController. CachedDevices
description: Récupère une collection de pointeurs d’interface IBasicDevice qui représente la vue mise en cache de tous les appareils DLNA détectables. | Méthode DeviceController. CachedDevices
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- API de diffusion multimédia en continu de méthode CachedDevices
- API de diffusion multimédia en continu de méthode CachedDevices, interface DeviceController
- API de diffusion multimédia en continu de l’interface DeviceController, méthode CachedDevices
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86e2c4209649450fb3a8df46cde151a0b9899cd26e58bfc0b35fd7ac6e7d02b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236359"
---
# <a name="devicecontrollercacheddevices-method"></a>Méthode DeviceController. CachedDevices

Récupère une collection de pointeurs d’interface [**IBasicDevice**](ibasicdevice.md) qui représente la vue mise en cache de tous les appareils DLNA détectables.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit une collection énumérable de pointeurs d’interface [**IBasicDevice**](ibasicdevice.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))
</dt> </dl>

 

