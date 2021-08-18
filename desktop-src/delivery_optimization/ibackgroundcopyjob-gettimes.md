---
title: Méthode méthode ibackgroundcopyjob GetTimes (Deliveryoptimization. h)
description: Récupère les horodatages liés aux travaux, tels que l’heure à laquelle le travail a été créé ou modifié pour la dernière fois.
ms.assetid: 9002FB8D-08CB-4878-980F-15FE0DC952A6
keywords:
- Méthode GetTimes
- Méthode GetTimes, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetTimes
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetTimes
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3179342630fe932dd55efc4e75e15cd06a879d6cdc93005981cc7e0ebca7e05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755209"
---
# <a name="ibackgroundcopyjobgettimes-method"></a>Méthode ibackgroundcopyjob :: GetTimes, méthode

Récupère les horodatages liés aux travaux, tels que l’heure à laquelle le travail a été créé ou modifié pour la dernière fois.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTimes(
  [out] BG_JOB_TIMES *pTimes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTimes* \[ à\]
</dt> <dd>

Contient des horodatages liés aux travaux. Pour connaître les horodatages disponibles, consultez la structure [**BG_JOB_TIMES**](bg-job-times.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | Les horodatages ont été correctement récupérés.<br/> |



 

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

[**BG_JOB_TIMES**](bg-job-times.md)
</dt> </dl>

 

 





