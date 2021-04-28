---
description: D3DXQuaternionNormalize, fonction (D3dx9math. h)-calcule un Quaternion de longueur unitaire.
ms.assetid: 31f56c2b-96b0-4110-a5b9-ce09983779b6
title: D3DXQuaternionNormalize, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5d4a7938b96d3d8693fd2091fcbd4f664f465c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094037"
---
# <a name="d3dxquaternionnormalize-function-d3dx9mathh"></a><span data-ttu-id="430ba-103">D3DXQuaternionNormalize, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="430ba-103">D3DXQuaternionNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="430ba-104">Calcule un Quaternion de longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="430ba-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="430ba-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="430ba-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="430ba-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="430ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="430ba-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="430ba-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="430ba-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="430ba-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="430ba-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="430ba-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="430ba-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="430ba-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="430ba-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="430ba-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="430ba-112">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="430ba-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="430ba-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="430ba-113">Return value</span></span>

<span data-ttu-id="430ba-114">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="430ba-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="430ba-115">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est la normale du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="430ba-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="430ba-116">Notes </span><span class="sxs-lookup"><span data-stu-id="430ba-116">Remarks</span></span>

<span data-ttu-id="430ba-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="430ba-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="430ba-118">De cette façon, la fonction **D3DXQuaternionNormalize** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="430ba-118">In this way, the **D3DXQuaternionNormalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="430ba-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="430ba-119">Requirements</span></span>



| <span data-ttu-id="430ba-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="430ba-120">Requirement</span></span> | <span data-ttu-id="430ba-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="430ba-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="430ba-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="430ba-122">Header</span></span><br/>  | <dl> <span data-ttu-id="430ba-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="430ba-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="430ba-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="430ba-124">Library</span></span><br/> | <dl> <span data-ttu-id="430ba-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="430ba-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="430ba-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="430ba-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="430ba-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="430ba-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="430ba-128">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="430ba-128">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




