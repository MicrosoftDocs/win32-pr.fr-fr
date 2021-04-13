---
title: IBasicDevice (méthode)
description: Retourne un vecteur d’adresses IP.
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- Méthode adressesIP diffusion multimédia en continu API
- AdressesIP méthode diffusion multimédia en continu API, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode adressesIP
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0623b6e2e5d96cb0a400ab1e820424b7eecf46c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380764"
---
# <a name="ibasicdeviceipaddresses-method"></a>IBasicDevice :: adressesIP, méthode

Retourne un vecteur d’adresses IP.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit une collection énumérable de pointeurs vers des adresses IP.

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

 

 





