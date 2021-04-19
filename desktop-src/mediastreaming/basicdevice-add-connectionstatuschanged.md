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
ms.openlocfilehash: 61a36e46d554a953ecd061ccf2396d33b0578d8f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538282"
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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Pour annuler l’inscription du gestionnaire d’événements qui a été enregistré par cette méthode, transmettez la valeur de *jeton* à la méthode [**Remove \_ ConnectionStatusChanged**](basicdevice-remove-connectionstatuschanged.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

