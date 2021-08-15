---
title: Méthode IBasicDevice UniqueDeviceName
description: Récupère le nom d’appareil unique de l’appareil (UDN).
ms.assetid: 393EFF96-69E1-4081-905D-D8CC47B5FC4A
keywords:
- API de diffusion multimédia en continu de méthode UniqueDeviceName
- API de diffusion multimédia en continu de méthode UniqueDeviceName, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode UniqueDeviceName
topic_type:
- apiref
api_name:
- IBasicDevice.UniqueDeviceName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b70fbc2021cf717cdb49d8a222aa33ad4e9213f297364b81af065c3bbeaed99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972318"
---
# <a name="ibasicdeviceuniquedevicename-method"></a>IBasicDevice :: UniqueDeviceName, méthode

Récupère le nom d’appareil unique de l’appareil (UDN).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UniqueDeviceName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers le modèle de périphérique s UDN.

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

 

 





