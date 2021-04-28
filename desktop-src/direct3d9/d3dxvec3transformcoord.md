---
description: D3DXVec3TransformCoord, fonction (D3dx9math. h)-transforme un vecteur 3D en une matrice donnée, en reprojetant le résultat dans w = 1.
ms.assetid: 4075b067-1e64-46c9-be73-5fa765c9cb9d
title: D3DXVec3TransformCoord, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4e3514d4717262a7afab7ae808d747de3a1b635
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115627"
---
# <a name="d3dxvec3transformcoord-function-d3dx9mathh"></a><span data-ttu-id="d0873-103">D3DXVec3TransformCoord, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d0873-103">D3DXVec3TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="d0873-104">Transforme un vecteur 3D par une matrice donnée, en reprojetant le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="d0873-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0873-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0873-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d0873-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0873-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0873-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d0873-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0873-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0873-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d0873-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d0873-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d0873-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d0873-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0873-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d0873-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d0873-112">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="d0873-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d0873-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d0873-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0873-114">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d0873-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d0873-115">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="d0873-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0873-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d0873-116">Return value</span></span>

<span data-ttu-id="d0873-117">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0873-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d0873-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le vecteur transformé.</span><span class="sxs-lookup"><span data-stu-id="d0873-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0873-119">Notes </span><span class="sxs-lookup"><span data-stu-id="d0873-119">Remarks</span></span>

<span data-ttu-id="d0873-120">Cette fonction transforme le vecteur, *PV* (x, y, z, 1), par la matrice, *PM*, en projetant le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="d0873-120">This function transforms the vector, *pV* (x, y, z, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="d0873-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="d0873-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d0873-122">De cette façon, la fonction **D3DXVec3TransformCoord** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="d0873-122">In this way, the **D3DXVec3TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0873-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0873-123">Requirements</span></span>



| <span data-ttu-id="d0873-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0873-124">Requirement</span></span> | <span data-ttu-id="d0873-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0873-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0873-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0873-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d0873-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0873-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d0873-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d0873-128">Library</span></span><br/> | <dl> <span data-ttu-id="d0873-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0873-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d0873-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0873-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0873-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="d0873-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d0873-132">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="d0873-132">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
</dt> <dt>

[<span data-ttu-id="d0873-133">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="d0873-133">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
</dt> </dl>

 

 




