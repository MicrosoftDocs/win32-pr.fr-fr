---
title: Méthode IMediaRendererActionInformation IsVolumeAvailable
description: Récupère une valeur qui indique si DMR est capable d’ajuster le niveau de volume audio.
ms.assetid: 6DFDC37A-3304-4CDB-9928-C113D2F64ED0
keywords:
- API de diffusion multimédia en continu de méthode IsVolumeAvailable
- API de diffusion multimédia en continu de méthode IsVolumeAvailable, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode IsVolumeAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsVolumeAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce36a9151998a5f7b0a7785aebc1795bd29d31ff47cfdd2368978ad040f3597c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972208"
---
# <a name="imediarendereractioninformationisvolumeavailable-method"></a>IMediaRendererActionInformation :: IsVolumeAvailable, méthode

Récupère une valeur qui indique si DMR est capable d’ajuster le niveau de volume audio.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsVolumeAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Valeur booléenne qui est **true** si la fonction DMR est capable d’ajuster le niveau de volume audio et **false** si ce n’est pas le cas.

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

 

