---
description: Créez une matrice de traduction.
ms.assetid: a3565a06-22af-4ded-8835-da4c7ae81805
title: D3DXMatrixTranslation, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7abf55e5b51091de5d823ba837cdc8ad51e3940b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523226"
---
# <a name="d3dxmatrixtranslation-function-d3dx10mathh"></a><span data-ttu-id="5503f-103">D3DXMatrixTranslation, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="5503f-103">D3DXMatrixTranslation function (D3DX10Math.h)</span></span>

<span data-ttu-id="5503f-104">Créez une matrice de traduction.</span><span class="sxs-lookup"><span data-stu-id="5503f-104">Create a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5503f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5503f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="5503f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5503f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5503f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5503f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5503f-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5503f-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5503f-109">Matrice qui va devenir une matrice de translation.</span><span class="sxs-lookup"><span data-stu-id="5503f-109">The matrix that will become a translation matrix.</span></span> <span data-ttu-id="5503f-110">Consultez [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="5503f-110">See [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="5503f-111">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5503f-111">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5503f-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5503f-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5503f-113">Composant x de la traduction.</span><span class="sxs-lookup"><span data-stu-id="5503f-113">The x-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="5503f-114">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5503f-114">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5503f-115">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5503f-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5503f-116">Composant y de la traduction.</span><span class="sxs-lookup"><span data-stu-id="5503f-116">The y-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="5503f-117">*z* \[\]</span><span class="sxs-lookup"><span data-stu-id="5503f-117">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5503f-118">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5503f-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5503f-119">Composant z de la traduction.</span><span class="sxs-lookup"><span data-stu-id="5503f-119">The z-component of the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5503f-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5503f-120">Return value</span></span>

<span data-ttu-id="5503f-121">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5503f-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5503f-122">Matrice de translation.</span><span class="sxs-lookup"><span data-stu-id="5503f-122">The translation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="5503f-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5503f-123">Requirements</span></span>



| <span data-ttu-id="5503f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5503f-124">Requirement</span></span> | <span data-ttu-id="5503f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="5503f-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5503f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="5503f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5503f-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5503f-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5503f-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5503f-128">Library</span></span><br/> | <dl> <span data-ttu-id="5503f-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5503f-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5503f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5503f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5503f-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="5503f-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
