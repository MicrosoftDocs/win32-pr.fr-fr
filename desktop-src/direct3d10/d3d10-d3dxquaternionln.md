---
description: 'Fonction D3DXQuaternionLn (D3DX10Math. h) : calcule le logarithme népérien.'
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
ms.openlocfilehash: 9abaaa231e424e55e496b7901882e9da17c59786
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103207"
---
# <a name="d3dxquaternionln-function-d3dx10mathh"></a><span data-ttu-id="3f0ca-103">D3DXQuaternionLn, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="3f0ca-103">D3DXQuaternionLn function (D3DX10Math.h)</span></span>

<span data-ttu-id="3f0ca-104">Calcule le logarithme népérien.</span><span class="sxs-lookup"><span data-stu-id="3f0ca-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f0ca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f0ca-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="3f0ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f0ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f0ca-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3f0ca-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0ca-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f0ca-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3f0ca-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3f0ca-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3f0ca-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3f0ca-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0ca-111">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="3f0ca-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3f0ca-112">Pointeur vers la structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="3f0ca-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f0ca-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3f0ca-113">Return value</span></span>

<span data-ttu-id="3f0ca-114">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f0ca-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3f0ca-115">Pointeur vers une structure D3DXQUATERNION qui est le logarithme népérien.</span><span class="sxs-lookup"><span data-stu-id="3f0ca-115">Pointer to a D3DXQUATERNION structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f0ca-116">Notes </span><span class="sxs-lookup"><span data-stu-id="3f0ca-116">Remarks</span></span>

<span data-ttu-id="3f0ca-117">La fonction D3DXQuaternionLn fonctionne uniquement pour les quaternions d’unité.</span><span class="sxs-lookup"><span data-stu-id="3f0ca-117">The D3DXQuaternionLn function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="3f0ca-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="3f0ca-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="3f0ca-119">De cette façon, la fonction D3DXQuaternionLn peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="3f0ca-119">In this way, the D3DXQuaternionLn function can be used as a parameter for another function.</span></span>

<span data-ttu-id="3f0ca-120">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="3f0ca-120">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f0ca-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f0ca-121">Requirements</span></span>



| <span data-ttu-id="3f0ca-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f0ca-122">Requirement</span></span> | <span data-ttu-id="3f0ca-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f0ca-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f0ca-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f0ca-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3f0ca-125"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f0ca-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="3f0ca-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3f0ca-126">Library</span></span><br/> | <dl> <span data-ttu-id="3f0ca-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f0ca-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3f0ca-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f0ca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f0ca-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="3f0ca-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
