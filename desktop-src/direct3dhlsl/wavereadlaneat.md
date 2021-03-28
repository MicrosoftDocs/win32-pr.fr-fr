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
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2020
ms.locfileid: "104381742"
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

## <a name="remarks"></a>Notes

Cette fonction est effectivement une diffusion de la valeur dans la voie laneIndex’th.

Cette fonction est prise en charge à partir du Shader Model 6,0, dans les types suivants de nuanceurs :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




