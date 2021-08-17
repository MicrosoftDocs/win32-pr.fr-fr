---
title: Méthode IBasicDevice DiscoveredOnCurrentNetwork
description: Récupère une valeur qui indique si l’appareil se trouve sur le réseau actuel.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- API de diffusion multimédia en continu de méthode DiscoveredOnCurrentNetwork
- API de diffusion multimédia en continu de méthode DiscoveredOnCurrentNetwork, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode DiscoveredOnCurrentNetwork
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 605962315e4eab2cdbd5beab264747d282d78ef7c6f44b3bbcbf2f249bac7548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473488"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a>IBasicDevice ::D méthode iscoveredOnCurrentNetwork

Récupère une valeur qui indique si l’appareil se trouve sur le réseau actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un pointeur vers une valeur booléenne qui est **true** si l’appareil se trouve sur le réseau actuel.

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

 

 





