---
title: Méthode méthode ibackgroundcopyjob GetState (Deliveryoptimization. h)
description: Récupère l’état du travail.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- Méthode GetState
- Méthode GetState, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetState
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64a26d1cc301230a9bb8330b9a2b2daf3178b1538ec95f593cd5e3f4d3099d7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755299"
---
# <a name="ibackgroundcopyjobgetstate-method"></a>Méthode ibackgroundcopyjob :: GetState, méthode

Récupère l’état du travail.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pJobState* \[ à\]
</dt> <dd>

État du travail. Par exemple, l’état indique si le travail est erroné, s’il est en cours de transfert de données ou s’il est suspendu. Pour obtenir la liste des États de travail, consultez l’énumération [**BG_JOB_STATE**](bg-job-state-.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | L’état de la tâche a été récupéré avec succès.<br/> |



 

## <a name="remarks"></a>Remarques

Si vous souhaitez savoir quand un travail est en erreur ou si a transféré tous les fichiers du travail, vous pouvez utiliser cette méthode pour interroger l’état du travail ou vous pouvez vous inscrire pour recevoir une notification lorsque des événements se produisent. Pour plus d’informations sur l’inscription à la réception d’une notification d’événement, consultez l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .

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

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> </dl>

 

 





