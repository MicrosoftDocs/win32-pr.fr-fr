---
title: Propriété GetTransportInformationOperation terminée
description: Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par GetTransportInformationAsync est terminée.
ms.assetid: 11E60E00-75B5-4412-B115-4438255AEB8A
keywords:
- API de diffusion multimédia en continu des propriétés terminées
- API de diffusion multimédia en continu des propriétés, interface GetTransportInformationOperation
- API de diffusion multimédia en continu de l’interface GetTransportInformationOperation, propriété terminée
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.Completed
- GetTransportInformationOperation.get_Completed
- GetTransportInformationOperation.put_Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 389d7b281c10458e854407f9ce02bd2656fe6d4b16574408d75ae06ccc06d7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735782"
---
# <a name="gettransportinformationoperationcompleted-property"></a>GetTransportInformationOperation :: Completed, propriété

Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) est terminée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a>Valeur de la propriété

Gestionnaire d'événements.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 

 