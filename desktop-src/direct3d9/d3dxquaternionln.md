---
description: 'Fonction D3DXQuaternionLn (D3dx9math. h) : calcule le logarithme népérien.'
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
ms.openlocfilehash: d1a529c1c6ca4d7f81bf4d41fcdb4a7c7179874b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094057"
---
# <a name="d3dxquaternionln-function-d3dx9mathh"></a><span data-ttu-id="7597f-103">D3DXQuaternionLn, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7597f-103">D3DXQuaternionLn function (D3dx9math.h)</span></span>

<span data-ttu-id="7597f-104">Calcule le logarithme népérien.</span><span class="sxs-lookup"><span data-stu-id="7597f-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="7597f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7597f-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="7597f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7597f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7597f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7597f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7597f-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="7597f-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7597f-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7597f-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7597f-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7597f-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7597f-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="7597f-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7597f-112">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="7597f-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7597f-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7597f-113">Return value</span></span>

<span data-ttu-id="7597f-114">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="7597f-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7597f-115">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le logarithme népérien.</span><span class="sxs-lookup"><span data-stu-id="7597f-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="7597f-116">Notes </span><span class="sxs-lookup"><span data-stu-id="7597f-116">Remarks</span></span>

<span data-ttu-id="7597f-117">La fonction **D3DXQuaternionLn** fonctionne uniquement pour les quaternions d’unité.</span><span class="sxs-lookup"><span data-stu-id="7597f-117">The **D3DXQuaternionLn** function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="7597f-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="7597f-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7597f-119">De cette façon, la fonction **D3DXQuaternionLn** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="7597f-119">In this way, the **D3DXQuaternionLn** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7597f-120">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="7597f-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="7597f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7597f-121">Requirements</span></span>



| <span data-ttu-id="7597f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7597f-122">Requirement</span></span> | <span data-ttu-id="7597f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7597f-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7597f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7597f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7597f-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7597f-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7597f-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7597f-126">Library</span></span><br/> | <dl> <span data-ttu-id="7597f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7597f-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7597f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7597f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7597f-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="7597f-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7597f-130">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="7597f-130">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="7597f-131">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="7597f-131">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




