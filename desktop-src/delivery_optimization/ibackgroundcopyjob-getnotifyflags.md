---
title: Méthode méthode ibackgroundcopyjob GetNotifyFlags (Deliveryoptimization. h)
description: Récupère les indicateurs de notification d’événement pour le travail.
ms.assetid: 95ADC97F-63DC-4EB6-B85C-7BCC79238C12
keywords:
- Méthode GetNotifyFlags
- Méthode GetNotifyFlags, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0f25a79fbf3ec508526f8107b55ad70c37b860ca99115945f9ee9f77b84ab138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755389"
---
# <a name="ibackgroundcopyjobgetnotifyflags-method"></a>Méthode ibackgroundcopyjob :: GetNotifyFlags, méthode

Récupère les indicateurs de notification d’événement pour le travail.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNotifyFlags(
  [out] ULONG *pNotifyFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNotifyFlags* \[ à\]
</dt> <dd>

Identifie les événements que votre application reçoit. Le tableau suivant répertorie les valeurs de l’indicateur de notification d’événement.



| Valeur                                                                                                                                                                                                  | Signification                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> </dl>    | Tous les fichiers du travail ont été transférés.<br/>                  |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <dt>**BG_NOTIFY_JOB_ERROR**</dt> </dl>                      | Une erreur s’est produite.<br/>                                              |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <dt>**BG_NOTIFY_DISABLE**</dt> </dl>                             | La notification d’événements est désactivée. Si cette option est définie, ignore les autres indicateurs.<br/> |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> </dl> | La tâche a été modifiée.<br/>                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                                |
|------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | Les indicateurs de notification d’événement ont été correctement récupérés.<br/> |



 

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





