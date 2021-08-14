---
title: WavePrefixCountBits fonction)
description: Retourne la somme de toutes les variables booléennes spécifiées ayant la valeur true sur tous les couloirs actifs dont les index sont plus petits que le couloir actuel.
ms.assetid: AEC9AFD7-6478-4397-B531-73990D30AA48
keywords:
- WavePrefixCountBits fonction HLSL
topic_type:
- apiref
api_name:
- WavePrefixCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 048b63d24e87d97f0e0223083a91694c0471b9e38ad21afbc487c02d711d720d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504675"
---
# <a name="waveprefixcountbits-function"></a>WavePrefixCountBits fonction)

Retourne la somme de toutes les variables booléennes spécifiées ayant la valeur true sur tous les couloirs actifs dont les index sont plus petits que le couloir actuel.

## <a name="syntax"></a>Syntaxe


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bBit* 
</dt> <dd>

Variables booléennes spécifiées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Somme de toutes les variables booléennes spécifiées ayant la valeur true sur tous les couloirs actifs avec des index plus petits que la voie actuelle.

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 



 

## <a name="examples"></a>Exemples

Le code suivant décrit comment implémenter une écriture compactée dans un flux ordonné, où le nombre d’éléments écrits par voie Lane est 1 ou 0.

``` syntax
bool bDoesThisLaneHaveAnAppendItem = <expr>;
// compute number of items to append for the whole wave
uint laneAppendOffset = WavePrefixCountBits( bDoesThisLaneHaveAnAppendItem );
uint appendCount = WaveActiveCountBits( bDoesThisLaneHaveAnAppendItem);
// update the output location for this whole wave
uint appendOffset;
if ( WaveIsFirstLane () )
{
    // this way, we only issue one atomic for the entire wave, which reduces contention
    // and keeps the output data for each lane in this wave together in the output buffer
    InterlockedAdd(bufferSize, appendCount, appendOffset);
}
appendOffset = WaveReadLaneFirst( appendOffset ); // broadcast value
appendOffset += laneAppendOffset; // and add in the offset for this lane
buffer[appendOffset] = myData; // write to the offset location for this lane
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




