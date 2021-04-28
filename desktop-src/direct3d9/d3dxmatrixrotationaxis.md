---
description: 'D3DXMatrixRotationAxis, fonction (D3dx9math. h) : crée une matrice qui pivote autour d’un axe arbitraire.'
ms.assetid: 368c8f64-7709-4200-94d3-3dbc92a960c1
title: D3DXMatrixRotationAxis, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 720ac4d3bdae2910cee7913b9c34316d72526688
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118187"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="d2f66-103">D3DXMatrixRotationAxis, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d2f66-103">D3DXMatrixRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="d2f66-104">Crée une matrice qui pivote autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="d2f66-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f66-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2f66-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="d2f66-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2f66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2f66-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d2f66-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f66-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2f66-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d2f66-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d2f66-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d2f66-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2f66-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f66-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d2f66-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d2f66-112">Pointeur vers l’axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="d2f66-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="d2f66-113">Consultez [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="d2f66-113">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2f66-114">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2f66-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f66-115">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2f66-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2f66-116">Angle de rotation en radians.</span><span class="sxs-lookup"><span data-stu-id="d2f66-116">Angle of rotation in radians.</span></span> <span data-ttu-id="d2f66-117">Les angles sont mesurés dans le sens des aiguilles d’une montre sur l’axe de rotation vers l’origine.</span><span class="sxs-lookup"><span data-stu-id="d2f66-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2f66-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d2f66-118">Return value</span></span>

<span data-ttu-id="d2f66-119">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2f66-119">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d2f66-120">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) pivotée autour de l’axe spécifié.</span><span class="sxs-lookup"><span data-stu-id="d2f66-120">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2f66-121">Notes </span><span class="sxs-lookup"><span data-stu-id="d2f66-121">Remarks</span></span>

<span data-ttu-id="d2f66-122">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="d2f66-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d2f66-123">De cette façon, la fonction **D3DXMatrixRotationAxis** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="d2f66-123">In this way, the **D3DXMatrixRotationAxis** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f66-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2f66-124">Requirements</span></span>



| <span data-ttu-id="d2f66-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2f66-125">Requirement</span></span> | <span data-ttu-id="d2f66-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2f66-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f66-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2f66-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d2f66-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2f66-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d2f66-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d2f66-129">Library</span></span><br/> | <dl> <span data-ttu-id="d2f66-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2f66-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2f66-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2f66-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f66-132">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="d2f66-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d2f66-133">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="d2f66-133">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="d2f66-134">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="d2f66-134">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="d2f66-135">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="d2f66-135">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="d2f66-136">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="d2f66-136">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="d2f66-137">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="d2f66-137">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
