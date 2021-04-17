---
description: Recherche l’intersection entre un plan et une ligne.
ms.assetid: 2723cd3e-fdc3-4aab-a089-0089e5b14e3e
title: D3DXPlaneIntersectLine, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4a91a4592d039510e11147ffb680c880c43ccec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211681"
---
# <a name="d3dxplaneintersectline-function-d3dx9mathh"></a><span data-ttu-id="ff90e-103">D3DXPlaneIntersectLine, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ff90e-103">D3DXPlaneIntersectLine function (D3dx9math.h)</span></span>

<span data-ttu-id="ff90e-104">Recherche l’intersection entre un plan et une ligne.</span><span class="sxs-lookup"><span data-stu-id="ff90e-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff90e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff90e-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="ff90e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff90e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff90e-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ff90e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff90e-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff90e-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ff90e-109">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , identifiant l’intersection entre le plan et la ligne spécifiés.</span><span class="sxs-lookup"><span data-stu-id="ff90e-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="ff90e-110">*pp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff90e-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff90e-111">Type : **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="ff90e-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="ff90e-112">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) source.</span><span class="sxs-lookup"><span data-stu-id="ff90e-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ff90e-113">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff90e-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff90e-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ff90e-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ff90e-115">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source, définissant un point de départ de ligne.</span><span class="sxs-lookup"><span data-stu-id="ff90e-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="ff90e-116">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff90e-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff90e-117">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ff90e-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ff90e-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source, définissant un point de fin de ligne.</span><span class="sxs-lookup"><span data-stu-id="ff90e-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff90e-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff90e-119">Return value</span></span>

<span data-ttu-id="ff90e-120">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff90e-120">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ff90e-121">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est l’intersection entre le plan et la ligne spécifiés.</span><span class="sxs-lookup"><span data-stu-id="ff90e-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff90e-122">Notes</span><span class="sxs-lookup"><span data-stu-id="ff90e-122">Remarks</span></span>

<span data-ttu-id="ff90e-123">Si la ligne est parallèle au plan, la **valeur null** est retournée.</span><span class="sxs-lookup"><span data-stu-id="ff90e-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="ff90e-124">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="ff90e-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ff90e-125">De cette façon, la fonction **D3DXPlaneIntersectLine** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="ff90e-125">In this way, the **D3DXPlaneIntersectLine** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff90e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff90e-126">Requirements</span></span>



| <span data-ttu-id="ff90e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff90e-127">Requirement</span></span> | <span data-ttu-id="ff90e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff90e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff90e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff90e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ff90e-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff90e-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ff90e-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ff90e-131">Library</span></span><br/> | <dl> <span data-ttu-id="ff90e-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff90e-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ff90e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff90e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff90e-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="ff90e-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




