---
title: Méthode BasicDevice.add_ConnectionStatusChanged
description: Inscrit un gestionnaire d’événements pour l’événement ConnectionStatusChanged. | Méthode BasicDevice.add_ConnectionStatusChanged
ms.assetid: FFAA0981-508C-4300-9CA9-24C6AFC1183D
keywords:
- API de diffusion multimédia en continu de méthode add_ConnectionStatusChanged
- API de diffusion multimédia en continu de méthode add_ConnectionStatusChanged, interface BasicDevice
- API de diffusion multimédia en continu de l’interface BasicDevice, méthode add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a416770a0ea3a4d317a2308fc9f5c9d940e89900aabbc7651ceb93b789454338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462259"
---
# <a name="basicdeviceadd_connectionstatuschanged-method"></a>BasicDevice. Add \_ ConnectionStatusChanged, méthode

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

Pour annuler l’inscription du gestionnaire d’événements qui a été enregistré par cette méthode, transmettez la valeur de *jeton* à la méthode [**Remove \_ ConnectionStatusChanged**](basicdevice-remove-connectionstatuschanged.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

