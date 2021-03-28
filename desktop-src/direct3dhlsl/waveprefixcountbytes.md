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
ms.openlocfilehash: 72f35df1e463ff89441938e4cae19a890821baf9
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032095"
---
# <a name="waveprefixcountbits-function"></a><span data-ttu-id="137e2-104">WavePrefixCountBits fonction)</span><span class="sxs-lookup"><span data-stu-id="137e2-104">WavePrefixCountBits function</span></span>

<span data-ttu-id="137e2-105">Retourne la somme de toutes les variables booléennes spécifiées ayant la valeur true sur tous les couloirs actifs dont les index sont plus petits que le couloir actuel.</span><span class="sxs-lookup"><span data-stu-id="137e2-105">Returns the sum of all the specified boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="137e2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="137e2-106">Syntax</span></span>


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="137e2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="137e2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="137e2-108">*bBit*</span><span class="sxs-lookup"><span data-stu-id="137e2-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="137e2-109">Variables booléennes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="137e2-109">The specified boolean variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="137e2-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="137e2-110">Return value</span></span>

<span data-ttu-id="137e2-111">Somme de toutes les variables booléennes spécifiées ayant la valeur true sur tous les couloirs actifs avec des index plus petits que la voie actuelle.</span><span class="sxs-lookup"><span data-stu-id="137e2-111">The sum of all the specified Boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="137e2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="137e2-112">Remarks</span></span>

<span data-ttu-id="137e2-113">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="137e2-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="137e2-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="137e2-114">Examples</span></span>

<span data-ttu-id="137e2-115">Le code suivant décrit comment implémenter une écriture compactée dans un flux ordonné, où le nombre d’éléments écrits par voie Lane est 1 ou 0.</span><span class="sxs-lookup"><span data-stu-id="137e2-115">The following code describes how to implement a compacted write to an ordered stream where the number of elements written per lane is either 1 or 0.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="137e2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="137e2-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="137e2-117">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="137e2-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="137e2-118">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="137e2-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




