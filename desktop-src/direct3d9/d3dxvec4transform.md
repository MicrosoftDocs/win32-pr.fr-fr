---
description: D3DXVec4Transform, fonction (D3dx9math. h)-transforme un vecteur 4D par une matrice donnée.
ms.assetid: de93f138-7cf8-43cc-8255-c053c799aea8
title: D3DXVec4Transform, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e5a9fdd92a2d978c746543fbbbeec6503d07404
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115507"
---
# <a name="d3dxvec4transform-function-d3dx9mathh"></a><span data-ttu-id="a70dc-103">D3DXVec4Transform, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a70dc-103">D3DXVec4Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="a70dc-104">Transforme un vecteur 4D par une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="a70dc-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a70dc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a70dc-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="a70dc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a70dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a70dc-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a70dc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a70dc-108">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a70dc-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a70dc-109">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a70dc-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a70dc-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a70dc-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a70dc-111">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a70dc-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a70dc-112">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="a70dc-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a70dc-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a70dc-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a70dc-114">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a70dc-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a70dc-115">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="a70dc-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a70dc-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a70dc-116">Return value</span></span>

<span data-ttu-id="a70dc-117">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a70dc-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a70dc-118">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le vecteur 4D transformé.</span><span class="sxs-lookup"><span data-stu-id="a70dc-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="a70dc-119">Notes </span><span class="sxs-lookup"><span data-stu-id="a70dc-119">Remarks</span></span>

<span data-ttu-id="a70dc-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="a70dc-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a70dc-121">De cette façon, la fonction **D3DXVec4Transform** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="a70dc-121">In this way, the **D3DXVec4Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a70dc-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a70dc-122">Requirements</span></span>



| <span data-ttu-id="a70dc-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a70dc-123">Requirement</span></span> | <span data-ttu-id="a70dc-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a70dc-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a70dc-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a70dc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a70dc-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a70dc-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a70dc-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a70dc-127">Library</span></span><br/> | <dl> <span data-ttu-id="a70dc-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a70dc-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a70dc-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a70dc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a70dc-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="a70dc-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




