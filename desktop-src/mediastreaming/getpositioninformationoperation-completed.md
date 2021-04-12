---
title: GetPositionInformationOperation. Completed, propriété
description: Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par GetPositionInformationAsync est terminée.
ms.assetid: 144065AE-6C23-4E9D-B9D0-6849E7FB74C4
keywords:
- API de diffusion multimédia en continu des propriétés terminées
- API de diffusion multimédia en continu des propriétés, interface GetPositionInformationOperation
- API de diffusion multimédia en continu de l’interface GetPositionInformationOperation, propriété terminée
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90b4ed4a6402b8c7bfc1ee559bd0b43765a64cec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381923"
---
# <a name="getpositioninformationoperationcompleted-property"></a>GetPositionInformationOperation. Completed, propriété

Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) est terminée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Completed(
  [in]  GetPositionInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetPositionInformationCompletedHandler **value
);
```



## <a name="property-value"></a>Valeur de la propriété

Gestionnaire d'événements.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetPositionInformationOperation**](getpositioninformationoperation.md)
</dt> </dl>

 

 