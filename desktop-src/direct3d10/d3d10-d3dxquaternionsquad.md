---
description: 'Fonction D3DXQuaternionSquad (D3DX10Math. h) : interpole entre les quaternions, à l’aide de l’interpolation Quadrangle sphérique.'
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
ms.openlocfilehash: 9671b2a161124228c264da7eac0a2aa3a915ff95
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108757"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a><span data-ttu-id="84092-103">D3DXQuaternionSquad, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="84092-103">D3DXQuaternionSquad function (D3DX10Math.h)</span></span>

<span data-ttu-id="84092-104">Interpole entre les quaternions, à l’aide de l’interpolation sphérique Quadrangle.</span><span class="sxs-lookup"><span data-stu-id="84092-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="84092-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84092-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="84092-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84092-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84092-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="84092-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84092-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="84092-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="84092-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="84092-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="84092-110">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84092-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84092-111">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="84092-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="84092-112">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="84092-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="84092-113">*PA* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84092-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84092-114">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="84092-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="84092-115">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="84092-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="84092-116">*PB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84092-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84092-117">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="84092-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="84092-118">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="84092-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="84092-119">*ordinateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84092-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84092-120">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="84092-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="84092-121">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="84092-121">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="84092-122">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84092-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84092-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84092-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84092-124">Paramètre qui indique la distance à interpoler entre les quaternions.</span><span class="sxs-lookup"><span data-stu-id="84092-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84092-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="84092-125">Return value</span></span>

<span data-ttu-id="84092-126">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="84092-126">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="84092-127">Pointeur vers une structure D3DXQUATERNION qui est le résultat de l’interpolation sphérique Quadrangle.</span><span class="sxs-lookup"><span data-stu-id="84092-127">Pointer to a D3DXQUATERNION structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="84092-128">Notes </span><span class="sxs-lookup"><span data-stu-id="84092-128">Remarks</span></span>

<span data-ttu-id="84092-129">Cette fonction utilise la séquence suivante d’opérations d’interpolation linéaire sphérique :</span><span class="sxs-lookup"><span data-stu-id="84092-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="84092-130">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="84092-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="84092-131">De cette façon, la fonction D3DXQuaternionSquad peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="84092-131">In this way, the D3DXQuaternionSquad function can be used as a parameter for another function.</span></span>

<span data-ttu-id="84092-132">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="84092-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="84092-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84092-133">Requirements</span></span>



| <span data-ttu-id="84092-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84092-134">Requirement</span></span> | <span data-ttu-id="84092-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="84092-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84092-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="84092-136">Header</span></span><br/>  | <dl> <span data-ttu-id="84092-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="84092-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="84092-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="84092-138">Library</span></span><br/> | <dl> <span data-ttu-id="84092-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84092-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="84092-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84092-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84092-141">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="84092-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
