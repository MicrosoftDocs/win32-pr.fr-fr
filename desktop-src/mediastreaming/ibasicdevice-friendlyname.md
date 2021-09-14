---
title: IBasicDevice FriendlyName, méthode
description: Récupère le nom convivial de l’appareil.
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- Méthode FriendlyName API de diffusion multimédia en continu
- Méthode FriendlyName API de diffusion multimédia en continu, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode FriendlyName
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec2b2edfa3a98dfdbbdd1d236acb6e1f1433f141
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313510"
---
# <a name="ibasicdevicefriendlyname-method"></a>IBasicDevice :: FriendlyName, méthode

Récupère le nom convivial de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers le nom convivial de l’appareil.

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

 

 





