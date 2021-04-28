---
description: 'Fonction D3DXSHRotate (D3dx9math. h) : fait pivoter le vecteur d’harmonique sphérique (SH) par la matrice donnée.'
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: D3DXSHRotate, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8f888186fb6d7563a5904d4e6e3f1eabe626afd1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093867"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a><span data-ttu-id="1bb73-103">D3DXSHRotate, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1bb73-103">D3DXSHRotate function (D3dx9math.h)</span></span>

<span data-ttu-id="1bb73-104">Fait pivoter le vecteur d’harmonique sphérique (SH) par la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="1bb73-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bb73-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bb73-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _Out_       FLOAT      *pOut,
  _In_        UINT       Order,
  _In_  const D3DXMATRIX *pMatrix,
  _In_  const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="1bb73-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bb73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bb73-107">*moue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1bb73-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb73-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bb73-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1bb73-109">Pointeur vers les coefficients de sortie de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="1bb73-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="1bb73-110">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="1bb73-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="1bb73-111">Ce pointeur ne doit pas être un alias avec *pin*.</span><span class="sxs-lookup"><span data-stu-id="1bb73-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="1bb73-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1bb73-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1bb73-113">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bb73-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb73-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bb73-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bb73-115">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="1bb73-115">Order of the SH evaluation.</span></span> <span data-ttu-id="1bb73-116">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="1bb73-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="1bb73-117">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="1bb73-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="1bb73-118">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="1bb73-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="1bb73-119">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bb73-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb73-120">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1bb73-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1bb73-121">Pointeur vers la matrice de rotation.</span><span class="sxs-lookup"><span data-stu-id="1bb73-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="1bb73-122">La sous-matrice de rotation doit être orthogonale, avec un déterminant d’unité.</span><span class="sxs-lookup"><span data-stu-id="1bb73-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="1bb73-123">*code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bb73-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb73-124">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1bb73-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1bb73-125">Pointeur vers les coefficients SH pivotés.</span><span class="sxs-lookup"><span data-stu-id="1bb73-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bb73-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bb73-126">Return value</span></span>

<span data-ttu-id="1bb73-127">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bb73-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1bb73-128">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="1bb73-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bb73-129">Notes </span><span class="sxs-lookup"><span data-stu-id="1bb73-129">Remarks</span></span>

<span data-ttu-id="1bb73-130">Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :</span><span class="sxs-lookup"><span data-stu-id="1bb73-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="1bb73-131">l est le degré de la fonction de base.</span><span class="sxs-lookup"><span data-stu-id="1bb73-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="1bb73-132">m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.</span><span class="sxs-lookup"><span data-stu-id="1bb73-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bb73-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bb73-133">Requirements</span></span>



| <span data-ttu-id="1bb73-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bb73-134">Requirement</span></span> | <span data-ttu-id="1bb73-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bb73-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bb73-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="1bb73-136">Header</span></span><br/>  | <dl> <span data-ttu-id="1bb73-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bb73-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1bb73-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1bb73-138">Library</span></span><br/> | <dl> <span data-ttu-id="1bb73-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bb73-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1bb73-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bb73-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bb73-141">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="1bb73-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1bb73-142">Transfert de luminance précalculé (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1bb73-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
