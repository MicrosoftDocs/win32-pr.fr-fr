---
description: Projette un vecteur de l’espace à l’écran dans l’espace de l’objet.
ms.assetid: c96d732d-0594-42b4-bc54-458a313f153e
title: D3DXVec3Unproject, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 21916392c689bcac794d44ec2c42c3e0b39abb0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522762"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a><span data-ttu-id="28e15-103">D3DXVec3Unproject, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="28e15-103">D3DXVec3Unproject function (D3DX10Math.h)</span></span>

<span data-ttu-id="28e15-104">Projette un vecteur de l’espace à l’écran dans l’espace de l’objet.</span><span class="sxs-lookup"><span data-stu-id="28e15-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e15-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28e15-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="28e15-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28e15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28e15-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="28e15-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28e15-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="28e15-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="28e15-109">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="28e15-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="28e15-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28e15-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e15-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="28e15-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="28e15-112">Pointeur vers la structure D3DXVECTOR3 source.</span><span class="sxs-lookup"><span data-stu-id="28e15-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="28e15-113">*pViewport* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28e15-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e15-114">Type : **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="28e15-114">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="28e15-115">Pointeur vers une [**\_ fenêtre d’affichage D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)représentant la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="28e15-115">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="28e15-116">*pProjection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28e15-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e15-117">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="28e15-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="28e15-118">Pointeur vers une structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) représentant la matrice de projection.</span><span class="sxs-lookup"><span data-stu-id="28e15-118">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="28e15-119">*pview* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28e15-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e15-120">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="28e15-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="28e15-121">Pointeur vers une structure D3DXMATRIX, représentant la matrice de vue.</span><span class="sxs-lookup"><span data-stu-id="28e15-121">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="28e15-122">*pWorld* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28e15-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e15-123">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="28e15-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="28e15-124">Pointeur vers une structure D3DXMATRIX représentant la matrice universelle.</span><span class="sxs-lookup"><span data-stu-id="28e15-124">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28e15-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28e15-125">Return value</span></span>

<span data-ttu-id="28e15-126">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="28e15-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="28e15-127">Pointeur vers une structure D3DXVECTOR3 qui est le vecteur projeté de l’espace à l’écran jusqu’à l’espace de l’objet.</span><span class="sxs-lookup"><span data-stu-id="28e15-127">Pointer to a D3DXVECTOR3 structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="28e15-128">Notes</span><span class="sxs-lookup"><span data-stu-id="28e15-128">Remarks</span></span>

<span data-ttu-id="28e15-129">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="28e15-129">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="28e15-130">De cette façon, la fonction D3DXVec3Unproject peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="28e15-130">In this way, the D3DXVec3Unproject function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e15-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28e15-131">Requirements</span></span>



| <span data-ttu-id="28e15-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28e15-132">Requirement</span></span> | <span data-ttu-id="28e15-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="28e15-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28e15-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="28e15-134">Header</span></span><br/> | <dl> <span data-ttu-id="28e15-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="28e15-135"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28e15-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28e15-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e15-137">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="28e15-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
