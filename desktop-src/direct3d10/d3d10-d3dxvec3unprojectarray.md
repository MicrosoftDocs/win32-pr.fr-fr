---
description: D3DXVec3UnprojectArray, fonction (D3DX10Math. h)-projette un tableau (x, y, z, 0) de l’espace à l’écran dans l’espace de l’objet.
ms.assetid: 02db5b32-7fa3-4cde-bd63-0d8b3dfc31e7
title: D3DXVec3UnprojectArray, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 727744445e952fa0135feff944c768aaba1aba36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103007"
---
# <a name="d3dxvec3unprojectarray-function-d3dx10mathh"></a><span data-ttu-id="cea1e-103">D3DXVec3UnprojectArray, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="cea1e-103">D3DXVec3UnprojectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="cea1e-104">Projette un tableau (x, y, z, 0) de l’espace à l’écran dans l’espace de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cea1e-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="cea1e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cea1e-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_          UINT           OutStride,
  _In_    const D3DXVECTOR3    *pV,
  _In_          UINT           VStride,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld,
  _In_          UINT           n
);
```



## <a name="parameters"></a><span data-ttu-id="cea1e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cea1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea1e-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cea1e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cea1e-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="cea1e-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cea1e-109">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="cea1e-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cea1e-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea1e-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea1e-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea1e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea1e-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="cea1e-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="cea1e-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea1e-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea1e-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cea1e-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cea1e-115">Pointeur vers la structure D3DXVECTOR3 source.</span><span class="sxs-lookup"><span data-stu-id="cea1e-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="cea1e-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea1e-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea1e-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea1e-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea1e-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cea1e-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="cea1e-119">*pViewport* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea1e-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea1e-120">Type : **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="cea1e-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="cea1e-121">Pointeur vers une [**\_ fenêtre d’affichage D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)représentant la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="cea1e-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="cea1e-122">*pProjection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea1e-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea1e-123">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cea1e-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cea1e-124">Pointeur vers une structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) représentant la matrice de projection.</span><span class="sxs-lookup"><span data-stu-id="cea1e-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="cea1e-125">*pview* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea1e-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea1e-126">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cea1e-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cea1e-127">Pointeur vers une structure D3DXMATRIX, représentant la matrice de vue.</span><span class="sxs-lookup"><span data-stu-id="cea1e-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="cea1e-128">*pWorld* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea1e-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea1e-129">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cea1e-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cea1e-130">Pointeur vers une structure D3DXMATRIX représentant la matrice universelle.</span><span class="sxs-lookup"><span data-stu-id="cea1e-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="cea1e-131">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea1e-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea1e-132">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea1e-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea1e-133">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="cea1e-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cea1e-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cea1e-134">Return value</span></span>

<span data-ttu-id="cea1e-135">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="cea1e-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cea1e-136">Pointeur vers une structure D3DXVECTOR3 qui est le tableau projeté de l’espace à l’écran jusqu’à l’espace de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cea1e-136">Pointer to a D3DXVECTOR3 structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="cea1e-137">Notes </span><span class="sxs-lookup"><span data-stu-id="cea1e-137">Remarks</span></span>

<span data-ttu-id="cea1e-138">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="cea1e-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="cea1e-139">De cette façon, la fonction [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="cea1e-139">In this way, the [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea1e-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cea1e-140">Requirements</span></span>



| <span data-ttu-id="cea1e-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cea1e-141">Requirement</span></span> | <span data-ttu-id="cea1e-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="cea1e-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cea1e-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="cea1e-143">Header</span></span><br/> | <dl> <span data-ttu-id="cea1e-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cea1e-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cea1e-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cea1e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea1e-146">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="cea1e-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
