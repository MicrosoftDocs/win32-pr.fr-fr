---
description: Crée une matrice qui met à l’échelle le long de l’axe x, de l’axe y et de l’axe z.
ms.assetid: 1804bf41-26de-4be1-ad62-7a871d7408e6
title: D3DXMatrixScaling, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixScaling
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: adb1becb67a561778b31c90ea3d6c96e776c9a67
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323217"
---
# <a name="d3dxmatrixscaling-function-d3dx10mathh"></a><span data-ttu-id="6ca54-103">D3DXMatrixScaling, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6ca54-103">D3DXMatrixScaling function (D3DX10Math.h)</span></span>

<span data-ttu-id="6ca54-104">Crée une matrice qui met à l’échelle le long de l’axe x, de l’axe y et de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="6ca54-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ca54-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ca54-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="6ca54-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ca54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ca54-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6ca54-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ca54-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ca54-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6ca54-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6ca54-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6ca54-110">*SX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ca54-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ca54-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ca54-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ca54-112">Facteur d’échelle appliqué le long de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="6ca54-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="6ca54-113">*SY* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ca54-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ca54-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ca54-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ca54-115">Facteur d’échelle appliqué le long de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="6ca54-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="6ca54-116">*SZ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ca54-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ca54-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ca54-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ca54-118">Facteur d’échelle appliqué le long de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="6ca54-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ca54-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6ca54-119">Return value</span></span>

<span data-ttu-id="6ca54-120">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ca54-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6ca54-121">Pointeur vers la transformation de mise à l’échelle D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="6ca54-121">Pointer to the scaling transformation D3DXMATRIX.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ca54-122">Notes</span><span class="sxs-lookup"><span data-stu-id="6ca54-122">Remarks</span></span>

<span data-ttu-id="6ca54-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="6ca54-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6ca54-124">De cette façon, la fonction D3DXMatrixScaling peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="6ca54-124">In this way, the D3DXMatrixScaling function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ca54-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ca54-125">Requirements</span></span>



| <span data-ttu-id="6ca54-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ca54-126">Requirement</span></span> | <span data-ttu-id="6ca54-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ca54-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca54-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ca54-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6ca54-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ca54-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6ca54-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6ca54-130">Library</span></span><br/> | <dl> <span data-ttu-id="6ca54-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ca54-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ca54-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ca54-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca54-133">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="6ca54-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
