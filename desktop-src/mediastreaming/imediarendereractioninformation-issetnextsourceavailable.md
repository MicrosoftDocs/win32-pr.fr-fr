---
title: Méthode IMediaRendererActionInformation IsSetNextSourceAvailable
description: Récupère une valeur qui indique si DMR accepte actuellement la méthode SetNextSourceFromUriAsync, la méthode SetNextSourceFromStreamAsync ou la méthode SetNextSourceFromMediaSourceAsync.
ms.assetid: 7588E992-4070-4E0F-8C4B-7DFC097A5076
keywords:
- API de diffusion multimédia en continu de méthode IsSetNextSourceAvailable
- API de diffusion multimédia en continu de méthode IsSetNextSourceAvailable, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode IsSetNextSourceAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSetNextSourceAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee18eadbc535dd2cd4b48ec6f77adb1d3dec2f5a0c1f5065cee009e27635eda9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092299"
---
# <a name="imediarendereractioninformationissetnextsourceavailable-method"></a>IMediaRendererActionInformation :: IsSetNextSourceAvailable, méthode

Récupère une valeur qui indique si DMR accepte actuellement la méthode [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , la méthode [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) ou la méthode [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsSetNextSourceAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Valeur booléenne qui est **true** si la méthode DMR accepte actuellement la méthode [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , la méthode [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) ou la méthode [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) , et **false** si ce n’est pas le cas.

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

 

