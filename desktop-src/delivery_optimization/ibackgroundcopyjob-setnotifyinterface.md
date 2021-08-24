---
title: Méthode méthode ibackgroundcopyjob SetNotifyInterface (Deliveryoptimization. h)
description: Identifie votre implémentation de l’interface IBackgroundCopyCallback. Utilisez l’interface IBackgroundCopyCallback pour recevoir la notification des événements liés aux travaux.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- Méthode SetNotifyInterface
- Méthode SetNotifyInterface, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode SetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd54255d87ee3f15f87d692e06b7a503e773634ab4ec30c3f388388233aab2b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793408"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a>Méthode ibackgroundcopyjob :: SetNotifyInterface, méthode

Identifie votre implémentation de l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) . Utilisez l’interface **IBackgroundCopyCallback** pour recevoir la notification des événements liés aux travaux.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNotifyInterface* 
</dt> <dd>

Pointeur d’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) . Pour supprimer le pointeur d’interface de rappel actuel, affectez la valeur **null** à ce paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | Le pointeur d’interface de notification a été correctement défini.<br/> |



 

## <a name="remarks"></a>Remarques

Appelez cette méthode uniquement si vous implémentez l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) . Utilisez la méthode **SetNotifyInterface** conjointement avec la méthode [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) pour spécifier le type de notification que vous souhaitez recevoir.

L’interface de notification n’est plus valide quand votre application se termine ; Ne conserve pas l’interface Notify. Par conséquent, le processus d’initialisation de votre application doit appeler la méthode **SetNotifyInterface** sur les tâches existantes pour lesquelles vous souhaitez recevoir des notifications. Si vous avez besoin de capturer l’État et les informations de progression qui se sont produites depuis la dernière exécution de votre application, interrogez les informations d’État et de progression pendant l’initialisation de l’application.

Seul le propriétaire/créateur du travail ou un administrateur peut s’inscrire aux notifications.

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





