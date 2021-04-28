---
description: D3DXVec3UnprojectArray, fonction (D3dx9math. h)-projette un tableau (x, y, z, 0) de l’espace à l’écran dans l’espace de l’objet.
ms.assetid: fef2a76c-c2fe-48c5-a1bb-6669bcc76b9b
title: D3DXVec3UnprojectArray, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 67e42b30a8f8d44bb9b21668a515a202436b7631
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097717"
---
# <a name="d3dxvec3unprojectarray-function-d3dx9mathh"></a><span data-ttu-id="e4233-103">D3DXVec3UnprojectArray, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e4233-103">D3DXVec3UnprojectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="e4233-104">Projette un tableau (x, y, z, 0) de l’espace à l’écran dans l’espace de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e4233-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4233-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4233-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a><span data-ttu-id="e4233-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4233-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4233-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e4233-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4233-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4233-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e4233-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e4233-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e4233-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4233-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4233-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4233-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4233-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="e4233-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="e4233-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4233-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4233-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4233-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e4233-115">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="e4233-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e4233-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4233-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4233-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4233-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4233-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e4233-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="e4233-119">*pViewport* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4233-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4233-120">Type : **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4233-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="e4233-121">Pointeur vers une structure [**D3DVIEWPORT9**](d3dviewport9.md) , représentant la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e4233-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="e4233-122">*pProjection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4233-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4233-123">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4233-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e4233-124">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) représentant la matrice de projection.</span><span class="sxs-lookup"><span data-stu-id="e4233-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e4233-125">*pview* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4233-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4233-126">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4233-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e4233-127">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) , représentant la matrice de vue.</span><span class="sxs-lookup"><span data-stu-id="e4233-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e4233-128">*pWorld* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4233-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4233-129">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4233-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e4233-130">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) représentant la matrice universelle.</span><span class="sxs-lookup"><span data-stu-id="e4233-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e4233-131">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4233-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4233-132">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4233-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4233-133">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="e4233-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4233-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e4233-134">Return value</span></span>

<span data-ttu-id="e4233-135">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4233-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e4233-136">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le tableau projeté de l’espace à l’écran jusqu’à l’espace de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e4233-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4233-137">Notes </span><span class="sxs-lookup"><span data-stu-id="e4233-137">Remarks</span></span>

<span data-ttu-id="e4233-138">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="e4233-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e4233-139">De cette façon, la fonction [**D3DXVec3Unproject**](d3dxvec3unproject.md) peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="e4233-139">In this way, the [**D3DXVec3Unproject**](d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4233-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4233-140">Requirements</span></span>



| <span data-ttu-id="e4233-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4233-141">Requirement</span></span> | <span data-ttu-id="e4233-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4233-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4233-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4233-143">Header</span></span><br/>  | <dl> <span data-ttu-id="e4233-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4233-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e4233-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e4233-145">Library</span></span><br/> | <dl> <span data-ttu-id="e4233-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4233-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4233-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4233-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4233-148">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="e4233-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e4233-149">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="e4233-149">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 
