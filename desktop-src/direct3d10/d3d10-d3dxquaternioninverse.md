---
description: 'D3DXQuaternionInverse, fonction (D3DX10Math. h) : conjugue et renormalise un Quaternion.'
ms.assetid: 8e1bba91-8895-43a2-805b-1368050f8e82
title: D3DXQuaternionInverse, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionInverse
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 84816ac72841dcda0aef726535b7f5219d5467e4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103197"
---
# <a name="d3dxquaternioninverse-function-d3dx10mathh"></a><span data-ttu-id="b5787-103">D3DXQuaternionInverse, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b5787-103">D3DXQuaternionInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="b5787-104">Conjugue et renormalise un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="b5787-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5787-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5787-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="b5787-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5787-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5787-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b5787-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5787-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5787-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b5787-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b5787-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b5787-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5787-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5787-111">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5787-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b5787-112">Pointeur vers la structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="b5787-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5787-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b5787-113">Return value</span></span>

<span data-ttu-id="b5787-114">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5787-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b5787-115">Pointeur vers une structure D3DXQUATERNION qui est le Quaternion inverse du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="b5787-115">Pointer to a D3DXQUATERNION structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5787-116">Notes </span><span class="sxs-lookup"><span data-stu-id="b5787-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="b5787-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="b5787-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b5787-118">De cette façon, la fonction D3DXQuaternionInverse peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="b5787-118">In this way, the D3DXQuaternionInverse function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b5787-119">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="b5787-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5787-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5787-120">Requirements</span></span>



| <span data-ttu-id="b5787-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5787-121">Requirement</span></span> | <span data-ttu-id="b5787-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5787-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5787-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5787-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b5787-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5787-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b5787-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5787-125">Library</span></span><br/> | <dl> <span data-ttu-id="b5787-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5787-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5787-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5787-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5787-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="b5787-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
