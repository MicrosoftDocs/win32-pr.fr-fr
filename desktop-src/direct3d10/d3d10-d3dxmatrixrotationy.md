---
description: 'D3DXMatrixRotationY, fonction (D3DX10Math. h) : crée une matrice qui pivote autour de l’axe y.'
ms.assetid: b58def9b-29dc-4c7d-89a3-188ef9b9f94f
title: D3DXMatrixRotationY, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationY
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 570179fadc9008c5f919acf657541e53ab399ac8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108967"
---
# <a name="d3dxmatrixrotationy-function-d3dx10mathh"></a><span data-ttu-id="987bd-103">D3DXMatrixRotationY, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="987bd-103">D3DXMatrixRotationY function (D3DX10Math.h)</span></span>

<span data-ttu-id="987bd-104">Crée une matrice qui pivote autour de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="987bd-104">Builds a matrix that rotates around the y-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="987bd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="987bd-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationY(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="987bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="987bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="987bd-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="987bd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="987bd-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="987bd-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="987bd-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="987bd-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="987bd-110">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="987bd-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="987bd-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="987bd-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="987bd-112">Angle de rotation en radians.</span><span class="sxs-lookup"><span data-stu-id="987bd-112">Angle of rotation in radians.</span></span> <span data-ttu-id="987bd-113">Les angles sont mesurés dans le sens des aiguilles d’une montre sur l’axe de rotation vers l’origine.</span><span class="sxs-lookup"><span data-stu-id="987bd-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="987bd-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="987bd-114">Return value</span></span>

<span data-ttu-id="987bd-115">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="987bd-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="987bd-116">Pointeur vers une structure D3DXMATRIX pivotée autour de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="987bd-116">Pointer to a D3DXMATRIX structure rotated around the y-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="987bd-117">Notes </span><span class="sxs-lookup"><span data-stu-id="987bd-117">Remarks</span></span>

<span data-ttu-id="987bd-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="987bd-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="987bd-119">De cette façon, la fonction D3DXMatrixRotationY peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="987bd-119">In this way, the D3DXMatrixRotationY function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="987bd-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="987bd-120">Requirements</span></span>



| <span data-ttu-id="987bd-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="987bd-121">Requirement</span></span> | <span data-ttu-id="987bd-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="987bd-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="987bd-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="987bd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="987bd-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="987bd-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="987bd-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="987bd-125">Library</span></span><br/> | <dl> <span data-ttu-id="987bd-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="987bd-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="987bd-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="987bd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="987bd-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="987bd-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
