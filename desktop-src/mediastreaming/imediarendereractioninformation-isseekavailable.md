---
title: Méthode IMediaRendererActionInformation IsSeekAvailable
description: Récupère une valeur qui indique si DMR accepte actuellement la méthode SeekAsync.
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- API de diffusion multimédia en continu de méthode IsSeekAvailable
- API de diffusion multimédia en continu de méthode IsSeekAvailable, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode IsSeekAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32b5c7eef78dad4ebfeeebb40c323d7b13e540033eb54852f7da41942f5ec83e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735512"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a>IMediaRendererActionInformation :: IsSeekAvailable, méthode

Récupère une valeur qui indique si DMR accepte actuellement la méthode [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Valeur booléenne qui est **true** si DMR accepte actuellement la méthode [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) et **false** si ce n’est pas le cas.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

