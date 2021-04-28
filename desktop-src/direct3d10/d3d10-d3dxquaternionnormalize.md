---
description: D3DXQuaternionNormalize, fonction (D3DX10Math. h)-calcule un Quaternion de longueur unitaire.
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
ms.openlocfilehash: 6d031dfc63cb92d43a9cca27813c9425e2ff1acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103137"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a><span data-ttu-id="41653-103">D3DXQuaternionNormalize, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="41653-103">D3DXQuaternionNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="41653-104">Calcule un Quaternion de longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="41653-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="41653-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41653-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="41653-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41653-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41653-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="41653-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="41653-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="41653-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="41653-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="41653-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="41653-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41653-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41653-111">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="41653-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="41653-112">Pointeur vers la structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="41653-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41653-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="41653-113">Return value</span></span>

<span data-ttu-id="41653-114">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="41653-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="41653-115">Pointeur vers une structure D3DXQUATERNION qui est la normale du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="41653-115">Pointer to a D3DXQUATERNION structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="41653-116">Notes </span><span class="sxs-lookup"><span data-stu-id="41653-116">Remarks</span></span>

<span data-ttu-id="41653-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="41653-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="41653-118">De cette façon, la fonction D3DXQuaternionNormalize peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="41653-118">In this way, the D3DXQuaternionNormalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="41653-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41653-119">Requirements</span></span>



| <span data-ttu-id="41653-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41653-120">Requirement</span></span> | <span data-ttu-id="41653-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="41653-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41653-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="41653-122">Header</span></span><br/>  | <dl> <span data-ttu-id="41653-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="41653-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="41653-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="41653-124">Library</span></span><br/> | <dl> <span data-ttu-id="41653-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41653-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41653-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41653-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41653-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="41653-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
