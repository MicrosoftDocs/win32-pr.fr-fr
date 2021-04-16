---
description: Interpole entre les quaternions, à l’aide de l’interpolation sphérique Quadrangle.
ms.assetid: ba953731-4372-4b32-942b-23abfe479704
title: D3DXQuaternionSquad, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: af2bb582909cf09a4044b293f3f298a5da2335a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530999"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a><span data-ttu-id="fc0ad-103">D3DXQuaternionSquad, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="fc0ad-103">D3DXQuaternionSquad function (D3DX10Math.h)</span></span>

<span data-ttu-id="fc0ad-104">Interpole entre les quaternions, à l’aide de l’interpolation sphérique Quadrangle.</span><span class="sxs-lookup"><span data-stu-id="fc0ad-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc0ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc0ad-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="fc0ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc0ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc0ad-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fc0ad-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc0ad-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc0ad-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fc0ad-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="fc0ad-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fc0ad-110">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc0ad-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc0ad-111">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="fc0ad-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fc0ad-112">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="fc0ad-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="fc0ad-113">*PA* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc0ad-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc0ad-114">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="fc0ad-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fc0ad-115">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="fc0ad-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="fc0ad-116">*PB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc0ad-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc0ad-117">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="fc0ad-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fc0ad-118">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="fc0ad-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="fc0ad-119">*ordinateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc0ad-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc0ad-120">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="fc0ad-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fc0ad-121">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="fc0ad-121">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="fc0ad-122">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc0ad-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc0ad-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc0ad-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc0ad-124">Paramètre qui indique la distance à interpoler entre les quaternions.</span><span class="sxs-lookup"><span data-stu-id="fc0ad-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc0ad-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc0ad-125">Return value</span></span>

<span data-ttu-id="fc0ad-126">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc0ad-126">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fc0ad-127">Pointeur vers une structure D3DXQUATERNION qui est le résultat de l’interpolation sphérique Quadrangle.</span><span class="sxs-lookup"><span data-stu-id="fc0ad-127">Pointer to a D3DXQUATERNION structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc0ad-128">Notes</span><span class="sxs-lookup"><span data-stu-id="fc0ad-128">Remarks</span></span>

<span data-ttu-id="fc0ad-129">Cette fonction utilise la séquence suivante d’opérations d’interpolation linéaire sphérique :</span><span class="sxs-lookup"><span data-stu-id="fc0ad-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="fc0ad-130">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="fc0ad-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="fc0ad-131">De cette façon, la fonction D3DXQuaternionSquad peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="fc0ad-131">In this way, the D3DXQuaternionSquad function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fc0ad-132">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="fc0ad-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc0ad-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc0ad-133">Requirements</span></span>



| <span data-ttu-id="fc0ad-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc0ad-134">Requirement</span></span> | <span data-ttu-id="fc0ad-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc0ad-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc0ad-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc0ad-136">Header</span></span><br/>  | <dl> <span data-ttu-id="fc0ad-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc0ad-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="fc0ad-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fc0ad-138">Library</span></span><br/> | <dl> <span data-ttu-id="fc0ad-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc0ad-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fc0ad-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc0ad-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc0ad-141">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="fc0ad-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
