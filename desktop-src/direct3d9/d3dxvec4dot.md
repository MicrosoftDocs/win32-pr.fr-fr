---
description: Détermine le produit scalaire de deux vecteurs 4D.
ms.assetid: 565dede8-6cc8-4313-9480-2f252cac94f2
title: D3DXVec4Dot, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a0ef075a768fe9b70a38a4bc3d88b094359bd546
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394148"
---
# <a name="d3dxvec4dot-function"></a><span data-ttu-id="c4744-103">D3DXVec4Dot fonction)</span><span class="sxs-lookup"><span data-stu-id="c4744-103">D3DXVec4Dot function</span></span>

<span data-ttu-id="c4744-104">Détermine le produit scalaire de deux vecteurs 4D.</span><span class="sxs-lookup"><span data-stu-id="c4744-104">Determines the dot product of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4744-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4744-105">Syntax</span></span>


```C++
FLOAT D3DXVec4Dot(
  _In_ const D3DXVECTOR4 *pV1,
  _In_ const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="c4744-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4744-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4744-107">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4744-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4744-108">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c4744-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c4744-109">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="c4744-109">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c4744-110">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4744-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4744-111">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c4744-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c4744-112">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="c4744-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4744-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4744-113">Return value</span></span>

<span data-ttu-id="c4744-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4744-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4744-115">Produit scalaire.</span><span class="sxs-lookup"><span data-stu-id="c4744-115">The dot product.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4744-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4744-116">Requirements</span></span>



| <span data-ttu-id="c4744-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4744-117">Requirement</span></span> | <span data-ttu-id="c4744-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4744-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4744-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4744-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c4744-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4744-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c4744-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c4744-121">Library</span></span><br/> | <dl> <span data-ttu-id="c4744-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4744-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4744-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4744-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4744-124">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="c4744-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c4744-125">**D3DXVec4Cross**</span><span class="sxs-lookup"><span data-stu-id="c4744-125">**D3DXVec4Cross**</span></span>](d3dxvec4cross.md)
</dt> </dl>

 

 
