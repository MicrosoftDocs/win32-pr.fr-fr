---
title: Méthode ibackgroundcopyjob méthode Cancel (Deliveryoptimization. h)
description: Supprime le travail de la file d’attente de transfert et supprime les fichiers temporaires associés du client (Téléchargements) et le serveur (chargements).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Cancel, méthode
- Cancel, méthode, méthode ibackgroundcopyjob, interface
- Interface méthode ibackgroundcopyjob, méthode Cancel
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843457"
---
# <a name="ibackgroundcopyjobcancel-method"></a>Méthode ibackgroundcopyjob :: Cancel, méthode

Supprime le travail de la file d’attente de transfert et supprime les fichiers temporaires associés du client (Téléchargements) et le serveur (chargements).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                                          | Description                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl>             | La tâche a été annulée avec succès.<br/>                                                                |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Impossible d’annuler un travail dont l’État est BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Notes

Vous pouvez annuler un travail à tout moment ; Toutefois, le travail ne peut pas être récupéré une fois qu’il a été annulé.

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

[**Méthode ibackgroundcopyjob :: complet**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





