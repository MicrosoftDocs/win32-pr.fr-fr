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
ms.openlocfilehash: bb8dc60c25cf3ec12e0ebeaa863e239c287d7c46
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101509"
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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

