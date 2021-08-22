---
description: 'Version accessible à distance de la méthode IMFWorkQueueServices :: BeginRegisterPlatformWorkQueueWithMMCSS.'
ms.assetid: 158497a9-9d66-4e58-919d-e35765fd29e4
title: RemoteBeginRegisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b19d163e8f3e34a9d4b0eca70f70c15442f683450319243e80f3842548f78d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974278"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcss"></a>RemoteBeginRegisterPlatformWorkQueueWithMMCSS

Version accessible à distance de la méthode [**IMFWorkQueueServices :: BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) .

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSS(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>Remarques

Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode. La méthode n’apparaît pas dans le vtable pour l’interface. Si [**BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




