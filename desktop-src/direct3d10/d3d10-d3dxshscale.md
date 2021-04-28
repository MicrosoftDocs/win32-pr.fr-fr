---
description: 'D3DXSHScale, fonction (D3DX10. h) : met à l’échelle un vecteur d’harmonique sphérique (SH). en d’autres termes, moue \[ i \] = PA \[ i \] \* Scale.'
ms.assetid: e323d238-f635-4780-982d-8798ba178f31
title: D3DXSHScale, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0fab96575e5542eaaed725a88f9ba52c3289a4ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108497"
---
# <a name="d3dxshscale-function-d3dx10h"></a><span data-ttu-id="c33f4-103">D3DXSHScale, fonction (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="c33f4-103">D3DXSHScale function (D3DX10.h)</span></span>

<span data-ttu-id="c33f4-104">Met à l’échelle un vecteur d’harmonique sphérique (SH); en d’autres termes, moue \[ i \] = PA \[ i \] \* Scale.</span><span class="sxs-lookup"><span data-stu-id="c33f4-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="c33f4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c33f4-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pIn,
  _In_ const FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="c33f4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c33f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c33f4-107">*moue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c33f4-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33f4-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c33f4-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c33f4-109">Pointeur vers les coefficients de sortie de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="c33f4-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="c33f4-110">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="c33f4-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="c33f4-111">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c33f4-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c33f4-112">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c33f4-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33f4-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c33f4-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c33f4-114">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="c33f4-114">Order of the SH evaluation.</span></span> <span data-ttu-id="c33f4-115">La valeur doit être comprise entre D3DXSH \_ MINORDER et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="c33f4-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="c33f4-116">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="c33f4-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="c33f4-117">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="c33f4-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="c33f4-118">*code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c33f4-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33f4-119">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c33f4-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c33f4-120">Pointeur vers le vecteur SH à mettre à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="c33f4-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="c33f4-121">Mise à l' *échelle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c33f4-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33f4-122">Type : **const [**float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c33f4-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c33f4-123">Pointeur désignant la valeur de l’échelle.</span><span class="sxs-lookup"><span data-stu-id="c33f4-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c33f4-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c33f4-124">Return value</span></span>

<span data-ttu-id="c33f4-125">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c33f4-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c33f4-126">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="c33f4-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="c33f4-127">Notes </span><span class="sxs-lookup"><span data-stu-id="c33f4-127">Remarks</span></span>

<span data-ttu-id="c33f4-128">Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :</span><span class="sxs-lookup"><span data-stu-id="c33f4-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="c33f4-129">l est le degré de la fonction de base.</span><span class="sxs-lookup"><span data-stu-id="c33f4-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="c33f4-130">m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.</span><span class="sxs-lookup"><span data-stu-id="c33f4-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="c33f4-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c33f4-131">Requirements</span></span>



| <span data-ttu-id="c33f4-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c33f4-132">Requirement</span></span> | <span data-ttu-id="c33f4-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c33f4-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c33f4-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="c33f4-134">Header</span></span><br/>  | <dl> <span data-ttu-id="c33f4-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c33f4-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c33f4-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c33f4-136">Library</span></span><br/> | <dl> <span data-ttu-id="c33f4-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c33f4-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c33f4-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c33f4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c33f4-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="c33f4-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
