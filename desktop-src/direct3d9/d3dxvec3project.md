---
description: Projette un vecteur 3D à partir de l’espace d’objet dans l’espace à l’écran.
ms.assetid: b012771d-052f-4bf9-b39c-387d8a63fa59
title: D3DXVec3Project, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c8198987b970fd6d79db3c73f715df4f0ac6981
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322857"
---
# <a name="d3dxvec3project-function-d3dx9mathh"></a><span data-ttu-id="e7f8f-103">D3DXVec3Project, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e7f8f-103">D3DXVec3Project function (D3dx9math.h)</span></span>

<span data-ttu-id="e7f8f-104">Projette un vecteur 3D à partir de l’espace d’objet dans l’espace à l’écran.</span><span class="sxs-lookup"><span data-stu-id="e7f8f-104">Projects a 3D vector from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7f8f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7f8f-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="e7f8f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7f8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7f8f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e7f8f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f8f-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7f8f-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e7f8f-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e7f8f-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e7f8f-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f8f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f8f-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e7f8f-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e7f8f-112">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="e7f8f-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e7f8f-113">*pViewport* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f8f-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f8f-114">Type : **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="e7f8f-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="e7f8f-115">Pointeur vers une structure [**D3DVIEWPORT9**](d3dviewport9.md) , représentant la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e7f8f-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="e7f8f-116">*pProjection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f8f-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f8f-117">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e7f8f-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e7f8f-118">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) représentant la matrice de projection.</span><span class="sxs-lookup"><span data-stu-id="e7f8f-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e7f8f-119">*pview* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f8f-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f8f-120">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e7f8f-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e7f8f-121">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) , représentant la matrice de vue.</span><span class="sxs-lookup"><span data-stu-id="e7f8f-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e7f8f-122">*pWorld* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f8f-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f8f-123">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e7f8f-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e7f8f-124">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) représentant la matrice universelle.</span><span class="sxs-lookup"><span data-stu-id="e7f8f-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7f8f-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7f8f-125">Return value</span></span>

<span data-ttu-id="e7f8f-126">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7f8f-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e7f8f-127">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le vecteur projeté de l’espace de l’objet à l’espace à l’écran.</span><span class="sxs-lookup"><span data-stu-id="e7f8f-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7f8f-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e7f8f-128">Remarks</span></span>

<span data-ttu-id="e7f8f-129">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="e7f8f-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e7f8f-130">De cette façon, la fonction **D3DXVec3Project** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="e7f8f-130">In this way, the **D3DXVec3Project** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7f8f-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7f8f-131">Requirements</span></span>



| <span data-ttu-id="e7f8f-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7f8f-132">Requirement</span></span> | <span data-ttu-id="e7f8f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7f8f-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f8f-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7f8f-134">Header</span></span><br/>  | <dl> <span data-ttu-id="e7f8f-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7f8f-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e7f8f-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7f8f-136">Library</span></span><br/> | <dl> <span data-ttu-id="e7f8f-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7f8f-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7f8f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7f8f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7f8f-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="e7f8f-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e7f8f-140">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="e7f8f-140">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 




