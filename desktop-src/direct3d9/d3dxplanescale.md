---
description: Mettre à l’échelle le plan avec le facteur d’échelle donné.
ms.assetid: 3a0454ef-2821-472f-b7a4-5e49bb5f556e
title: D3DXPlaneScale, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39bd80ceebaee915b8175f2adf13b3b200000fa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525851"
---
# <a name="d3dxplanescale-function"></a><span data-ttu-id="2e079-103">D3DXPlaneScale fonction)</span><span class="sxs-lookup"><span data-stu-id="2e079-103">D3DXPlaneScale function</span></span>

<span data-ttu-id="2e079-104">Mettre à l’échelle le plan avec le facteur d’échelle donné.</span><span class="sxs-lookup"><span data-stu-id="2e079-104">Scale the plane with the given scaling factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e079-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e079-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneScale(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="2e079-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e079-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e079-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2e079-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e079-108">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e079-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="2e079-109">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="2e079-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2e079-110">*pp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e079-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e079-111">Type : **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e079-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="2e079-112">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) source.</span><span class="sxs-lookup"><span data-stu-id="2e079-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2e079-113"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e079-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e079-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e079-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e079-115">Facteur d’échelle.</span><span class="sxs-lookup"><span data-stu-id="2e079-115">Scale factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e079-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e079-116">Return value</span></span>

<span data-ttu-id="2e079-117">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e079-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="2e079-118">Pointeur vers une structure [**D3DXPLANE**](d3dxplane.md) qui représente le plan mis à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="2e079-118">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the scaled plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e079-119">Notes</span><span class="sxs-lookup"><span data-stu-id="2e079-119">Remarks</span></span>

<span data-ttu-id="2e079-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="2e079-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2e079-121">Par conséquent, cette fonction peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="2e079-121">Therefore, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e079-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e079-122">Requirements</span></span>



| <span data-ttu-id="2e079-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e079-123">Requirement</span></span> | <span data-ttu-id="2e079-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e079-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e079-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e079-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2e079-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e079-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2e079-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2e079-127">Library</span></span><br/> | <dl> <span data-ttu-id="2e079-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e079-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e079-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e079-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e079-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="2e079-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
