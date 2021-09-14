---
title: Méthode ibackgroundcopyjob GetId, méthode (Deliveryoptimization. h)
description: Récupère l’identificateur utilisé pour identifier le travail dans la file d’attente.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId (méthode)
- GetId, méthode, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetId
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade12d72d68b43df7d9ae3d1f33010bb95b7052a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921755"
---
# <a name="ibackgroundcopyjobgetid-method"></a>Méthode ibackgroundcopyjob :: GetId, méthode

Récupère l’identificateur utilisé pour identifier le travail dans la file d’attente.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pJobID* \[ à\]
</dt> <dd>

GUID qui identifie le travail dans la file d’attente DO.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com **HRESULT** standard en cas d’erreur.

## <a name="remarks"></a>Notes

Le service génère l’identificateur lorsque vous [créez](ibackgroundcopymanager-createjob.md) le travail. Pour utiliser l’identificateur pour récupérer un pointeur d’interface [**méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md) pour le travail, appelez la méthode [**IBackgroundCopyManager :: GetJob**](ibackgroundcopymanager-getjob.md) .

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

[**IBackgroundCopyManager :: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





