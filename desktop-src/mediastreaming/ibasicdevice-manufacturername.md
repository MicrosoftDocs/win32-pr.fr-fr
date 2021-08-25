---
title: Méthode IBasicDevice ManufacturerName
description: Récupère le nom du fabricant de l’appareil.
ms.assetid: F04400C9-02FC-4CB5-B355-A7E84BECD098
keywords:
- API de diffusion multimédia en continu de méthode ManufacturerName
- API de diffusion multimédia en continu de méthode ManufacturerName, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode ManufacturerName
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 453e11fc547998b6dc3e39017684c30cacd205c0c17b21846925d4de472f43a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011829"
---
# <a name="ibasicdevicemanufacturername-method"></a>IBasicDevice :: ManufacturerName, méthode

Récupère le nom du fabricant de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ManufacturerName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers le nom du fabricant de l’appareil.

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

 

 





