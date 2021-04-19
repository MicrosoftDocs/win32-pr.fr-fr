---
description: Détermine le produit scalaire de deux vecteurs 2D.
ms.assetid: ae77ff29-44be-4b67-9c63-aaffa4fe8d59
title: D3DXVec2Dot, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 79b65127c415695b3df9f927b6edff8fcdd5c58d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537248"
---
# <a name="d3dxvec2dot-function"></a><span data-ttu-id="4b8a6-103">D3DXVec2Dot fonction)</span><span class="sxs-lookup"><span data-stu-id="4b8a6-103">D3DXVec2Dot function</span></span>

<span data-ttu-id="4b8a6-104">Détermine le produit scalaire de deux vecteurs 2D.</span><span class="sxs-lookup"><span data-stu-id="4b8a6-104">Determines the dot product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b8a6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b8a6-105">Syntax</span></span>


```C++
FLOAT D3DXVec2Dot(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="4b8a6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b8a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b8a6-107">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b8a6-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b8a6-108">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4b8a6-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4b8a6-109">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="4b8a6-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4b8a6-110">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b8a6-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b8a6-111">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4b8a6-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4b8a6-112">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="4b8a6-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b8a6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b8a6-113">Return value</span></span>

<span data-ttu-id="4b8a6-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b8a6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4b8a6-115">Produit scalaire.</span><span class="sxs-lookup"><span data-stu-id="4b8a6-115">The dot product.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b8a6-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b8a6-116">Requirements</span></span>



| <span data-ttu-id="4b8a6-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b8a6-117">Requirement</span></span> | <span data-ttu-id="4b8a6-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b8a6-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b8a6-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="4b8a6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4b8a6-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b8a6-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4b8a6-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4b8a6-121">Library</span></span><br/> | <dl> <span data-ttu-id="4b8a6-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b8a6-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4b8a6-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b8a6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b8a6-124">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="4b8a6-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4b8a6-125">**D3DXVec2CCW**</span><span class="sxs-lookup"><span data-stu-id="4b8a6-125">**D3DXVec2CCW**</span></span>](d3dxvec2ccw.md)
</dt> </dl>

 

 
