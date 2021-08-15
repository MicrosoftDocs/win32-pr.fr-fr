---
title: WaveActiveBitXor fonction)
description: Retourne l’opérateur de bits XOR de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et les réplique sur tous les couloirs actifs.
ms.assetid: A6807D17-1E6E-4997-AB52-32FAB5857219
keywords:
- WaveActiveBitXor fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 733ab8c40a59b784af8a7d50c4f8e1e543f344ee2d75ed9b6896992e6176ff18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504879"
---
# <a name="waveactivebitxor-function"></a>WaveActiveBitXor fonction)

Retourne l’opérateur de bits XOR de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et les réplique sur tous les couloirs actifs.

## <a name="syntax"></a>Syntaxe

``` syntax
<int_type> WaveActiveBitXor(
   <int_type> expr
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*expr* 
</dt> <dd>

Expression à évaluer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur XOR au niveau du bit.

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




