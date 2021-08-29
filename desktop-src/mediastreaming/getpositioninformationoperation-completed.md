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
ms.openlocfilehash: 847a910f537bc09d766c7e131824b276ed80dfed5490f425b82ae6632c93fc97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886929"
---
# <a name="getpositioninformationoperationcompleted-property"></a>GetPositionInformationOperation. Completed, propriété

Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) est terminée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Completed(
  [in]  GetPositionInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetPositionInformationCompletedHandler **value
);
```



## <a name="property-value"></a>Valeur de la propriété

Gestionnaire d'événements.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetPositionInformationOperation**](getpositioninformationoperation.md)
</dt> </dl>

 

 