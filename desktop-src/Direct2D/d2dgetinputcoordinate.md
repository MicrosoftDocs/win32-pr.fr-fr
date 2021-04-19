---
title: D2DGetInputCoordinate, fonction (D2d1effecthelpers. h)
description: Retourne la valeur de l’TEXCOORDN d’entrée. Disponible uniquement pour les entrées complexes.
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- D2DGetInputCoordinate fonction Direct2D
topic_type:
- apiref
api_name:
- D2DGetInputCoordinate
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5d9ee759de12bb8b017d582026dd5b5ca8c3fb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541724"
---
# <a name="d2dgetinputcoordinate-function"></a><span data-ttu-id="f835f-105">D2DGetInputCoordinate fonction)</span><span class="sxs-lookup"><span data-stu-id="f835f-105">D2DGetInputCoordinate function</span></span>

<span data-ttu-id="f835f-106">Retourne la valeur de l’TEXCOORDN d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f835f-106">Returns the value of the input TEXCOORDN.</span></span> <span data-ttu-id="f835f-107">Disponible uniquement pour les entrées complexes.</span><span class="sxs-lookup"><span data-stu-id="f835f-107">Available only for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f835f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f835f-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="f835f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f835f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f835f-110">*N* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f835f-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f835f-111">Numéro d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f835f-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f835f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f835f-112">Return value</span></span>

<span data-ttu-id="f835f-113">La fonction retourne un **float4**, au format TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="f835f-113">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="f835f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f835f-114">Remarks</span></span>

<span data-ttu-id="f835f-115">La coordonnée retournée par cette fonction se trouve dans l’espace Texel.</span><span class="sxs-lookup"><span data-stu-id="f835f-115">The coordinate returned by this function is in texel space.</span></span> <span data-ttu-id="f835f-116">Un nuanceur ne doit pas prendre de dépendances quant à la façon dont cette valeur est calculée.</span><span class="sxs-lookup"><span data-stu-id="f835f-116">A shader shouldn't take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="f835f-117">Il doit l’utiliser uniquement pour échantillonner l’entrée du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="f835f-117">It should use it only to sample the pixel shader's input.</span></span> <span data-ttu-id="f835f-118">Pour plus d’informations, consultez [Ajout d’un nuanceur de pixels à une transformation personnalisée](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).</span><span class="sxs-lookup"><span data-stu-id="f835f-118">For more info, see [Adding a pixel shader to a custom transform](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).</span></span>

<span data-ttu-id="f835f-119">L’exemple suivant illustre la fonction utilisée pour un effet de mappage de déplacement.</span><span class="sxs-lookup"><span data-stu-id="f835f-119">The following example shows the function used for a displacement map effect.</span></span>

``` syntax
float2 GetDisplacementOffset(float4 uv0, float4 uv1)  
{  
    // TODO: return the displacement offset 
}  
  
D2D_PS_ENTRY(DisplacementMapBilinear)  
{  
    const float4 coord0 = D2DGetInputCoordinate(0);  
    const float4 coord1 = D2DGetInputCoordinate(1);  
    return D2DSampleInput(0, GetDisplacementOffset(coord0, coord1) * coord0.zw + coord0.xy);  
}  
```

## <a name="requirements"></a><span data-ttu-id="f835f-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f835f-120">Requirements</span></span>



| <span data-ttu-id="f835f-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f835f-121">Requirement</span></span> | <span data-ttu-id="f835f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f835f-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f835f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f835f-123">Header</span></span><br/> | <dl> <span data-ttu-id="f835f-124"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="f835f-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="f835f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f835f-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="f835f-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f835f-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="f835f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f835f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f835f-128">Liaison de nuanceurs d’effet</span><span class="sxs-lookup"><span data-stu-id="f835f-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="f835f-129">Applications auxiliaires HLSL</span><span class="sxs-lookup"><span data-stu-id="f835f-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

