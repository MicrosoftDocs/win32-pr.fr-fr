---
description: Retourne la version normalisée d’un vecteur 4D.
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: D3DXVec4Normalize, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ebedbdddbe558bfad71520b64aa0cf2ff4c2f451
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323094"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a><span data-ttu-id="a383c-103">D3DXVec4Normalize, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a383c-103">D3DXVec4Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="a383c-104">Retourne la version normalisée d’un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="a383c-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a383c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a383c-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="a383c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a383c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a383c-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a383c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a383c-108">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a383c-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a383c-109">Pointeur vers le [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a383c-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a383c-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a383c-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a383c-111">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a383c-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a383c-112">Pointeur vers la structure D3DXVECTOR4 source.</span><span class="sxs-lookup"><span data-stu-id="a383c-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a383c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a383c-113">Return value</span></span>

<span data-ttu-id="a383c-114">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a383c-114">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a383c-115">Pointeur vers une structure D3DXVECTOR4 qui est la version normalisée du vecteur.</span><span class="sxs-lookup"><span data-stu-id="a383c-115">Pointer to a D3DXVECTOR4 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="a383c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a383c-116">Remarks</span></span>

<span data-ttu-id="a383c-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="a383c-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a383c-118">De cette façon, la fonction D3DXVec4Normalize peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="a383c-118">In this way, the D3DXVec4Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a383c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a383c-119">Requirements</span></span>



| <span data-ttu-id="a383c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a383c-120">Requirement</span></span> | <span data-ttu-id="a383c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a383c-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a383c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a383c-122">Header</span></span><br/> | <dl> <span data-ttu-id="a383c-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a383c-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a383c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a383c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a383c-125">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="a383c-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
