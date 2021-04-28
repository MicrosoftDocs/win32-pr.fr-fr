---
description: 'Fonction D3DXPlaneNormalize (D3dx9math. h) : normalise les coefficients de plan afin que la normale du plan ait une longueur d’unité.'
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: D3DXPlaneNormalize, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d38ccbc3f688ed61779cf48a77e97dfb544c686e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094147"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a><span data-ttu-id="30117-103">D3DXPlaneNormalize, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="30117-103">D3DXPlaneNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="30117-104">Normalise les coefficients de plan afin que la normale du plan ait une longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="30117-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="30117-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30117-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="30117-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30117-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30117-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="30117-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30117-108">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="30117-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="30117-109">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="30117-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="30117-110">*pp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30117-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30117-111">Type : **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="30117-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="30117-112">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) source.</span><span class="sxs-lookup"><span data-stu-id="30117-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30117-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="30117-113">Return value</span></span>

<span data-ttu-id="30117-114">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="30117-114">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="30117-115">Pointeur vers une structure [**D3DXPLANE**](d3dxplane.md) qui représente la normale du plan.</span><span class="sxs-lookup"><span data-stu-id="30117-115">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="30117-116">Notes </span><span class="sxs-lookup"><span data-stu-id="30117-116">Remarks</span></span>

<span data-ttu-id="30117-117">Cette fonction normalise un plan afin que \| a, b, c \| = = 1.</span><span class="sxs-lookup"><span data-stu-id="30117-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="30117-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="30117-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="30117-119">De cette façon, cette fonction peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="30117-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="30117-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30117-120">Requirements</span></span>



| <span data-ttu-id="30117-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30117-121">Requirement</span></span> | <span data-ttu-id="30117-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="30117-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30117-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="30117-123">Header</span></span><br/>  | <dl> <span data-ttu-id="30117-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="30117-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="30117-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="30117-125">Library</span></span><br/> | <dl> <span data-ttu-id="30117-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30117-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="30117-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30117-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30117-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="30117-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




