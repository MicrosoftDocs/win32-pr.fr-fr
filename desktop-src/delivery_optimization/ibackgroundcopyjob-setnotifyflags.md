---
title: Méthode méthode ibackgroundcopyjob SetNotifyFlags (Deliveryoptimization. h)
description: Spécifie le type de notification d’événement que vous souhaitez recevoir, par exemple les événements de transfert de travaux.
ms.assetid: 19E626A5-6B6E-44E0-BD6F-43F132F32890
keywords:
- Méthode SetNotifyFlags
- Méthode SetNotifyFlags, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode SetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cdb1750391027163a7ac8fb9ba8cc20085a06d187de0d7f05850641a5a774b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542916"
---
# <a name="ibackgroundcopyjobsetnotifyflags-method"></a>Méthode ibackgroundcopyjob :: SetNotifyFlags, méthode

Spécifie le type de notification d’événement que vous souhaitez recevoir, par exemple les événements de transfert de travaux.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetNotifyFlags(
  [in] ULONG NotifyFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NotifyFlags* \[ dans\]
</dt> <dd>

Définissez un ou plusieurs des indicateurs suivants pour identifier les événements que vous souhaitez recevoir.



| Valeur                                                                                                                                                                                                                                                                                    | Signification                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt> </dl>                          | Tous les fichiers du travail ont été transférés.<br/>                                                                                                                                                          |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt> </dl>                                            | Une erreur s’est produite.<br/>                                                                                                                                                                                      |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt> </dl>                                                   | Non pris en charge.<br/>                                                                                                                                                                                              |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt> </dl>                       | La tâche a été modifiée. Par exemple, une valeur de propriété a été modifiée, l’état de la tâche a changé ou la progression est effectuée en transférant les fichiers. Cet indicateur est ignoré si la notification de ligne de commande est spécifiée.<br/> |
| <span id="BG_NOTIFY_FILE_TRANSFERRED"></span><span id="bg_notify_file_transferred"></span><dl> <dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt> </dl>                       | Un fichier du travail a été transféré. Cet indicateur est ignoré si la notification de ligne de commande est spécifiée.<br/>                                                                                                     |
| <span id="BG_NOTIFY_FILE_RANGES_TRANSFERRED"></span><span id="bg_notify_file_ranges_transferred"></span><dl> <dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt> </dl> | Non pris en charge.<br/>                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                                          | Description                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl>             | Le type de notification d’événement a été correctement défini.<br/>                                          |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | L’état du travail ne peut pas être BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Remarques

Utilisez la méthode **SetNotifyFlags** conjointement avec [**méthode ibackgroundcopyjob :: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).

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

[**Méthode ibackgroundcopyjob :: GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





