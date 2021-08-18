---
title: Méthode IMediaRendererFactory CreateMediaRendererAsync
description: Crée de façon asynchrone une nouvelle instance d’un objet qui implémente l’interface IMediaRenderer à l’aide du nom de périphérique unique spécifié (UDN).
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- API de diffusion multimédia en continu de méthode CreateMediaRendererAsync
- API de diffusion multimédia en continu de méthode CreateMediaRendererAsync, interface IMediaRendererFactory
- API de diffusion multimédia en continu de l’interface IMediaRendererFactory, méthode CreateMediaRendererAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e459324d96f031ab3433f0d8bfe8ba5de562d76c95f51affd7b72d130655fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735486"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a>IMediaRendererFactory :: CreateMediaRendererAsync, méthode

Crée de façon asynchrone une nouvelle instance d’un objet qui implémente l’interface [**IMediaRenderer**](imediarenderer.md) à l’aide du nom de périphérique unique spécifié (UDN).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*deviceIdentifier* \[ dans\]
</dt> <dd>

HSTRING contenant un UDN qui identifie l’appareil DMR DLNA pour lequel une instance de [**IMediaRenderer**](imediarenderer.md) sera créée.

</dd> <dt>

*valeur* \[ out, retval\]
</dt> <dd>

Reçoit une référence à un objet [**CreateMediaRendererOperation**](createmediarendereroperation.md) qui est utilisé pour obtenir les résultats de l’opération asynchrone.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

