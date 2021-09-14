---
title: Méthode méthode ibackgroundcopyjob getPriority, (Deliveryoptimization. h)
description: Récupère le niveau de priorité du travail. Le niveau de priorité détermine le moment où le travail est traité par rapport à d’autres travaux dans la file d’attente de transfert.
ms.assetid: 2F778B35-8DBB-4540-88C2-A2E18EBB0D89
keywords:
- Méthode getPriority,
- Méthode getPriority,, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode getPriority,
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae9a865045ee1264a0598a3d3c1db8cc3c3b8bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008142"
---
# <a name="ibackgroundcopyjobgetpriority-method"></a>Méthode ibackgroundcopyjob :: getPriority,, méthode

Récupère le niveau de priorité du travail. Le niveau de priorité détermine le moment où le travail est traité par rapport à d’autres travaux dans la file d’attente de transfert.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPriority(
  [out] BG_JOB_PRIORITY *pPriority
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPriority* \[ à\]
</dt> <dd>

Priorité du travail par rapport aux autres travaux dans la file d’attente de transfert.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | Le niveau de priorité a été récupéré avec succès.<br/> |



 

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

[**Méthode ibackgroundcopyjob :: SetPriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





