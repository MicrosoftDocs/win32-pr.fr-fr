---
title: Méthode IBackgroundCopyManager CreateJob (Deliveryoptimization.h)
description: Crée un travail.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- Méthode CreateJob
- Méthode CreateJob, interface IBackgroundCopyManager
- Interface IBackgroundCopyManager, méthode CreateJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 165b0a74f71ee5267fb3bd300baec4e48c51662b33c83203ebae1ba462f10a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953559"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a>IBackgroundCopyManager :: CreateJob, méthode

Crée un travail.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDisplayName* \[ dans\]
</dt> <dd>

Chaîne terminée par le caractère null qui contient un nom complet pour le travail. En règle générale, le nom complet est utilisé pour identifier la tâche dans une interface utilisateur. Notez que plusieurs travaux peuvent avoir le même nom complet. Ne doit pas avoir la **valeur null**. Le nom est limité à 256 caractères, à l’exclusion de la marque de fin null.

</dd> <dt>

*Type* \[ dans\]
</dt> <dd>

Type de tâche de transfert, par exemple BG_JOB_TYPE_DOWNLOAD. Pour obtenir la liste des types de transfert, consultez l’énumération [**BG_JOB_TYPE**](bg-job-type.md) .

</dd> <dt>

*pJobID* \[ à\]
</dt> <dd>

Identifie de façon unique votre travail dans la file d’attente. Utilisez cet identificateur lorsque vous appelez la méthode [**IBackgroundCopyManager :: GetJob**](ibackgroundcopymanager-getjob.md) pour obtenir un travail à partir de la file d’attente.

</dd> <dt>

*ppJob* \[ à\]
</dt> <dd>

Pointeur d’interface [**méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md) que vous utilisez pour modifier les propriétés du travail et spécifier les fichiers à transférer. Pour activer le travail dans la file d’attente, appelez la méthode [**méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md) . Libérez *ppJob* quand vous avez terminé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | La nouvelle tâche a été générée.<br/> |



 

## <a name="remarks"></a>Remarques

Seul l’utilisateur qui crée le travail ou un utilisateur disposant de privilèges d’administrateur peut [Ajouter des fichiers au travail](https://www.bing.com/search?q=add+files+to+the+job) et [modifier les propriétés du travail](https://www.bing.com/search?q=change+the+job's+properties).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager est défini en tant que 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>
