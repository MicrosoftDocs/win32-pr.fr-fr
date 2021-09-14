---
title: Méthode IBasicDevice ModelNumber
description: Récupère le numéro de modèle de l’appareil.
ms.assetid: C4199135-0C6C-4427-8152-224D7D29C270
keywords:
- API de diffusion multimédia en continu de méthode ModelNumber
- API de diffusion multimédia en continu de méthode ModelNumber, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode ModelNumber
topic_type:
- apiref
api_name:
- IBasicDevice.ModelNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8034e67e5f3c552f0af83678d75e33881f1318f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313505"
---
# <a name="ibasicdevicemodelnumber-method"></a>IBasicDevice :: ModelNumber, méthode

Récupère le numéro de modèle de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ModelNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers le numéro de modèle de l’appareil.

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

 

 





