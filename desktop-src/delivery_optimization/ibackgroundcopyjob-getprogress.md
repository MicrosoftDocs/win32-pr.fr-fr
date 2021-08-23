---
title: Méthode méthode ibackgroundcopyjob GetProgress (Deliveryoptimization. h)
description: Récupère des informations de progression relatives au travail, telles que le nombre d’octets et de fichiers transférés.
ms.assetid: E23C82E1-3805-4C5D-9F18-0DA17F7C473E
keywords:
- Méthode GetProgress
- Méthode GetProgress, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07a498aef2a9dcfd108733b45526bd876817d8d5075323d0edd95c7cbf3de8df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755319"
---
# <a name="ibackgroundcopyjobgetprogress-method"></a>Méthode ibackgroundcopyjob :: GetProgress, méthode

Récupère des informations de progression relatives au travail, telles que le nombre d’octets et de fichiers transférés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetProgress(
  [out] BG_JOB_PROGRESS *pProgress
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pProgress* \[ à\]
</dt> <dd>

Contient des données que vous pouvez utiliser pour calculer le pourcentage d’achèvement de la tâche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | Les informations de progression ont été récupérées avec succès.<br/> |



 

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
</dt> </dl>

 

 





