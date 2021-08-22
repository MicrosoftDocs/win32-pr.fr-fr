---
title: Interface IBackgroundCopyManager (Deliveryoptimization. h)
description: Crée des tâches de transfert, extrait un objet énumérateur qui contient les travaux dans la file d’attente et extrait des tâches individuelles de la file d’attente.
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- Interface IBackgroundCopyManager
- Interface IBackgroundCopyManager, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cf1ca14443823a5448a63c04d19d00957d4064353183d79aa7762f729115301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542151"
---
# <a name="ibackgroundcopymanager-interface"></a>Interface IBackgroundCopyManager

Crée des tâches de transfert, extrait un objet énumérateur qui contient les travaux dans la file d’attente et extrait des tâches individuelles de la file d’attente.

## <a name="members"></a>Membres

L’interface **IBackgroundCopyManager** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyManager** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IBackgroundCopyManager** possède ces méthodes.



| Méthode                                                | Description                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [**CreateJob**](ibackgroundcopymanager-createjob.md) | Crée une tâche de transfert.<br/>                   |
| [**GetJob**](ibackgroundcopymanager-getjob.md)       | Récupère un travail spécifié de la file d’attente.<br/> |



 

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

[**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

