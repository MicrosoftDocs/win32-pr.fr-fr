---
title: Interface méthode ibackgroundcopyjob (Deliveryoptimization. h)
description: Utilisez l’interface méthode ibackgroundcopyjob pour ajouter des fichiers au travail, définir le niveau de priorité du travail, déterminer l’état du travail et pour démarrer et arrêter le travail.
ms.assetid: 0D1EAC8D-0013-4FBC-A07F-14CD5D709549
keywords:
- Interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27febd08519a06f7ad452882cf0725fed209e0306182ba336343049936795acf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543025"
---
# <a name="ibackgroundcopyjob-interface"></a>Interface méthode ibackgroundcopyjob

Utilisez l’interface [**méthode ibackgroundcopyjob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) pour ajouter des fichiers au travail, définir le niveau de priorité du travail, déterminer l’état du travail et pour démarrer et arrêter le travail.

Pour créer un travail, appelez la méthode [**IBackgroundCopyManager :: createJob**](ibackgroundcopymanager-createjob.md) . Pour récupérer un pointeur d’interface [**méthode ibackgroundcopyjob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) sur un travail existant, appelez la méthode [**IBackgroundCopyManager :: GetJob**](ibackgroundcopymanager-getjob.md) .

## <a name="members"></a>Membres

L’interface **méthode ibackgroundcopyjob** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Méthode ibackgroundcopyjob** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **méthode ibackgroundcopyjob** possède ces méthodes.



| Méthode                                                                  | Description                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Annuler**](ibackgroundcopyjob-cancel.md)                             | Annule le travail et supprime les fichiers temporaires du client.<br/>                                                                                                                                                           |
| [**Terminé**](ibackgroundcopyjob-complete.md)                         | Met fin au travail et enregistre les fichiers transférés sur le client.<br/>                                                                                                                                                            |
| [**EnumFiles**](ibackgroundcopyjob-enumfiles.md)                       | Retourne un pointeur d’interface vers un objet énumérateur que vous utilisez pour énumérer les fichiers du travail.<br/>                                                                                                                   |
| [**GetDisplayName,**](ibackgroundcopyjob-getdisplayname.md)             | Récupère le nom complet qui identifie le travail.<br/>                                                                                                                                                                    |
| [**GetError**](ibackgroundcopyjob-geterror.md)                         | Récupère un pointeur d’interface vers l’objet d’erreur après qu’une erreur s’est produite.<br/>                                                                                                                                              |
| [**GetId**](ibackgroundcopyjob-getid.md)                               | Récupère l’identificateur du travail dans la file d’attente.<br/>                                                                                                                                                                      |
| [**GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md) | Récupère la durée pendant laquelle continue d’essayer de transférer le fichier après avoir rencontré une condition d’erreur temporaire.<br/>                                                                                             |
| [**GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)             | Récupère les indicateurs de notification d’événements (rappel) que vous avez définis pour votre application.<br/>                                                                                                                                   |
| [**GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)     | Récupère un pointeur vers votre implémentation de l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (rappels).<br/>                                                                                    |
| [**GetPriority,**](ibackgroundcopyjob-getpriority.md)                   | Récupère le niveau de priorité que vous avez défini pour le travail.<br/>                                                                                                                                                                 |
| [**GetProgress**](ibackgroundcopyjob-getprogress.md)                   | Récupère des informations de progression relatives au travail, telles que le nombre d’octets et de fichiers transférés au client.<br/>                                                                                                           |
| [**GetState**](ibackgroundcopyjob-getstate.md)                         | Récupère l’état du travail.<br/>                                                                                                                                                                                        |
| [**GetTimes**](ibackgroundcopyjob-gettimes.md)                         | Récupère les horodatages pour les activités liées au travail, telles que l’heure de création du travail.<br/>                                                                                                                         |
| [**GetType**](ibackgroundcopyjob-gettype.md)                           | Récupère le type de transfert effectué, tel qu’un téléchargement de fichier.<br/>                                                                                                                                               |
| [**Reprendre**](ibackgroundcopyjob-resume.md)                             | Démarre un nouveau travail ou redémarre un travail suspendu.<br/>                                                                                                                                                                          |
| [**SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md) | Spécifie la durée pendant laquelle continue à essayer de transférer le fichier après avoir rencontré une condition d’erreur temporaire.<br/>                                                                                             |
| [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)             | Spécifie le type de notification d’événement à recevoir.<br/>                                                                                                                                                                   |
| [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)     | Spécifie un pointeur vers votre implémentation de l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (rappels). L’interface reçoit une notification basée sur les indicateurs de notification d’événement que vous définissez.<br/> |
| [**SetPriority**](ibackgroundcopyjob-setpriority.md)                   | Spécifie la priorité du travail par rapport aux autres travaux de la file d’attente de transfert.<br/>                                                                                                                                        |
| [**Momentané**](ibackgroundcopyjob-suspend.md)                           | Suspend la tâche.<br/>                                                                                                                                                                                                        |



 

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

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> </dl>

 

