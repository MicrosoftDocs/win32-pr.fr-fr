---
title: IBasicDevice add_ConnectionStatusChanged méthode)
description: Inscrit un gestionnaire d’événements pour l’événement ConnectionStatusChanged. | IBasicDevice add_ConnectionStatusChanged méthode)
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- API de diffusion multimédia en continu de méthode add_ConnectionStatusChanged
- API de diffusion multimédia en continu de méthode add_ConnectionStatusChanged, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e90ea1f90ccd5b1e141b0e4071213abfe6f4a05a85d3c0d4ced505e1b0f164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952659"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a>IBasicDevice :: Add \_ ConnectionStatusChanged, méthode

Inscrit un gestionnaire d’événements pour l’événement [**ConnectionStatusChanged**](connectionstatuschanged.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gestionnaire* \[ dans\]
</dt> <dd>

Fonction de gestionnaire d’événements [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .

</dd> <dt>

*jeton* \[ out, retval\]
</dt> <dd>

Référence à un jeton qui peut être utilisé pour annuler l’inscription du gestionnaire d’événements.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

Pour annuler l’inscription du gestionnaire d’événements qui a été enregistré par cette méthode, transmettez la valeur de *jeton* à la méthode [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

