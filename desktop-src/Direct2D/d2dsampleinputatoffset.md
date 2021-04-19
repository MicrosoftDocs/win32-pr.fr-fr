---
title: D2DSampleInputAtOffset, fonction (D2d1effecthelpers. h)
description: Échantillonne l’entrée N à un offset de décalage par rapport à la coordonnée d’entrée. Disponible uniquement pour les entrées complexes.
ms.assetid: 4A01264E-04E3-49BD-9EF8-7834D9B8B0B8
keywords:
- D2DSampleInputAtOffset fonction Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtOffset
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7718f8f48ddfd316d1312dbdff3a5da1f45dfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545659"
---
# <a name="d2dsampleinputatoffset-function"></a><span data-ttu-id="3deb4-105">D2DSampleInputAtOffset fonction)</span><span class="sxs-lookup"><span data-stu-id="3deb4-105">D2DSampleInputAtOffset function</span></span>

<span data-ttu-id="3deb4-106">Échantillonne l’entrée N à un offset de décalage par rapport à la coordonnée d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3deb4-106">Samples input N at an offset of offset from the input coordinate.</span></span> <span data-ttu-id="3deb4-107">Disponible uniquement pour les entrées complexes.</span><span class="sxs-lookup"><span data-stu-id="3deb4-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="3deb4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3deb4-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInputAtOffset(
  in uint N,
  in float2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="3deb4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3deb4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3deb4-110">*N* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3deb4-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3deb4-111">Numéro d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3deb4-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="3deb4-112">*décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3deb4-112">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3deb4-113">Décalage UV.</span><span class="sxs-lookup"><span data-stu-id="3deb4-113">The uv offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3deb4-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3deb4-114">Return value</span></span>

<span data-ttu-id="3deb4-115">La fonction retourne un **float4**, au format TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="3deb4-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="3deb4-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3deb4-116">Remarks</span></span>

<span data-ttu-id="3deb4-117">L’exemple suivant illustre la fonction utilisée dans le cadre d’un masque de dégradé de mise en surbrillance et d’ombres.</span><span class="sxs-lookup"><span data-stu-id="3deb4-117">The following example shows the function being used as part of a highlighting and shadows gradient mask.</span></span>

``` syntax
  
D2D_PS_ENTRY(HighlightsAndShadowsGradientMask)  
{  
    MIN_TYPE(float4) blurred = D2DGetInput(0);  
  
    // Compute X and Y gradients 
    MIN_TYPE(float) dX1 = D2DSampleInputAtOffset(0, float2(1, 0));
    MIN_TYPE(float) dX2 = D2DSampleInputAtOffset(0, float2(-1, 0));
    MIN_TYPE(float) dY1 = D2DSampleInputAtOffset(0, float2(0, 1));
    MIN_TYPE(float) dY2 = D2DSampleInputAtOffset(0, float2(0, -1));
    
    // TODO: math to calculate shadow gradients

    // Return the value in the alpha channel.  
    blurred.a = // TODO: math to calculate blurred value
  
    return blurred;  
}  
```

## <a name="requirements"></a><span data-ttu-id="3deb4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3deb4-118">Requirements</span></span>



| <span data-ttu-id="3deb4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3deb4-119">Requirement</span></span> | <span data-ttu-id="3deb4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3deb4-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3deb4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3deb4-121">Header</span></span><br/> | <dl> <span data-ttu-id="3deb4-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="3deb4-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="3deb4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3deb4-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="3deb4-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3deb4-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="3deb4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3deb4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3deb4-126">Liaison de nuanceurs d’effet</span><span class="sxs-lookup"><span data-stu-id="3deb4-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="3deb4-127">Applications auxiliaires HLSL</span><span class="sxs-lookup"><span data-stu-id="3deb4-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





