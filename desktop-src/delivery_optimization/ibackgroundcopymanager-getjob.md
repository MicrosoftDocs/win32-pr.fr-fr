---
title: Méthode IBackgroundCopyManager GetJob (Deliveryoptimization. h)
description: Récupère un travail spécifié à partir de la file d’attente de transfert. En règle générale, votre application conserve l’identificateur de tâche, ce qui vous permet de récupérer ultérieurement la tâche à partir de la file d’attente.
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- Méthode GetJob
- Méthode GetJob, interface IBackgroundCopyManager
- Interface IBackgroundCopyManager, méthode GetJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d8d05b496eaa0d6f1520f22efeed8a39af5eb8e4c338457e18c65a7913489472
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542287"
---
# <a name="ibackgroundcopymanagergetjob-method"></a>IBackgroundCopyManager :: GetJob, méthode

Récupère un travail spécifié à partir de la file d’attente de transfert. En règle générale, votre application conserve l’identificateur de tâche, ce qui vous permet de récupérer ultérieurement la tâche à partir de la file d’attente.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*JobID* \[ dans\]
</dt> <dd>

Identifie le travail à récupérer à partir de la file d’attente de transfert. La méthode [**createJob**](ibackgroundcopymanager-createjob.md) retourne l’identificateur de la tâche.

</dd> <dt>

*ppJob* \[ à\]
</dt> <dd>

Pointeur d’interface [**méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md) vers le travail spécifié par *JobID*. Lorsque vous avez terminé, libérez *ppJob*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                                      | Description                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl>         | La tâche a été récupérée à partir de la file d’attente de transfert.<br/> |
| <dl> <dt>**DO_E_NOT_FOUND**</dt> </dl> | La tâche est introuvable dans la file d’attente.<br/>                     |
| <dl> <dt>**E_ACCESSDENIED**</dt> </dl>   | L’utilisateur n’a pas l’autorisation de récupérer le travail.<br/>      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager est défini en tant que 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: GetId**](ibackgroundcopyjob-getid.md)
</dt> <dt>

[**IBackgroundCopyManager :: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





