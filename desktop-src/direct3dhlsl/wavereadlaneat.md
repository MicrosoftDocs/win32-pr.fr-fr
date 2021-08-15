---
title: WaveReadLaneAt fonction)
description: Retourne la valeur de l’expression pour l’index Lane donné dans l’onde spécifiée.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- WaveReadLaneAt fonction HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08fa669f8c4284c26052dd68bdbe9ab4f5b99b80b8bdf9445aa3375f0a87a9c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504619"
---
# <a name="wavereadlaneat-function"></a>WaveReadLaneAt fonction)

Retourne la valeur de l’expression pour l’index Lane donné dans l’onde spécifiée.

## <a name="syntax"></a>Syntaxe

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*expr* 
</dt> <dd>

Expression à évaluer.

</dd> <dt>

*laneIndex* 
</dt> <dd>

Index de la voie pour laquelle le résultat *expr* sera retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur résultante est le résultat de *expr*. Elle est uniforme si *laneIndex* est uniforme.

## <a name="remarks"></a>Remarques

Cette fonction est effectivement une diffusion de la valeur de la *laneIndex*« ième allée ».

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.

## <a name="see-also"></a>Voir aussi

* [Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [Shader, modèle 6](shader-model-6-0.md)
