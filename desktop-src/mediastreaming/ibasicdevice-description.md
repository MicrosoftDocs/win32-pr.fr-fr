---
title: IBasicDevice, méthode de description
description: Récupère une description de l’appareil.
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- Méthode de description API de diffusion multimédia en continu
- Méthode de description API de diffusion multimédia en continu, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode de description
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f094246d1424c458e624d4a49358b63a84b9b7d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196760"
---
# <a name="ibasicdevicedescription-method"></a>IBasicDevice ::D méthode escription

Récupère une description de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers la description de l’appareil.

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

 

 





