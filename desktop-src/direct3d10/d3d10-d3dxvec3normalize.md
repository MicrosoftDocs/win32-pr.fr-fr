---
description: Retourne la version normalisée d’un vecteur 3D.
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
ms.openlocfilehash: 413b807c53e0b46b115af2aa283e4902a45f5979
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870165"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a><span data-ttu-id="01338-103">D3DXVec3Normalize, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="01338-103">D3DXVec3Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="01338-104">Retourne la version normalisée d’un vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="01338-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="01338-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01338-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="01338-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01338-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01338-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="01338-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="01338-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="01338-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="01338-109">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="01338-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="01338-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01338-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01338-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="01338-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="01338-112">Pointeur vers la structure D3DXVECTOR3 source.</span><span class="sxs-lookup"><span data-stu-id="01338-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01338-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01338-113">Return value</span></span>

<span data-ttu-id="01338-114">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="01338-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="01338-115">Pointeur vers une structure D3DXVECTOR3 qui est la version normalisée du vecteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="01338-115">Pointer to a D3DXVECTOR3 structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="01338-116">Notes</span><span class="sxs-lookup"><span data-stu-id="01338-116">Remarks</span></span>

<span data-ttu-id="01338-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="01338-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="01338-118">De cette façon, la fonction D3DXVec3Normalize peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="01338-118">In this way, the D3DXVec3Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="01338-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01338-119">Requirements</span></span>



| <span data-ttu-id="01338-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01338-120">Requirement</span></span> | <span data-ttu-id="01338-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="01338-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01338-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="01338-122">Header</span></span><br/> | <dl> <span data-ttu-id="01338-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="01338-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01338-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01338-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01338-125">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="01338-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
