---
description: 'Version accessible à distance de la méthode IMFMediaStream :: RequestSample.'
ms.assetid: 05ed4de0-fe5c-4183-8f1d-55d5a27e436a
title: RemoteRequestSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b572a9de9a74a744b9a9fc2c31dd816900301da623869cecdb03820ccbcf1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034907"
---
# <a name="remoterequestsample"></a>RemoteRequestSample

Version accessible à distance de la méthode [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .

``` syntax
[call_as(RequestSample)]
HRESULT RemoteRequestSample();
```

## <a name="remarks"></a>Remarques

Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode. La méthode n’apparaît pas dans le vtable pour l’interface. Si [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                                              |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)
</dt> </dl>

 

 




