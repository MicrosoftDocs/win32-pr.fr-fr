---
title: IBasicDevice ManufacturerUrl, méthode
description: Récupère l’URL du fabricant de l’appareil.
ms.assetid: E8372D15-D8B5-49E4-950A-96B4A88B0450
keywords:
- Méthode ManufacturerUrl API de diffusion multimédia en continu
- ManufacturerUrl, méthode, API de diffusion multimédia en continu, interface IBasicDevice
- API streaming de média de l’interface IBasicDevice, méthode ManufacturerUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 306b4c194d7354b071d4daaf223a17f977b38b44243adaef856f9acffbf49c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972338"
---
# <a name="ibasicdevicemanufacturerurl-method"></a>IBasicDevice :: ManufacturerUrl, méthode

Récupère l’URL du fabricant de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ManufacturerUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’URL du fabricant de l’appareil.

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

 

 





