---
description: Conjugue et renormalise un Quaternion.
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
ms.openlocfilehash: b2f830b7f8f797e4ed94eb22b4c2a05c3bd3e4cd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394216"
---
# <a name="d3dxquaternioninverse-function-d3dx9mathh"></a><span data-ttu-id="410d8-103">D3DXQuaternionInverse, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="410d8-103">D3DXQuaternionInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="410d8-104">Conjugue et renormalise un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="410d8-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="410d8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="410d8-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="410d8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="410d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="410d8-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="410d8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="410d8-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="410d8-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="410d8-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="410d8-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="410d8-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="410d8-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="410d8-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="410d8-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="410d8-112">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="410d8-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="410d8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="410d8-113">Return value</span></span>

<span data-ttu-id="410d8-114">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="410d8-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="410d8-115">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le Quaternion inverse du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="410d8-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="410d8-116">Notes</span><span class="sxs-lookup"><span data-stu-id="410d8-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="410d8-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="410d8-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="410d8-118">De cette façon, la fonction **D3DXQuaternionInverse** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="410d8-118">In this way, the **D3DXQuaternionInverse** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="410d8-119">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="410d8-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="410d8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="410d8-120">Requirements</span></span>



| <span data-ttu-id="410d8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="410d8-121">Requirement</span></span> | <span data-ttu-id="410d8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="410d8-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="410d8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="410d8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="410d8-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="410d8-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="410d8-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="410d8-125">Library</span></span><br/> | <dl> <span data-ttu-id="410d8-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="410d8-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="410d8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="410d8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="410d8-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="410d8-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="410d8-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="410d8-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
</dt> <dt>

[<span data-ttu-id="410d8-130">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="410d8-130">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
</dt> </dl>

 

 




