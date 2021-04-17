---
description: Calcule le logarithme népérien.
ms.assetid: 73ca7d13-1e20-48fc-b0ed-0d3127d094a7
title: D3DXQuaternionLn, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b51fcc77da29216acd2bfc1c011a063014da5d69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531017"
---
# <a name="d3dxquaternionln-function-d3dx9mathh"></a><span data-ttu-id="741ca-103">D3DXQuaternionLn, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="741ca-103">D3DXQuaternionLn function (D3dx9math.h)</span></span>

<span data-ttu-id="741ca-104">Calcule le logarithme népérien.</span><span class="sxs-lookup"><span data-stu-id="741ca-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="741ca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="741ca-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="741ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="741ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="741ca-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="741ca-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="741ca-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="741ca-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="741ca-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="741ca-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="741ca-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="741ca-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="741ca-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="741ca-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="741ca-112">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="741ca-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="741ca-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="741ca-113">Return value</span></span>

<span data-ttu-id="741ca-114">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="741ca-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="741ca-115">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le logarithme népérien.</span><span class="sxs-lookup"><span data-stu-id="741ca-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="741ca-116">Notes</span><span class="sxs-lookup"><span data-stu-id="741ca-116">Remarks</span></span>

<span data-ttu-id="741ca-117">La fonction **D3DXQuaternionLn** fonctionne uniquement pour les quaternions d’unité.</span><span class="sxs-lookup"><span data-stu-id="741ca-117">The **D3DXQuaternionLn** function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="741ca-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="741ca-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="741ca-119">De cette façon, la fonction **D3DXQuaternionLn** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="741ca-119">In this way, the **D3DXQuaternionLn** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="741ca-120">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="741ca-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="741ca-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="741ca-121">Requirements</span></span>



| <span data-ttu-id="741ca-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="741ca-122">Requirement</span></span> | <span data-ttu-id="741ca-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="741ca-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="741ca-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="741ca-124">Header</span></span><br/>  | <dl> <span data-ttu-id="741ca-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="741ca-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="741ca-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="741ca-126">Library</span></span><br/> | <dl> <span data-ttu-id="741ca-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="741ca-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="741ca-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="741ca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="741ca-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="741ca-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="741ca-130">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="741ca-130">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="741ca-131">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="741ca-131">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




