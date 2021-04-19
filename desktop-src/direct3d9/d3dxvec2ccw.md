---
description: Retourne le composant z en utilisant le produit croisé de deux vecteurs 2D.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: D3DXVec2CCW, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71c6e14171a9e7d12d86c30f05885cecf50ce973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538971"
---
# <a name="d3dxvec2ccw-function"></a><span data-ttu-id="de3f2-103">D3DXVec2CCW fonction)</span><span class="sxs-lookup"><span data-stu-id="de3f2-103">D3DXVec2CCW function</span></span>

<span data-ttu-id="de3f2-104">Retourne le composant z en utilisant le produit croisé de deux vecteurs 2D.</span><span class="sxs-lookup"><span data-stu-id="de3f2-104">Returns the z-component by taking the cross product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="de3f2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de3f2-105">Syntax</span></span>


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="de3f2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de3f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de3f2-107">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="de3f2-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de3f2-108">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="de3f2-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="de3f2-109">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="de3f2-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="de3f2-110">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="de3f2-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de3f2-111">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="de3f2-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="de3f2-112">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="de3f2-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de3f2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de3f2-113">Return value</span></span>

<span data-ttu-id="de3f2-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="de3f2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="de3f2-115">Composant z.</span><span class="sxs-lookup"><span data-stu-id="de3f2-115">The z-component.</span></span>

## <a name="remarks"></a><span data-ttu-id="de3f2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="de3f2-116">Remarks</span></span>

<span data-ttu-id="de3f2-117">Cette fonction détermine le composant z en déterminant le produit croisé en fonction de la formule suivante : ((x1, y1, 0) Croix (x2, Y2, 0)).</span><span class="sxs-lookup"><span data-stu-id="de3f2-117">This function determines the z-component by determining the cross-product based on the following formula: ((x1,y1,0) cross (x2,y2,0)).</span></span> <span data-ttu-id="de3f2-118">Ou comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="de3f2-118">Or as shown in the following example.</span></span>


```
pV1->x * pV2->y - pV1->y * pV2->x
```



<span data-ttu-id="de3f2-119">Si la valeur du composant z est positive, le vecteur v2 est dans le sens inverse des aiguilles d’une position dans le vecteur v1.</span><span class="sxs-lookup"><span data-stu-id="de3f2-119">If the value of the z-component is positive, the vector V2 is counterclockwise from the vector V1.</span></span> <span data-ttu-id="de3f2-120">Ces informations sont utiles pour l’élimination des faces arrière.</span><span class="sxs-lookup"><span data-stu-id="de3f2-120">This information is useful for back-face culling.</span></span>

## <a name="requirements"></a><span data-ttu-id="de3f2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de3f2-121">Requirements</span></span>



| <span data-ttu-id="de3f2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de3f2-122">Requirement</span></span> | <span data-ttu-id="de3f2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="de3f2-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de3f2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="de3f2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="de3f2-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="de3f2-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="de3f2-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="de3f2-126">Library</span></span><br/> | <dl> <span data-ttu-id="de3f2-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de3f2-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="de3f2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de3f2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de3f2-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="de3f2-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="de3f2-130">**D3DXVec2Dot**</span><span class="sxs-lookup"><span data-stu-id="de3f2-130">**D3DXVec2Dot**</span></span>](d3dxvec2dot.md)
</dt> </dl>

 

 
