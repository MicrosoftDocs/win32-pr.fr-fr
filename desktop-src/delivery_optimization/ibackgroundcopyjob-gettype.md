---
title: Méthode ibackgroundcopyjob GetType, méthode (Deliveryoptimization. h)
description: Récupère le type de transfert effectué, tel qu’un téléchargement de fichier ou un chargement.
ms.assetid: F543A601-9385-4A73-A4E2-DE61433E84D3
keywords:
- GetType (méthode)
- GetType, méthode, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetType
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetType
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b0a09a3c7387b5b911bf6731921e7ed4e9b9163
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012979"
---
# <a name="ibackgroundcopyjobgettype-method"></a>Méthode ibackgroundcopyjob :: GetType, méthode

Récupère le type de transfert effectué, tel qu’un téléchargement de fichier ou un chargement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetType(
  [out] BG_JOB_TYPE *pJobType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pJobType* \[ à\]
</dt> <dd>

Type de transfert effectué. Pour obtenir la liste des types de transfert, consultez l’énumération [**BG_JOB_TYPE**](bg-job-type.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                          |
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | Le type de transfert a été correctement récupéré.<br/> |



 

## <a name="remarks"></a>Notes

Spécifiez le type de transfert lors de la création du travail.

## <a name="requirements"></a>Spécifications



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

[**BG_JOB_TYPE**](bg-job-type.md)
</dt> <dt>

[**IBackgroundCopyManager :: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





