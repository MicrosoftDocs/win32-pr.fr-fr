---
title: D2DSampleInput, fonction (D2d1effecthelpers. h)
description: Échantillonne l’entrée N à la position UV. Disponible uniquement pour les entrées complexes.
ms.assetid: 8C1E3B23-D05B-4FCC-B32F-A5870A7C3FEF
keywords:
- D2DSampleInput fonction Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5929e9c113e5fa9a7c8a72003357b280a810e49e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534888"
---
# <a name="d2dsampleinput-function"></a><span data-ttu-id="1b4ac-105">D2DSampleInput fonction)</span><span class="sxs-lookup"><span data-stu-id="1b4ac-105">D2DSampleInput function</span></span>

<span data-ttu-id="1b4ac-106">Échantillonne l’entrée N à la position UV.</span><span class="sxs-lookup"><span data-stu-id="1b4ac-106">Samples input N at position uv.</span></span> <span data-ttu-id="1b4ac-107">Disponible uniquement pour les entrées complexes.</span><span class="sxs-lookup"><span data-stu-id="1b4ac-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b4ac-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b4ac-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="1b4ac-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b4ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b4ac-110">*N* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b4ac-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4ac-111">Numéro d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1b4ac-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="1b4ac-112">*UV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b4ac-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4ac-113">Position UV.</span><span class="sxs-lookup"><span data-stu-id="1b4ac-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b4ac-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b4ac-114">Return value</span></span>

<span data-ttu-id="1b4ac-115">La fonction retourne un **float4**, au format TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="1b4ac-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b4ac-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1b4ac-116">Remarks</span></span>

<span data-ttu-id="1b4ac-117">L’exemple suivant illustre la fonction utilisée pour calculer les normales des surfaces.</span><span class="sxs-lookup"><span data-stu-id="1b4ac-117">The following example shows the function being used to calculate surface normals.</span></span>

``` syntax
   
float3 CalculateSurfaceNormal(TAPARGS)  
{  
    float3 normal = float3(0, 0, 1.0);  
  
    // unrolled loop  
    normal.xy += tap1.zw * D2DSampleInput(0, tap1.xy).a;  
    normal.xy += tap2.zw * D2DSampleInput(0, tap2.xy).a;  
    normal.xy += tap3.zw * D2DSampleInput(0, tap3.xy).a;  
    normal.xy += tap4.zw * D2DSampleInput(0, tap4.xy).a;  
    normal.xy += tap5.zw * D2DSampleInput(0, tap5.xy).a;  
    normal.xy += tap6.zw * D2DSampleInput(0, tap6.xy).a;  
  
    normal = normalize(normal);  
      
    return normal;  
}  
```

## <a name="requirements"></a><span data-ttu-id="1b4ac-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b4ac-118">Requirements</span></span>



| <span data-ttu-id="1b4ac-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b4ac-119">Requirement</span></span> | <span data-ttu-id="1b4ac-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b4ac-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b4ac-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b4ac-121">Header</span></span><br/> | <dl> <span data-ttu-id="1b4ac-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="1b4ac-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="1b4ac-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1b4ac-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="1b4ac-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b4ac-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="1b4ac-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b4ac-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b4ac-126">Liaison de nuanceurs d’effet</span><span class="sxs-lookup"><span data-stu-id="1b4ac-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="1b4ac-127">Applications auxiliaires HLSL</span><span class="sxs-lookup"><span data-stu-id="1b4ac-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





