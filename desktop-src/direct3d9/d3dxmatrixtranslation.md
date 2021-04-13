---
description: Génère une matrice à l’aide des décalages spécifiés.
ms.assetid: 1cb713d5-b994-4496-a506-89451be09fb2
title: D3DXMatrixTranslation, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c74d56eaa0e41bc6ce9060ff291885a8a5c05a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322890"
---
# <a name="d3dxmatrixtranslation-function-d3dx9mathh"></a><span data-ttu-id="c9717-103">D3DXMatrixTranslation, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c9717-103">D3DXMatrixTranslation function (D3dx9math.h)</span></span>

<span data-ttu-id="c9717-104">Génère une matrice à l’aide des décalages spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c9717-104">Builds a matrix using the specified offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9717-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9717-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="c9717-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9717-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9717-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c9717-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9717-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9717-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c9717-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c9717-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c9717-110">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9717-110">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9717-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9717-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9717-112">Décalage de la coordonnée X.</span><span class="sxs-lookup"><span data-stu-id="c9717-112">X-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="c9717-113">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9717-113">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9717-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9717-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9717-115">Décalage de la coordonnée Y.</span><span class="sxs-lookup"><span data-stu-id="c9717-115">Y-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="c9717-116">*z* \[\]</span><span class="sxs-lookup"><span data-stu-id="c9717-116">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9717-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9717-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9717-118">Décalage de la coordonnée Z.</span><span class="sxs-lookup"><span data-stu-id="c9717-118">Z-coordinate offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9717-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9717-119">Return value</span></span>

<span data-ttu-id="c9717-120">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9717-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c9717-121">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui contient une matrice de transformation traduite.</span><span class="sxs-lookup"><span data-stu-id="c9717-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains a translated transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9717-122">Notes</span><span class="sxs-lookup"><span data-stu-id="c9717-122">Remarks</span></span>

<span data-ttu-id="c9717-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="c9717-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c9717-124">De cette façon, D3DXMATRIXTranslation peut être utilisé comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="c9717-124">In this way, the D3DXMATRIXTranslation can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9717-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9717-125">Requirements</span></span>



| <span data-ttu-id="c9717-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9717-126">Requirement</span></span> | <span data-ttu-id="c9717-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9717-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9717-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9717-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c9717-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9717-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c9717-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c9717-130">Library</span></span><br/> | <dl> <span data-ttu-id="c9717-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9717-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c9717-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9717-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9717-133">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="c9717-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
