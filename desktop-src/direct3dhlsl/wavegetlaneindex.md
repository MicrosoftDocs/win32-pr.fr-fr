---
title: WaveGetLaneIndex fonction)
description: Retourne l’index de la voie active dans l’onde actuelle.
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- WaveGetLaneIndex fonction HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8adea1091739981523ab19b69158ead9aafa600c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104991032"
---
# <a name="wavegetlaneindex-function"></a>WaveGetLaneIndex fonction)

Retourne l’index de la voie active dans l’onde actuelle.

## <a name="syntax"></a>Syntaxe

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Index Lane actuel. Le résultat sera compris entre 0 et le résultat renvoyé par [**WaveGetLaneCount**](wavegetlanecount.md).

## <a name="remarks"></a>Notes

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




