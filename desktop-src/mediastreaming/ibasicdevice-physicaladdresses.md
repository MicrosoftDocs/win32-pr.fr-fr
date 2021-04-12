---
title: Méthode IBasicDevice PhysicalAddresses
description: Retourne un vecteur d’adresses physiques.
ms.assetid: 85F48EE3-14A1-46DA-A3C3-F94A8A43CF92
keywords:
- API de diffusion multimédia en continu de méthode PhysicalAddresses
- API de diffusion multimédia en continu de méthode PhysicalAddresses, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode PhysicalAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.PhysicalAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f1cd87435c78e1f6877d1bb6afd1b38981b05dc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312448"
---
# <a name="ibasicdevicephysicaladdresses-method"></a>IBasicDevice ::P méthode hysicalAddresses

Retourne un vecteur d’adresses physiques.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PhysicalAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit une collection énumérable de pointeurs vers des adresses physiques.

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

 

 





