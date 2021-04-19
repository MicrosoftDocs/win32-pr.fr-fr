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
ms.openlocfilehash: c0bb39e03a9788e0c444f682b61d39fc1c65781b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535134"
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

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))
</dt> </dl>

 

