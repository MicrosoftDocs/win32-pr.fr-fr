---
title: IBasicDevice ModelName, méthode
description: Récupère le nom du modèle de l’appareil.
ms.assetid: 8F871E89-97C1-4788-83AB-B7E0D8D6E0B5
keywords:
- API de diffusion multimédia en continu de la méthode ModelName
- Méthode ModelName API de diffusion multimédia en continu, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode ModelName
topic_type:
- apiref
api_name:
- IBasicDevice.ModelName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e486b372b2108bc85153f416032ef6bfbe8a397
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106510042"
---
# <a name="ibasicdevicemodelname-method"></a>IBasicDevice :: ModelName, méthode

Récupère le nom du modèle de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ModelName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers le nom du modèle de l’appareil.

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

 

 





