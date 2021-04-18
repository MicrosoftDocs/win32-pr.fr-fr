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
ms.openlocfilehash: 698b4b6c202ed157737b20296976a282c7f97ba3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106509228"
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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





