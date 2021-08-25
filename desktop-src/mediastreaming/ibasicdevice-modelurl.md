---
title: Méthode IBasicDevice ModelUrl
description: Récupère l’URL du modèle de l’appareil.
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- API de diffusion multimédia en continu de méthode ModelUrl
- API de diffusion multimédia en continu de méthode ModelUrl, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode ModelUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7595af295b0d0bc565d79bf5450ee6c5c16b0da4f3baa4fcf636e4e5386920
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847649"
---
# <a name="ibasicdevicemodelurl-method"></a>IBasicDevice :: ModelUrl, méthode

Récupère l’URL du modèle de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’URL du modèle de l’appareil.

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

 

 





