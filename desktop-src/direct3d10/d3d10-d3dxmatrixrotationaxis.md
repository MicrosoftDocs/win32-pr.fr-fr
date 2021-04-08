---
description: Crée une matrice qui pivote autour d’un axe arbitraire.
ms.assetid: dc4b8b3f-e1d2-475f-9dcb-622ada9fae6b
title: D3DXMatrixRotationAxis, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bba74aa7258b39b8fdbbb8cab09684a14bfbda91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043164"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="be4b1-103">D3DXMatrixRotationAxis, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="be4b1-103">D3DXMatrixRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="be4b1-104">Crée une matrice qui pivote autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="be4b1-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="be4b1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be4b1-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="be4b1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be4b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be4b1-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="be4b1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="be4b1-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="be4b1-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="be4b1-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="be4b1-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="be4b1-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be4b1-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be4b1-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="be4b1-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="be4b1-112">Pointeur vers l’axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="be4b1-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="be4b1-113">Consultez [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="be4b1-113">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="be4b1-114">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be4b1-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be4b1-115">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be4b1-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be4b1-116">Angle de rotation en radians.</span><span class="sxs-lookup"><span data-stu-id="be4b1-116">Angle of rotation in radians.</span></span> <span data-ttu-id="be4b1-117">Les angles sont mesurés dans le sens des aiguilles d’une montre sur l’axe de rotation vers l’origine.</span><span class="sxs-lookup"><span data-stu-id="be4b1-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be4b1-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be4b1-118">Return value</span></span>

<span data-ttu-id="be4b1-119">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="be4b1-119">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="be4b1-120">Pointeur vers une structure D3DXMATRIX pivotée autour de l’axe spécifié.</span><span class="sxs-lookup"><span data-stu-id="be4b1-120">Pointer to a D3DXMATRIX structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="be4b1-121">Notes</span><span class="sxs-lookup"><span data-stu-id="be4b1-121">Remarks</span></span>

<span data-ttu-id="be4b1-122">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="be4b1-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="be4b1-123">De cette façon, la fonction D3DXMatrixRotationAxis peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="be4b1-123">In this way, the D3DXMatrixRotationAxis function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="be4b1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be4b1-124">Requirements</span></span>



| <span data-ttu-id="be4b1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be4b1-125">Requirement</span></span> | <span data-ttu-id="be4b1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="be4b1-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be4b1-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="be4b1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="be4b1-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="be4b1-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="be4b1-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be4b1-129">Library</span></span><br/> | <dl> <span data-ttu-id="be4b1-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be4b1-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be4b1-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be4b1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be4b1-132">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="be4b1-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
