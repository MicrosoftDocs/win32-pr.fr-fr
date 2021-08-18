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
ms.openlocfilehash: cfaf3ba8ca9c74d094aa8cdc15f4c190d6e5141fb11ff255b6e7682b667846d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972348"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





