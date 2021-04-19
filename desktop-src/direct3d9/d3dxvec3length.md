---
description: Retourne la longueur d’un vecteur 3D.
ms.assetid: 78da506c-3169-48e9-934c-cc09271a10d4
title: D3DXVec3Length, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 653e53fb22961c858c7649f95e4453fec08087fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539435"
---
# <a name="d3dxvec3length-function"></a><span data-ttu-id="69442-103">D3DXVec3Length fonction)</span><span class="sxs-lookup"><span data-stu-id="69442-103">D3DXVec3Length function</span></span>

<span data-ttu-id="69442-104">Retourne la longueur d’un vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="69442-104">Returns the length of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="69442-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69442-105">Syntax</span></span>


```C++
FLOAT D3DXVec3Length(
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="69442-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69442-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69442-107">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69442-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69442-108">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="69442-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="69442-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="69442-109">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69442-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69442-110">Return value</span></span>

<span data-ttu-id="69442-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69442-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69442-112">Longueur du vecteur.</span><span class="sxs-lookup"><span data-stu-id="69442-112">The vector's length.</span></span>

## <a name="requirements"></a><span data-ttu-id="69442-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69442-113">Requirements</span></span>



| <span data-ttu-id="69442-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69442-114">Requirement</span></span> | <span data-ttu-id="69442-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="69442-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69442-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="69442-116">Header</span></span><br/>  | <dl> <span data-ttu-id="69442-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="69442-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="69442-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="69442-118">Library</span></span><br/> | <dl> <span data-ttu-id="69442-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69442-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="69442-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69442-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69442-121">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="69442-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="69442-122">**D3DXVec3LengthSq**</span><span class="sxs-lookup"><span data-stu-id="69442-122">**D3DXVec3LengthSq**</span></span>](d3dxvec3lengthsq.md)
</dt> </dl>

 

 
