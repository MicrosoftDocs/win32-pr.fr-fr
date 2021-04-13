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
ms.openlocfilehash: 4b3103640fd49880dc5ae5ca881618ac1091de62
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380740"
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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





