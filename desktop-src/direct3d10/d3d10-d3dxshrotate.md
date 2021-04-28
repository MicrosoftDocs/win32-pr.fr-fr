---
description: 'Fonction D3DXSHRotate (D3DX10. h) : fait pivoter le vecteur d’harmonique sphérique (SH) par la matrice donnée.'
ms.assetid: 22ed379a-ce08-46df-9cc1-8d5fde87c179
title: D3DXSHRotate, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2f2af3fe59c57ba32bc03bb59233bec72722bbb5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108537"
---
# <a name="d3dxshrotate-function-d3dx10h"></a><span data-ttu-id="6feee-103">D3DXSHRotate, fonction (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="6feee-103">D3DXSHRotate function (D3DX10.h)</span></span>

<span data-ttu-id="6feee-104">Fait pivoter le vecteur d’harmonique sphérique (SH) par la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="6feee-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6feee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6feee-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _In_       FLOAT      *pOut,
  _In_       UINT       Order,
  _In_ const D3DXMATRIX *pMatrix,
  _In_ const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="6feee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6feee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6feee-107">*moue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6feee-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6feee-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6feee-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6feee-109">Pointeur vers les coefficients de sortie de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="6feee-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="6feee-110">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="6feee-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="6feee-111">Ce pointeur ne doit pas être un alias avec pIn.</span><span class="sxs-lookup"><span data-stu-id="6feee-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="6feee-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="6feee-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6feee-113">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6feee-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6feee-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6feee-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6feee-115">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="6feee-115">Order of the SH evaluation.</span></span> <span data-ttu-id="6feee-116">La valeur doit être comprise entre D3DXSH \_ MINORDER et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="6feee-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="6feee-117">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="6feee-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="6feee-118">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="6feee-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="6feee-119">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6feee-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6feee-120">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6feee-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6feee-121">Pointeur vers la matrice de rotation.</span><span class="sxs-lookup"><span data-stu-id="6feee-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="6feee-122">La sous-matrice de rotation doit être orthogonale, avec un déterminant d’unité.</span><span class="sxs-lookup"><span data-stu-id="6feee-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="6feee-123">*code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6feee-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6feee-124">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6feee-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6feee-125">Pointeur vers les coefficients SH pivotés.</span><span class="sxs-lookup"><span data-stu-id="6feee-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6feee-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6feee-126">Return value</span></span>

<span data-ttu-id="6feee-127">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6feee-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6feee-128">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="6feee-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="6feee-129">Notes </span><span class="sxs-lookup"><span data-stu-id="6feee-129">Remarks</span></span>

<span data-ttu-id="6feee-130">Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :</span><span class="sxs-lookup"><span data-stu-id="6feee-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="6feee-131">l est le degré de la fonction de base.</span><span class="sxs-lookup"><span data-stu-id="6feee-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="6feee-132">m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.</span><span class="sxs-lookup"><span data-stu-id="6feee-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="6feee-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6feee-133">Requirements</span></span>



| <span data-ttu-id="6feee-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6feee-134">Requirement</span></span> | <span data-ttu-id="6feee-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="6feee-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6feee-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="6feee-136">Header</span></span><br/>  | <dl> <span data-ttu-id="6feee-137"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6feee-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6feee-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6feee-138">Library</span></span><br/> | <dl> <span data-ttu-id="6feee-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6feee-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6feee-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6feee-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6feee-141">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="6feee-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
