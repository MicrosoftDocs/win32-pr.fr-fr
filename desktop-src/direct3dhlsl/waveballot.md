---
title: WaveActiveBallot fonction)
description: Retourne un uint4 contenant un masque de masque de l’évaluation de l’expression booléenne pour tous les couloirs actifs dans l’onde actuelle.
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- WaveActiveBallot fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104508197"
---
# <a name="waveactiveballot-function"></a>WaveActiveBallot fonction)

Retourne un uint4 contenant un masque de masque de l’évaluation de l’expression booléenne pour tous les couloirs actifs dans l’onde actuelle. 

## <a name="syntax"></a>Syntaxe

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*expr* 
</dt> <dd>

Expression booléenne à évaluer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Uint4 contenant un masque de masque de l’évaluation de l’expression booléenne pour tous les couloirs actifs dans l’onde actuelle. Le bit le moins significatif correspond à la voie avec l’index zéro. Les bits correspondant aux couloirs inactifs sont nuls. Les bits qui sont supérieurs ou égaux à [**WaveGetLaneCount**](wavegetlanecount.md) seront nuls.

## <a name="remarks"></a>Notes

Les différents GPU ont des largeurs de processeur SIMD différentes (nombre de voies Lane). La plupart de ces fonctions **WaveXXX** peuvent fonctionner au niveau d’abstraction où la largeur de l’ordinateur SIMD est masquée. Pour optimiser la portabilité du code sur les GPU, utilisez les fonctions intrinsèques qui ne reposent pas sur la largeur de l’ordinateur. Par exemple, utilisez :

``` syntax
uint result = WaveActiveCountBits( bBit );
```

À la place de :

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 



 

## <a name="examples"></a>Exemples

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




