---
title: Méthode méthode ibackgroundcopyjob GetNoProgressTimeout (Deliveryoptimization. h)
description: Récupère la durée pendant laquelle le service tente de transférer le fichier après qu’une condition d’erreur temporaire se produit. En cas de progression, la minuterie est réinitialisée.
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- Méthode GetNoProgressTimeout
- Méthode GetNoProgressTimeout, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ccd236c17612aa03a28e07a08d087454f8db6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465519"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a>Méthode ibackgroundcopyjob :: GetNoProgressTimeout, méthode

Récupère la durée pendant laquelle le service tente de transférer le fichier après qu’une condition d’erreur temporaire se produit. En cas de progression, la minuterie est réinitialisée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pRetryPeriod* \[ dans\]
</dt> <dd>

Durée, en secondes, pendant laquelle le service tente de transférer le fichier après qu’une erreur temporaire se produit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | Le délai d’attente a été correctement récupéré.<br/> |



 

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

[**Méthode ibackgroundcopyjob :: SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





