---
description: 'Version accessible à distance de la méthode IMFWorkQueueServices :: EndUnregisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 8767a145-07b9-4427-9446-cee25e9074fa
title: RemoteEndUnregisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1131fcd920e306bc6d5f2954c283d41d61310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524294"
---
# <a name="remoteendunregistertopologyworkqueueswithmmcss"></a>RemoteEndUnregisterTopologyWorkQueuesWithMMCSS

Version accessible à distance de la méthode [**IMFWorkQueueServices :: EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) .

``` syntax
[call_as(EndUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndUnregisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a>Notes

Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode. La méthode n’apparaît pas dans le vtable pour l’interface. Si [**EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




