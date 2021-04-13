---
title: Méthode IBasicDevice ModelUrl
description: Récupère l’URL du modèle de l’appareil.
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- API de diffusion multimédia en continu de méthode ModelUrl
- API de diffusion multimédia en continu de méthode ModelUrl, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode ModelUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f616d1a122f5fe6025c80742df61eb86d41514a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312451"
---
# <a name="ibasicdevicemodelurl-method"></a>IBasicDevice :: ModelUrl, méthode

Récupère l’URL du modèle de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’URL du modèle de l’appareil.

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

 

 





