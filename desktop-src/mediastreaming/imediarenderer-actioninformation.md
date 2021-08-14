---
title: Méthode IMediaRenderer ActionInformation
description: Récupère des informations sur les méthodes qui peuvent être appelées actuellement sur la DMR.
ms.assetid: 7681FF92-DD13-4BBC-B860-E2BDFDA74FB9
keywords:
- API de diffusion multimédia en continu de méthode ActionInformation
- API de diffusion multimédia en continu de méthode ActionInformation, interface IMediaRenderer
- API de diffusion multimédia en continu de l’interface IMediaRenderer, méthode ActionInformation
topic_type:
- apiref
api_name:
- IMediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3caf251c080f218b99861d4a81920cd5c95c1f0e53bc6b006c84536f33f7f29c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735522"
---
# <a name="imediarendereractioninformation-method"></a>IMediaRenderer :: ActionInformation, méthode

Récupère des informations sur les méthodes qui peuvent être appelées actuellement sur la DMR.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit une référence à une interface [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

