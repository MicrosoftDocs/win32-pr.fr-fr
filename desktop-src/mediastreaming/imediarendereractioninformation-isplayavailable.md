---
title: Méthode IMediaRendererActionInformation IsPlayAvailable
description: Récupère une valeur qui indique si le DMR accepte actuellement les méthodes PlayAsync et PlayAtSpeedAsync.
ms.assetid: 969C55FA-872D-4063-B85C-573C8DA5593C
keywords:
- API de diffusion multimédia en continu de méthode IsPlayAvailable
- API de diffusion multimédia en continu de méthode IsPlayAvailable, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode IsPlayAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPlayAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 912e5478ef1d9bd7114d198a9671d38ba7b721c9dbd82d2a8080b5a7876e76cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235844"
---
# <a name="imediarendereractioninformationisplayavailable-method"></a>IMediaRendererActionInformation :: IsPlayAvailable, méthode

Récupère une valeur qui indique si le DMR accepte actuellement les méthodes [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) et [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsPlayAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Valeur booléenne qui est **true** si la dernière accepte les méthodes [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) et [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) , et **false** si ce n’est pas le cas.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

