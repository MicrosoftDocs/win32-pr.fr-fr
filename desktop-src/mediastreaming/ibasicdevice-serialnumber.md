---
title: IBasicDevice SerialNumber, méthode
description: Récupère le numéro de série de l’appareil.
ms.assetid: 238A5999-0E8B-4462-AFCF-790DB58CFCB4
keywords:
- Méthode SerialNumber API de diffusion multimédia en continu
- SerialNumber méthode SerialNumber API de diffusion multimédia en continu, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode SerialNumber
topic_type:
- apiref
api_name:
- IBasicDevice.SerialNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f24fad2e74c3ec2a5b489d8f5dd57265ea6d21bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312487"
---
# <a name="ibasicdeviceserialnumber-method"></a>IBasicDevice :: SerialNumber, méthode

Récupère le numéro de série de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SerialNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers le numéro de série de l’appareil.

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

 

 





