---
title: Méthode ibackgroundcopyjob SetPriority, méthode (Deliveryoptimization. h)
description: Spécifie le niveau de priorité de votre travail. Le niveau de priorité détermine le moment où votre travail est traité par rapport à d’autres travaux dans la file d’attente de transfert.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- SetPriority, méthode
- SetPriority, méthode, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode SetPriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ed1852d6990b94a000ac6affcec6020d266aaac5fae4611c3985a6f5c203aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542870"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a>Méthode ibackgroundcopyjob :: SetPriority, méthode

Spécifie le niveau de priorité de votre travail. Le niveau de priorité détermine le moment où votre travail est traité par rapport à d’autres travaux dans la file d’attente de transfert.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Priorité* \[ dans\]
</dt> <dd>

Spécifie le niveau de priorité de votre travail par rapport à d’autres travaux dans la file d’attente de transfert. La valeur par défaut est BG_JOB_PRIORITY_NORMAL. Pour obtenir la liste des niveaux de priorité, consultez l’énumération [**BG_JOB_PRIORITY**](bg-job-priority-.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | La priorité du travail a été correctement définie.<br/> |



 

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

[**BG_JOB_PRIORITY**](bg-job-priority-.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: getPriority,**](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





