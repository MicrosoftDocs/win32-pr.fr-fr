---
title: Méthode IMediaRenderer IsAudioSupported
description: Récupère une valeur qui indique si DMR peut lire du contenu audio.
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- API de diffusion multimédia en continu de méthode IsAudioSupported
- API de diffusion multimédia en continu de méthode IsAudioSupported, interface IMediaRenderer
- API de diffusion multimédia en continu de l’interface IMediaRenderer, méthode IsAudioSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5abe42e65e451464a5f7f3a4d59679db62c3634e95e89e5e275919dd0ece869e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777009"
---
# <a name="imediarendererisaudiosupported-method"></a>IMediaRenderer :: IsAudioSupported, méthode

Récupère une valeur qui indique si DMR peut lire du contenu audio.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Valeur booléenne qui est **true** si DMR est capable de diffuser du contenu audio et **false** si ce n’est pas le cas.

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

 

 





