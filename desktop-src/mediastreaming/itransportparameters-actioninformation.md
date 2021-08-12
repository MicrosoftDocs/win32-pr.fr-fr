---
title: Méthode ITransportParameters ActionInformation
description: Obtient une interface IMediaRendererActionInformation qui fournit des informations sur les méthodes qui peuvent être appelées actuellement sur la DMR.
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- API de diffusion multimédia en continu de méthode ActionInformation
- API de diffusion multimédia en continu de méthode ActionInformation, interface ITransportParameters
- API de diffusion multimédia en continu de l’interface ITransportParameters, méthode ActionInformation
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 551612fcaffb9379823efea15f29ed9feba1ff3d0c5af6e7271b61ad9d6036f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235854"
---
# <a name="itransportparametersactioninformation-method"></a>ITransportParameters :: ActionInformation, méthode

Obtient une interface [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) qui fournit des informations sur les méthodes qui peuvent être appelées actuellement sur la DMR.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ out, retval\]
</dt> <dd>

Reçoit une référence à une interface [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

