---
title: Méthode méthode ibackgroundcopyjob GetNotifyInterface (Deliveryoptimization. h)
description: Récupère le pointeur d’interface vers votre implémentation de l’interface IBackgroundCopyCallback.
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- Méthode GetNotifyInterface
- Méthode GetNotifyInterface, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6586a90de5783ceb24e5a7677f699a9cf6dfa60c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921748"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a>Méthode ibackgroundcopyjob :: GetNotifyInterface, méthode

Récupère le pointeur d’interface vers votre implémentation de l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppNotifyInterface* \[ à\]
</dt> <dd>

Pointeur d’interface vers votre implémentation de l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) . Lorsque vous avez terminé, libérez *ppNotifyInterface*.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | Le pointeur d’interface de notification a été correctement récupéré.<br/> |



 

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





