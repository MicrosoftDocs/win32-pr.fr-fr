---
description: 'Version accessible à distance de la méthode IMFMediaEventGenerator :: EndGetEvent.'
ms.assetid: 5b793760-546c-43d4-8251-d89d8d7152ad
title: RemoteEndGetEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 709cb65280e32c1aa662c5dfbec851b24d353370853db1742814a4ba5daf61de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034897"
---
# <a name="remoteendgetevent"></a>RemoteEndGetEvent

Version accessible à distance de la méthode [**IMFMediaEventGenerator :: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) .

``` syntax
[call_as(EndGetEvent)]
HRESULT RemoteEndGetEvent(
    IUnknown *pResult,
    DWORD *pcbEvent,
    BYTE **ppbEvent
);
```

## <a name="remarks"></a>Remarques

Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode. La méthode n’apparaît pas dans le vtable pour l’interface. Si [**EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                                              |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




