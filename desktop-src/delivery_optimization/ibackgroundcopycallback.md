---
title: Interface IBackgroundCopyCallback (Deliveryoptimization. h)
description: Implémentez l’interface IBackgroundCopyCallback pour recevoir une notification indiquant qu’un travail est terminé, a été modifié ou est erroné. Les clients utilisent cette interface au lieu d’interroger l’état du travail.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- Interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4169acec87e4d1e8a31eecaa4f93b9404aafb714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106540774"
---
# <a name="ibackgroundcopycallback-interface"></a>Interface IBackgroundCopyCallback

Implémentez l’interface **IBackgroundCopyCallback** pour recevoir une notification indiquant qu’un travail est terminé, a été modifié ou est erroné. Les clients utilisent cette interface au lieu d’interroger l’état du travail.

## <a name="members"></a>Membres

L’interface **IBackgroundCopyCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyCallback** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IBackgroundCopyCallback** possède ces méthodes.



| Méthode                                                                    | Description                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**JobError**](ibackgroundcopycallback-joberror-method.md)               | Appelée lorsqu’une erreur se produit.<br/>                                           |
| [**JobModification**](ibackgroundcopycallback-jobmodification-method.md) | Appelé lorsqu’un travail est modifié.<br/>                                         |
| [**JobTransferred**](ibackgroundcopycallback-jobtransferred.md)          | Appelé lorsque tous les fichiers du travail ont été transférés avec succès.<br/> |



 

## <a name="remarks"></a>Notes

Pour recevoir des notifications, appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) pour spécifier le pointeur d’interface vers votre implémentation **IBackgroundCopyCallback** . Pour spécifier les notifications que vous souhaitez recevoir, appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) .

Appelez vos rappels tant que le pointeur d’interface est valide. L’interface de notification n’est plus valide lorsque votre application se termine ; Ne conserve pas l’interface Notify. Par conséquent, le processus d’initialisation de votre application doit appeler la méthode [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) sur les tâches existantes pour lesquelles vous souhaitez recevoir des notifications.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback est défini en tant que 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

