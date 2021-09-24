---
title: Méthode ibackgroundcopyjob méthode Complete (Deliveryoptimization. h)
description: Met fin au travail et enregistre les fichiers transférés sur le client.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Méthode complète
- Méthode complète, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode complète
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f55afa5a95659df922d80a6894ed1586ceab0cbc
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520489"
---
# <a name="ibackgroundcopyjobcomplete-method"></a>Méthode ibackgroundcopyjob :: Complete, méthode

Met fin au travail et enregistre les fichiers transférés sur le client.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Complete();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne les valeurs **HRESULT** suivantes. La méthode peut également retourner des erreurs liées au changement du nom des copies temporaires des fichiers transférés en leurs noms donnés.



| Code de retour                                                                                          | Description                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl>             | Tous les fichiers ont été transférés avec succès.<br/>                                                                                                                                                         |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Pour les téléchargements, l’état du travail ne peut pas être BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED. <br/> Pour les téléchargements, l’état du travail doit être BG_JOB_STATE_TRANSFERRED.<br/> |



 

## <a name="remarks"></a>Remarques

Tous les fichiers ont été transférés avec succès si l’état du travail est **BG_JOB_STATE_TRANSFERRED**. Pour vérifier l’état de la tâche, appelez la méthode [**méthode ibackgroundcopyjob :: GetState**](ibackgroundcopyjob-getstate.md) . Vous pouvez également implémenter l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) pour recevoir une notification lorsque tous les fichiers ont été transférés au client.

L’optimisation de la distribution conserve uniquement les tâches qui sont inférieures à 30 jours. Tous les travaux plus anciens seront supprimés. L’optimisation de la distribution ne prend pas en charge le stratégie de groupe [paramètre jobinactivitytimeout](https://www.bing.com/search?q=JobInactivityTimeout) .

Pour les travaux de téléchargement, vous pouvez appeler la méthode **complète** à tout moment pendant le processus de transfert. Toutefois, seuls les fichiers qui ont été transférés vers le client avant l’appel de cette méthode sont enregistrés. Par exemple, si vous appelez la méthode **Complete** alors que l’optimisation de la distribution traite le troisième des cinq fichiers, seuls les deux premiers fichiers sont enregistrés. Pour déterminer les fichiers qui ont été transférés, appelez la méthode [**IBackgroundCopyFile :: GetProgress**](ibackgroundcopyfile-getprogress-method.md) et comparez le membre **bytesTransferred** au membre **bytesTotal** de la structure [**BG_FILE_PROGRESS**](bg-file-progress.md) .

Pour les travaux de chargement, vous pouvez appeler la méthode **Complete** uniquement lorsque l’état du travail est **BG_JOB_STATE_TRANSFERRED**.

Le propriétaire du fichier est l’utilisateur qui a effectué l’appel. Par exemple, si un administrateur termine la tâche de quelqu’un d’autre, l’administrateur n’est pas propriétaire du travail.

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

[**Méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





