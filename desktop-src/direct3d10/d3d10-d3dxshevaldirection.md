---
description: 'Fonction D3DXSHEvalDirection (D3DX10. h) : évalue les fonctions de base de l’harmonique sphérique (SH) à partir d’un vecteur de direction d’entrée.'
ms.assetid: c86973cc-c5b0-4358-b7eb-5c31f38b5b5a
title: D3DXSHEvalDirection, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7fa1f94d65ca8096a0398d71ca2f562b643d47a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108587"
---
# <a name="d3dxshevaldirection-function-d3dx10h"></a><span data-ttu-id="8ff96-103">D3DXSHEvalDirection, fonction (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="8ff96-103">D3DXSHEvalDirection function (D3DX10.h)</span></span>

<span data-ttu-id="8ff96-104">Évalue les fonctions de base de l’harmonique sphérique (SH) à partir d’un vecteur de direction d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8ff96-104">Evaluates the spherical harmonic (SH) basis functions from an input direction vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ff96-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ff96-105">Syntax</span></span>


```C++
FLOAT* D3DXSHEvalDirection(
  _In_       FLOAT       *pOut,
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a><span data-ttu-id="8ff96-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ff96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ff96-107">*moue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ff96-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff96-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ff96-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ff96-109">Pointeur vers les coefficients de sortie de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="8ff96-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="8ff96-110">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="8ff96-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="8ff96-111">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="8ff96-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8ff96-112">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ff96-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff96-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ff96-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ff96-114">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="8ff96-114">Order of the SH evaluation.</span></span> <span data-ttu-id="8ff96-115">La valeur doit être comprise entre D3DXSH \_ MINORDER et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="8ff96-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="8ff96-116">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="8ff96-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="8ff96-117">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="8ff96-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="8ff96-118">*pDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ff96-118">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff96-119">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ff96-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8ff96-120">(x, y, z) vecteur de direction dans lequel évaluer les fonctions de base SH.</span><span class="sxs-lookup"><span data-stu-id="8ff96-120">(x, y, z) direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="8ff96-121">Doit être normalisé.</span><span class="sxs-lookup"><span data-stu-id="8ff96-121">Must be normalized.</span></span> <span data-ttu-id="8ff96-122">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="8ff96-122">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ff96-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8ff96-123">Return value</span></span>

<span data-ttu-id="8ff96-124">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ff96-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ff96-125">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="8ff96-125">Pointer to SH output coefficients.</span></span> <span data-ttu-id="8ff96-126">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="8ff96-126">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ff96-127">Notes </span><span class="sxs-lookup"><span data-stu-id="8ff96-127">Remarks</span></span>

<span data-ttu-id="8ff96-128">Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :</span><span class="sxs-lookup"><span data-stu-id="8ff96-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="8ff96-129">l est le degré de la fonction de base.</span><span class="sxs-lookup"><span data-stu-id="8ff96-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="8ff96-130">m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.</span><span class="sxs-lookup"><span data-stu-id="8ff96-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

<span data-ttu-id="8ff96-131">Sur la sphère avec rayon d’unité, comme indiqué dans l’illustration suivante, la direction peut être spécifiée simplement avec thêta, l’angle autour de l’axe z dans la direction de droite, et Phi, l’angle de z.</span><span class="sxs-lookup"><span data-stu-id="8ff96-131">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![illustration d’une sphère avec rayon unitaire](images/spherical-coordinates.png)

<span data-ttu-id="8ff96-133">Les équations suivantes montrent la relation entre les coordonnées cartésiennes (x, y, z) et sphériques (thêta, Phi) sur la sphère d’unité.</span><span class="sxs-lookup"><span data-stu-id="8ff96-133">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="8ff96-134">Le thêta angulaire varie d’une plage de 0 à 2 pi, tandis que la valeur de Phi varie de 0 à pi.</span><span class="sxs-lookup"><span data-stu-id="8ff96-134">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![équations de la relation entre les coordonnées cartésiennes et sphériques](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="8ff96-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ff96-136">Requirements</span></span>



| <span data-ttu-id="8ff96-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ff96-137">Requirement</span></span> | <span data-ttu-id="8ff96-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ff96-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff96-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ff96-139">Header</span></span><br/>  | <dl> <span data-ttu-id="8ff96-140"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ff96-140"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ff96-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8ff96-141">Library</span></span><br/> | <dl> <span data-ttu-id="8ff96-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ff96-142"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ff96-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ff96-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ff96-144">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="8ff96-144">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
