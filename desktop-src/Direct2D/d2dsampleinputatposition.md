---
title: D2DSampleInputAtPosition, fonction (D2d1effecthelpers. h)
description: Échantillonne l’entrée N à une position de scène absolue, plutôt qu’une position relative à l’entrée. Disponible uniquement pour les entrées complexes.
ms.assetid: E839287F-91D1-4591-8DE7-1DFC3001A23D
keywords:
- D2DSampleInputAtPosition fonction Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtPosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12bba2b83f3956cf4b654c00b0650a6a0ce9a54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544489"
---
# <a name="d2dsampleinputatposition-function"></a><span data-ttu-id="59fd5-105">D2DSampleInputAtPosition fonction)</span><span class="sxs-lookup"><span data-stu-id="59fd5-105">D2DSampleInputAtPosition function</span></span>

<span data-ttu-id="59fd5-106">Échantillonne l’entrée N à une position de scène absolue, plutôt qu’une position relative à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="59fd5-106">Samples input N at an absolute scene position, rather than an input-relative position.</span></span> <span data-ttu-id="59fd5-107">Disponible uniquement pour les entrées complexes.</span><span class="sxs-lookup"><span data-stu-id="59fd5-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="59fd5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59fd5-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInputAtPosition(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="59fd5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59fd5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59fd5-110">*N* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59fd5-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59fd5-111">Numéro d’entrée.</span><span class="sxs-lookup"><span data-stu-id="59fd5-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="59fd5-112">*UV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59fd5-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59fd5-113">Position UV.</span><span class="sxs-lookup"><span data-stu-id="59fd5-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59fd5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59fd5-114">Return value</span></span>

<span data-ttu-id="59fd5-115">La fonction retourne un **float4**, au format TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="59fd5-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="59fd5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="59fd5-116">Remarks</span></span>

<span data-ttu-id="59fd5-117">L’exemple suivant illustre la fonction utilisée dans un retour circulaire à la ligne.</span><span class="sxs-lookup"><span data-stu-id="59fd5-117">The following example shows the function used in a circular wrap.</span></span>

``` syntax
  
D2D_PS_ENTRY(CircularWrapPS)  
{  
    // TODO: perform math to calculate a circular wrap
  
    // Find the input scene position.  
    float2 inputScenePosition = float2( TODO: add math parameters );  
  
    return D2DSampleInputAtPosition(0, inputScenePosition);  
}
```

## <a name="requirements"></a><span data-ttu-id="59fd5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59fd5-118">Requirements</span></span>



| <span data-ttu-id="59fd5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59fd5-119">Requirement</span></span> | <span data-ttu-id="59fd5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fd5-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59fd5-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="59fd5-121">Header</span></span><br/> | <dl> <span data-ttu-id="59fd5-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="59fd5-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="59fd5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="59fd5-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="59fd5-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59fd5-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="59fd5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59fd5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59fd5-126">Liaison de nuanceurs d’effet</span><span class="sxs-lookup"><span data-stu-id="59fd5-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="59fd5-127">Applications auxiliaires HLSL</span><span class="sxs-lookup"><span data-stu-id="59fd5-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





