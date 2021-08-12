---
title: Méthode ibackgroundcopyjob suspend, méthode (Deliveryoptimization. h)
description: Interrompt un travail. Les nouveaux travaux, les travaux en erreur et les travaux qui ont terminé le transfert des fichiers sont automatiquement suspendus.
ms.assetid: 23EED354-A3AC-4865-8C06-ADA097851F96
keywords:
- Suspend, méthode
- Suspend, méthode, méthode ibackgroundcopyjob, interface
- Interface méthode ibackgroundcopyjob, méthode suspend
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Suspend
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9458347c8f09a2f04c4e2800a0f2f747571f5519b322133ef4b874b15cf77a7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542808"
---
# <a name="ibackgroundcopyjobsuspend-method"></a>Méthode ibackgroundcopyjob :: suspend, méthode

Interrompt un travail. Les nouveaux travaux, les travaux en erreur et les travaux qui ont terminé le transfert des fichiers sont automatiquement suspendus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Suspend();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                                          | Description                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl>             | La tâche a été suspendue.<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | L’état du travail ne peut pas être BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





