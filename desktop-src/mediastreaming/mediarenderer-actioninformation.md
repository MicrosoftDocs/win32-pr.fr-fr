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
ms.openlocfilehash: f23b0463397f38dd8d438f21767ca9e45c9f68465bee4452d46a63b3a3dc9027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972148"
---
# <a name="mediarendereractioninformation-property"></a>MediaRenderer. ActionInformation, propriété

Obtient des informations sur les méthodes qui peuvent être appelées actuellement sur la DMR.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="property-value"></a>Valeur de la propriété

Référence à une interface [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 