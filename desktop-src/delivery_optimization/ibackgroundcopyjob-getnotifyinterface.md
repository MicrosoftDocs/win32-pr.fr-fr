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
ms.openlocfilehash: ef8eab6c101cadde2b715c48fe3dae2443e72e93f623b397036e2467bcbf0b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755379"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | Le pointeur d’interface de notification a été correctement récupéré.<br/> |



 

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

[**Méthode ibackgroundcopyjob :: GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





