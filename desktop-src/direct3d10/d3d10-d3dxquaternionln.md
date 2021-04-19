---
description: Calcule le logarithme népérien.
ms.assetid: 576cf676-bb42-45ec-8e45-4612a7cdb167
title: D3DXQuaternionLn, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLn
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 07b081e0e2063d18ab8f2bb010e2b436c38df097
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524873"
---
# <a name="d3dxquaternionln-function-d3dx10mathh"></a><span data-ttu-id="e3506-103">D3DXQuaternionLn, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e3506-103">D3DXQuaternionLn function (D3DX10Math.h)</span></span>

<span data-ttu-id="e3506-104">Calcule le logarithme népérien.</span><span class="sxs-lookup"><span data-stu-id="e3506-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3506-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3506-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="e3506-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3506-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3506-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e3506-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3506-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3506-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e3506-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e3506-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e3506-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3506-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3506-111">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3506-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e3506-112">Pointeur vers la structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="e3506-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3506-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3506-113">Return value</span></span>

<span data-ttu-id="e3506-114">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3506-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e3506-115">Pointeur vers une structure D3DXQUATERNION qui est le logarithme népérien.</span><span class="sxs-lookup"><span data-stu-id="e3506-115">Pointer to a D3DXQUATERNION structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3506-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e3506-116">Remarks</span></span>

<span data-ttu-id="e3506-117">La fonction D3DXQuaternionLn fonctionne uniquement pour les quaternions d’unité.</span><span class="sxs-lookup"><span data-stu-id="e3506-117">The D3DXQuaternionLn function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="e3506-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="e3506-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e3506-119">De cette façon, la fonction D3DXQuaternionLn peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="e3506-119">In this way, the D3DXQuaternionLn function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e3506-120">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="e3506-120">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3506-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3506-121">Requirements</span></span>



| <span data-ttu-id="e3506-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3506-122">Requirement</span></span> | <span data-ttu-id="e3506-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3506-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3506-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3506-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e3506-125"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3506-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e3506-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e3506-126">Library</span></span><br/> | <dl> <span data-ttu-id="e3506-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3506-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3506-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3506-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3506-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="e3506-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
