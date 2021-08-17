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
ms.openlocfilehash: a2793a67e6dee60c20c613b32b96bb2dda76907b13bd5e7a9c71add86d2c35a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461899"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





