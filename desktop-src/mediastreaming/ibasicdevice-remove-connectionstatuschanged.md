---
title: IBasicDevice remove_ConnectionStatusChanged méthode)
description: Annule l’inscription d’un gestionnaire d’événements pour l’événement ConnectionStatusChanged. | IBasicDevice remove_ConnectionStatusChanged méthode)
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- API de diffusion multimédia en continu de méthode remove_ConnectionStatusChanged
- API de diffusion multimédia en continu de méthode remove_ConnectionStatusChanged, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35b2f08b6df25f57d77f5c3677a4c6499370d9472202b6808073c5a75d1e2c34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599799"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a>IBasicDevice :: Remove \_ ConnectionStatusChanged, méthode

Annule l’inscription d’un gestionnaire d’événements pour l’événement [**ConnectionStatusChanged**](connectionstatuschanged.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*jeton* \[ dans\]
</dt> <dd>

Référence à un jeton obtenu à partir de la méthode [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) lors de l’inscription du gestionnaire d’événements.

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

 

 





