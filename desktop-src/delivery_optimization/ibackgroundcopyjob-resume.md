---
title: Méthode ibackgroundcopyjob, méthode de reprise (Deliveryoptimization. h)
description: Active un nouveau travail ou redémarre un travail qui a été suspendu.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Resume, méthode
- Resume, méthode, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode Resume
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f87f5b5347785810d84331ce56f240cd1f016383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103241"
---
# <a name="ibackgroundcopyjobresume-method"></a>Méthode ibackgroundcopyjob :: Resume, méthode

Active un nouveau travail ou redémarre un travail qui a été suspendu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Resume();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                                          | Description                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl>             | Le travail a été redémarré avec succès.<br/>                                                           |
| <dl> <dt>**DO_E_EMPTY**</dt> </dl>          | Aucun fichier à transférer.<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | L’état du travail ne peut pas être BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Notes

Lorsque vous créez un travail, le travail est initialement suspendu. L’appel de la méthode **Resume** déplace le travail vers l’État Transfering. Notez que le travail doit contenir un ou plusieurs fichiers avant d’appeler cette méthode.

Si un travail qui se trouve dans l’État BG_JOB_STATE_TRANSIENT_ERROR ou BG_JOB_STATE_ERROR, appelez la méthode **Resume** pour redémarrer le travail après avoir corrigé l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                       |
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

[**Méthode ibackgroundcopyjob :: suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





