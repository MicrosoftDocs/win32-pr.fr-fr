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
ms.openlocfilehash: a69f0671c82363ff61179c0120b3db8f6e755de9
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383228"
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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





