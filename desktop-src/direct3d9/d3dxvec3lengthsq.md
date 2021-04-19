---
description: Retourne le carré de la longueur d’un vecteur 3D.
ms.assetid: 25dc50cc-542b-4989-a858-9b37603393a0
title: D3DXVec3LengthSq, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3LengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bb7d17d4f1bc06d68a73a2cff9288d159381387
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539481"
---
# <a name="d3dxvec3lengthsq-function"></a><span data-ttu-id="e4661-103">D3DXVec3LengthSq fonction)</span><span class="sxs-lookup"><span data-stu-id="e4661-103">D3DXVec3LengthSq function</span></span>

<span data-ttu-id="e4661-104">Retourne le carré de la longueur d’un vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="e4661-104">Returns the square of the length of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4661-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4661-105">Syntax</span></span>


```C++
FLOAT D3DXVec3LengthSq(
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="e4661-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4661-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4661-107">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4661-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4661-108">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4661-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e4661-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="e4661-109">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4661-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4661-110">Return value</span></span>

<span data-ttu-id="e4661-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4661-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4661-112">Longueur au carré du vecteur.</span><span class="sxs-lookup"><span data-stu-id="e4661-112">The vector's squared length.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4661-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4661-113">Requirements</span></span>



| <span data-ttu-id="e4661-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4661-114">Requirement</span></span> | <span data-ttu-id="e4661-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4661-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4661-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4661-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e4661-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4661-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e4661-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e4661-118">Library</span></span><br/> | <dl> <span data-ttu-id="e4661-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4661-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4661-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4661-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4661-121">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="e4661-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e4661-122">**D3DXVec3Length**</span><span class="sxs-lookup"><span data-stu-id="e4661-122">**D3DXVec3Length**</span></span>](d3dxvec3length.md)
</dt> </dl>

 

 
