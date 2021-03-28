---
title: WaveActiveMax fonction)
description: Retourne la valeur maximale de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique sur tous les couloirs actifs.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- WaveActiveMax fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c0fd10f578d598c326cdfb4cf943d3a35fe78a9
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2020
ms.locfileid: "104383384"
---
# <a name="waveactivemax-function"></a>WaveActiveMax fonction)

Retourne la valeur maximale de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique sur tous les couloirs actifs.

## <a name="syntax"></a>Syntaxe

``` syntax
<type> WaveActiveMax(
   <type> expr
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*expr* 
</dt> <dd>

Expression à évaluer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur maximale.

## <a name="remarks"></a>Notes

L’ordre des opérations n’est pas défini.

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 



 

## <a name="examples"></a>Exemples

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




