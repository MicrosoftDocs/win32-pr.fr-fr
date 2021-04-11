---
description: Calcule un Quaternion de longueur d’unité.
ms.assetid: 6735a632-64d7-4bc1-b63e-d0cd27f5a29b
title: D3DXQuaternionNormalize, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e121ef4892c65a0f04acaa89d44d4a5a9090740e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211872"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a><span data-ttu-id="64b02-103">D3DXQuaternionNormalize, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="64b02-103">D3DXQuaternionNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="64b02-104">Calcule un Quaternion de longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="64b02-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="64b02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64b02-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="64b02-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64b02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64b02-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="64b02-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="64b02-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="64b02-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="64b02-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="64b02-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="64b02-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64b02-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64b02-111">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="64b02-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="64b02-112">Pointeur vers la structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="64b02-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64b02-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64b02-113">Return value</span></span>

<span data-ttu-id="64b02-114">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="64b02-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="64b02-115">Pointeur vers une structure D3DXQUATERNION qui est la normale du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="64b02-115">Pointer to a D3DXQUATERNION structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="64b02-116">Notes</span><span class="sxs-lookup"><span data-stu-id="64b02-116">Remarks</span></span>

<span data-ttu-id="64b02-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="64b02-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="64b02-118">De cette façon, la fonction D3DXQuaternionNormalize peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="64b02-118">In this way, the D3DXQuaternionNormalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="64b02-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64b02-119">Requirements</span></span>



| <span data-ttu-id="64b02-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64b02-120">Requirement</span></span> | <span data-ttu-id="64b02-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="64b02-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64b02-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="64b02-122">Header</span></span><br/>  | <dl> <span data-ttu-id="64b02-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="64b02-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="64b02-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="64b02-124">Library</span></span><br/> | <dl> <span data-ttu-id="64b02-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64b02-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="64b02-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64b02-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64b02-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="64b02-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
