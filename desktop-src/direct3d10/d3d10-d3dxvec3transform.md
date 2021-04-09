---
description: Transforme le vecteur (x, y, z, 1) par une matrice donnée.
ms.assetid: 88b26d94-2550-4126-bf91-b06391ec5c75
title: D3DXVec3Transform, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 6db2e2ad4279863ba68f709f02f86796552e0463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953939"
---
# <a name="d3dxvec3transform-function-d3dx10mathh"></a><span data-ttu-id="71d84-103">D3DXVec3Transform, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="71d84-103">D3DXVec3Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="71d84-104">Transforme le vecteur (x, y, z, 1) par une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="71d84-104">Transforms vector (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d84-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71d84-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="71d84-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71d84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71d84-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="71d84-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="71d84-108">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="71d84-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="71d84-109">Pointeur vers la structure [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="71d84-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="71d84-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71d84-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71d84-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="71d84-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="71d84-112">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md)source.</span><span class="sxs-lookup"><span data-stu-id="71d84-112">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="71d84-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71d84-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71d84-114">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="71d84-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="71d84-115">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="71d84-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71d84-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71d84-116">Return value</span></span>

<span data-ttu-id="71d84-117">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="71d84-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="71d84-118">Pointeur vers une structure D3DXVECTOR4 qui est le vecteur transformé.</span><span class="sxs-lookup"><span data-stu-id="71d84-118">Pointer to a D3DXVECTOR4 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="71d84-119">Notes</span><span class="sxs-lookup"><span data-stu-id="71d84-119">Remarks</span></span>

<span data-ttu-id="71d84-120">Cette fonction transforme le vecteur, pV (x, y, z, 1), par la matrice pM.</span><span class="sxs-lookup"><span data-stu-id="71d84-120">This function transforms the vector, pV (x, y, z, 1), by the matrix pM.</span></span>

<span data-ttu-id="71d84-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="71d84-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="71d84-122">De cette façon, la fonction D3DXVec3Transform peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="71d84-122">In this way, the D3DXVec3Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="71d84-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71d84-123">Requirements</span></span>



| <span data-ttu-id="71d84-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71d84-124">Requirement</span></span> | <span data-ttu-id="71d84-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="71d84-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71d84-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="71d84-126">Header</span></span><br/> | <dl> <span data-ttu-id="71d84-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="71d84-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71d84-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71d84-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d84-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="71d84-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
