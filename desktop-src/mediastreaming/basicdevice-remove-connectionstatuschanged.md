---
title: Méthode BasicDevice.remove_ConnectionStatusChanged
description: Annule l’inscription d’un gestionnaire d’événements pour l’événement ConnectionStatusChanged. | Méthode BasicDevice.remove_ConnectionStatusChanged
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- API de diffusion multimédia en continu de méthode remove_ConnectionStatusChanged
- API de diffusion multimédia en continu de méthode remove_ConnectionStatusChanged, interface BasicDevice
- API de diffusion multimédia en continu de l’interface BasicDevice, méthode remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89057195c23aa917c7338a8abb740817bb6af7896261cf1d31bcb37d5d5d5ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972498"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a>Méthode BasicDevice. Remove \_ ConnectionStatusChanged

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

Référence à un jeton obtenu à partir de la méthode [**Add \_ ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) lors de l’inscription du gestionnaire d’événements.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

