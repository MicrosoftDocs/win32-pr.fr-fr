---
title: Méthode IMediaRendererActionInformation PlaySpeeds
description: Récupère la liste complète des valeurs PlaySpeed acceptées par le DMR.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- API de diffusion multimédia en continu de méthode PlaySpeeds
- API de diffusion multimédia en continu de méthode PlaySpeeds, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode PlaySpeeds
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 573fe9da4e71f9c16a9850da352e866ddbb0f77abc8c30861f2aa29647065fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972198"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a>IMediaRendererActionInformation ::P méthode laySpeeds

Récupère la liste complète des valeurs [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) acceptées par le DMR.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit un vecteur de structures [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) spécifiant la liste complète des valeurs **PlaySpeed** qui sont acceptées par le DMR.

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

 

