---
title: Méthode méthode ibackgroundcopyjob SetNoProgressTimeout (Deliveryoptimization. h)
description: Définit la durée pendant laquelle l’optimisation de la remise (DO) tente de transférer le fichier après qu’une condition d’erreur temporaire se produit. En cas de progression, la minuterie est réinitialisée.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Méthode SetNoProgressTimeout
- Méthode SetNoProgressTimeout, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode SetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dcf6905388d54103aaac34ae934c89e2fd8ccc16ce32a384eb730376606351b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542926"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a>Méthode ibackgroundcopyjob :: SetNoProgressTimeout, méthode

Définit la durée pendant laquelle l’optimisation de la remise (DO) tente de transférer le fichier après qu’une condition d’erreur temporaire se produit. En cas de progression, la minuterie est réinitialisée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RetryPeriod* \[ dans\]
</dt> <dd>

Durée, en secondes, pendant laquelle tente de transférer le fichier après qu’aucune progression n’a été effectuée. La période de nouvelle tentative par défaut pour un travail à priorité élevée est de 3600 secondes (1 heure) et, pour une tâche basse priorité, 86400 secondes (24 heures).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                                          | Description                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl>             | Période de nouvelle tentative définie avec succès.<br/>                                                            |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | L’état du travail ne peut pas être BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Remarques

Si ne progresse pas pendant la période de nouvelle tentative, il déplace l’état du travail de BG_JOB_STATE_TRANSIENT_ERROR à BG_JOB_STATE_ERROR. Si vous demandez une notification d’erreur, appelle votre rappel [**JobError**](https://www.bing.com/search?q=**JobError**) .

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

[**Méthode ibackgroundcopyjob :: GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





