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
ms.openlocfilehash: fdd39309774a61c4fd115ff09e16428101439a0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211548"
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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

