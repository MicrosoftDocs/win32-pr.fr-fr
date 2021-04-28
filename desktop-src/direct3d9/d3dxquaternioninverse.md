---
description: 'D3DXQuaternionInverse, fonction (D3dx9math. h) : conjugue et renormalise un Quaternion.'
ms.assetid: 25407a60-f7c0-4063-8d1d-2d6d03bdb217
title: D3DXQuaternionInverse, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ebb2520efa3c7c78d98fd8b90ec1ba9615e9927
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094067"
---
# <a name="d3dxquaternioninverse-function-d3dx9mathh"></a><span data-ttu-id="f2fc9-103">D3DXQuaternionInverse, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f2fc9-103">D3DXQuaternionInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="f2fc9-104">Conjugue et renormalise un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="f2fc9-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2fc9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2fc9-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="f2fc9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2fc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2fc9-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f2fc9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fc9-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2fc9-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f2fc9-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f2fc9-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f2fc9-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2fc9-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fc9-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2fc9-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f2fc9-112">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="f2fc9-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2fc9-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f2fc9-113">Return value</span></span>

<span data-ttu-id="f2fc9-114">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2fc9-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f2fc9-115">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le Quaternion inverse du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="f2fc9-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2fc9-116">Notes </span><span class="sxs-lookup"><span data-stu-id="f2fc9-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="f2fc9-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="f2fc9-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f2fc9-118">De cette façon, la fonction **D3DXQuaternionInverse** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="f2fc9-118">In this way, the **D3DXQuaternionInverse** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f2fc9-119">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="f2fc9-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2fc9-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2fc9-120">Requirements</span></span>



| <span data-ttu-id="f2fc9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2fc9-121">Requirement</span></span> | <span data-ttu-id="f2fc9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2fc9-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2fc9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2fc9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f2fc9-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2fc9-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f2fc9-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f2fc9-125">Library</span></span><br/> | <dl> <span data-ttu-id="f2fc9-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2fc9-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2fc9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2fc9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2fc9-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="f2fc9-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f2fc9-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="f2fc9-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
</dt> <dt>

[<span data-ttu-id="f2fc9-130">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="f2fc9-130">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
</dt> </dl>

 

 




