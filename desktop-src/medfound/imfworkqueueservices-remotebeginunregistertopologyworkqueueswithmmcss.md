---
description: 'Version accessible à distance de la méthode IMFWorkQueueServices :: BeginUnregisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 1a168462-400d-46c9-a489-7b861770469f
title: RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb4fe3fe7f7f82e426eabe2ffd6e0aadb19879ceef713c4a66c44ee4cfceea50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724449"
---
# <a name="remotebeginunregistertopologyworkqueueswithmmcss"></a>RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS

Version accessible à distance de la méthode [**IMFWorkQueueServices :: BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) .

``` syntax
[call_as(BeginUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>Remarques

Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode. La méthode n’apparaît pas dans le vtable pour l’interface. Si [**BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.

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

 

 




