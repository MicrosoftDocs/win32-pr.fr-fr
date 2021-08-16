---
title: Méthode de type IBasicDevice
description: Récupère une valeur d’énumération indiquant le type d’appareil de l’appareil DLNA.
ms.assetid: D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F
keywords:
- Méthode de type Media Streaming API
- Méthode de type Media Streaming API, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode de type
topic_type:
- apiref
api_name:
- IBasicDevice.Type
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 433b255615a3fb57d59589b09a4a8b3e0f4cec5c02115bc737041d1fd94a197f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100623"
---
# <a name="ibasicdevicetype-method"></a>IBasicDevice :: type, méthode

Récupère une valeur d’énumération indiquant le type d’appareil de l’appareil DLNA.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Type(
  [out] DeviceTypes *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers une valeur [**DeviceTypes**](devicetypes.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





