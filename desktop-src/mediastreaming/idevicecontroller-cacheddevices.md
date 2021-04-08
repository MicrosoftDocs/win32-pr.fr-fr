---
title: Méthode IDeviceController CachedDevices
description: Récupère une collection de pointeurs d’interface IBasicDevice qui représente la vue mise en cache de tous les appareils DLNA détectables. | Méthode IDeviceController CachedDevices
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- API de diffusion multimédia en continu de méthode CachedDevices
- API de diffusion multimédia en continu de méthode CachedDevices, interface IDeviceController
- API de diffusion multimédia en continu de l’interface IDeviceController, méthode CachedDevices
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69be1faea277fa8999ae5ddf3658aaa61a1116b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953768"
---
# <a name="idevicecontrollercacheddevices-method"></a>IDeviceController :: CachedDevices, méthode

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

[**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

