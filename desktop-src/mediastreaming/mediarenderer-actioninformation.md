---
title: MediaRenderer. ActionInformation, propriété
description: Obtient des informations sur les méthodes qui peuvent être appelées actuellement sur la DMR.
ms.assetid: c36d45cb-c01a-4418-8f21-906c95950d6f
keywords:
- API de diffusion multimédia en continu des propriétés ActionInformation
- API de diffusion multimédia en continu des propriétés ActionInformation, interface MediaRenderer
- API de diffusion multimédia en continu de l’interface MediaRenderer, propriété ActionInformation
topic_type:
- apiref
api_name:
- MediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f5ce6c0bf9baf30cd8184d5271ed996c6406ddf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510062"
---
# <a name="mediarendereractioninformation-property"></a>MediaRenderer. ActionInformation, propriété

Obtient des informations sur les méthodes qui peuvent être appelées actuellement sur la DMR.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="property-value"></a>Valeur de la propriété

Référence à une interface [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 