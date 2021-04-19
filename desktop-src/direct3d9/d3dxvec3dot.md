---
description: Détermine le produit scalaire de deux vecteurs 3D.
ms.assetid: 61aa7751-cc06-4673-929b-d7c1e691e395
title: D3DXVec3Dot, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22d6930a44f129154482f9b1aab24337e8bcdc83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524854"
---
# <a name="d3dxvec3dot-function"></a><span data-ttu-id="72005-103">D3DXVec3Dot fonction)</span><span class="sxs-lookup"><span data-stu-id="72005-103">D3DXVec3Dot function</span></span>

<span data-ttu-id="72005-104">Détermine le produit scalaire de deux vecteurs 3D.</span><span class="sxs-lookup"><span data-stu-id="72005-104">Determines the dot product of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="72005-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72005-105">Syntax</span></span>


```C++
FLOAT D3DXVec3Dot(
  _In_ const D3DXVECTOR3 *pV1,
  _In_ const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="72005-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72005-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72005-107">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72005-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72005-108">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="72005-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="72005-109">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="72005-109">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="72005-110">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72005-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72005-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="72005-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="72005-112">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="72005-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72005-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72005-113">Return value</span></span>

<span data-ttu-id="72005-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72005-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72005-115">Le produit de point.</span><span class="sxs-lookup"><span data-stu-id="72005-115">The dot-product.</span></span>

## <a name="requirements"></a><span data-ttu-id="72005-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72005-116">Requirements</span></span>



| <span data-ttu-id="72005-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72005-117">Requirement</span></span> | <span data-ttu-id="72005-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="72005-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72005-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="72005-119">Header</span></span><br/>  | <dl> <span data-ttu-id="72005-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="72005-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="72005-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="72005-121">Library</span></span><br/> | <dl> <span data-ttu-id="72005-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72005-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="72005-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72005-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72005-124">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="72005-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="72005-125">**D3DXVec3Cross**</span><span class="sxs-lookup"><span data-stu-id="72005-125">**D3DXVec3Cross**</span></span>](d3dxvec3cross.md)
</dt> </dl>

 

 
