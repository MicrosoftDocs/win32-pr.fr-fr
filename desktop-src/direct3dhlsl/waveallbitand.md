---
title: WaveActiveBitAnd fonction)
description: Retourne l’opération de bits AND de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique vers tous les couloirs actifs.
ms.assetid: 602884CD-E656-4DEB-A30A-8A7D127A2217
keywords:
- WaveActiveBitAnd fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96d09d91df4ff9226a8fb86203be0bd79bc3c11d1882553607358c3c84d3814c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282997"
---
# <a name="waveactivebitand-function"></a>WaveActiveBitAnd fonction)

Retourne l’opération de bits AND de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique vers tous les couloirs actifs.

## <a name="syntax"></a>Syntaxe


``` syntax
<int_type> WaveActiveBitAnd(
   <int_type> expr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*expr* 
</dt> <dd>

Expression à évaluer.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Valeur and au niveau du bit.

## <a name="remarks"></a>Notes

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




