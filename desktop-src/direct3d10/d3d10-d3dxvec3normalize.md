---
description: 'D3DXVec3Normalize, fonction (D3DX10Math. h) : retourne la version normalisée d’un vecteur 3D.'
ms.assetid: 420321a2-0c3b-419c-9620-acf184e7b4f0
title: D3DXVec3Normalize, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 3f1317b1b8887b9ff306fcaed2cb6da2d077010f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108177"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a><span data-ttu-id="c55a6-103">D3DXVec3Normalize, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="c55a6-103">D3DXVec3Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="c55a6-104">Retourne la version normalisée d’un vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="c55a6-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="c55a6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c55a6-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="c55a6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c55a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c55a6-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c55a6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c55a6-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c55a6-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c55a6-109">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c55a6-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c55a6-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c55a6-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c55a6-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c55a6-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c55a6-112">Pointeur vers la structure D3DXVECTOR3 source.</span><span class="sxs-lookup"><span data-stu-id="c55a6-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c55a6-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c55a6-113">Return value</span></span>

<span data-ttu-id="c55a6-114">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c55a6-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c55a6-115">Pointeur vers une structure D3DXVECTOR3 qui est la version normalisée du vecteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="c55a6-115">Pointer to a D3DXVECTOR3 structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="c55a6-116">Notes </span><span class="sxs-lookup"><span data-stu-id="c55a6-116">Remarks</span></span>

<span data-ttu-id="c55a6-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="c55a6-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c55a6-118">De cette façon, la fonction D3DXVec3Normalize peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="c55a6-118">In this way, the D3DXVec3Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c55a6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c55a6-119">Requirements</span></span>



| <span data-ttu-id="c55a6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c55a6-120">Requirement</span></span> | <span data-ttu-id="c55a6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c55a6-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c55a6-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c55a6-122">Header</span></span><br/> | <dl> <span data-ttu-id="c55a6-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c55a6-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c55a6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c55a6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c55a6-125">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="c55a6-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
