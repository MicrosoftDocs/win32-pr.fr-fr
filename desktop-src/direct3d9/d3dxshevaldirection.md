---
description: Évalue les fonctions de base de l’harmonique sphérique (SH) à partir d’un vecteur de direction d’entrée.
ms.assetid: f30ba32c-d6b0-4e4e-b5cd-839ed7821855
title: D3DXSHEvalDirection, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 005785667d25888550dea38c765a96ea56646d76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104567764"
---
# <a name="d3dxshevaldirection-function-d3dx9mathh"></a><span data-ttu-id="0efd1-103">D3DXSHEvalDirection, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0efd1-103">D3DXSHEvalDirection function (D3dx9math.h)</span></span>

<span data-ttu-id="0efd1-104">Évalue les fonctions de base de l’harmonique sphérique (SH) à partir d’un vecteur de direction d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0efd1-104">Evaluates the spherical harmonic (SH) basis functions from an input direction vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="0efd1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0efd1-105">Syntax</span></span>


```C++
FLOAT* D3DXSHEvalDirection(
  _Out_       FLOAT       *pOut,
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a><span data-ttu-id="0efd1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0efd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0efd1-107">*moue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0efd1-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0efd1-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0efd1-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0efd1-109">Pointeur vers les coefficients de sortie de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="0efd1-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="0efd1-110">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="0efd1-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="0efd1-111">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0efd1-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0efd1-112">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0efd1-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0efd1-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0efd1-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0efd1-114">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="0efd1-114">Order of the SH evaluation.</span></span> <span data-ttu-id="0efd1-115">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="0efd1-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="0efd1-116">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="0efd1-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="0efd1-117">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="0efd1-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="0efd1-118">*pDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0efd1-118">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0efd1-119">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0efd1-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0efd1-120">(x, y, z) vecteur de direction dans lequel évaluer les fonctions de base SH.</span><span class="sxs-lookup"><span data-stu-id="0efd1-120">(x, y, z) direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="0efd1-121">Doit être normalisé.</span><span class="sxs-lookup"><span data-stu-id="0efd1-121">Must be normalized.</span></span> <span data-ttu-id="0efd1-122">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0efd1-122">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0efd1-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0efd1-123">Return value</span></span>

<span data-ttu-id="0efd1-124">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0efd1-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0efd1-125">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="0efd1-125">Pointer to SH output coefficients.</span></span> <span data-ttu-id="0efd1-126">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0efd1-126">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="0efd1-127">Notes</span><span class="sxs-lookup"><span data-stu-id="0efd1-127">Remarks</span></span>

<span data-ttu-id="0efd1-128">Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :</span><span class="sxs-lookup"><span data-stu-id="0efd1-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="0efd1-129">l est le degré de la fonction de base.</span><span class="sxs-lookup"><span data-stu-id="0efd1-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="0efd1-130">m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.</span><span class="sxs-lookup"><span data-stu-id="0efd1-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

<span data-ttu-id="0efd1-131">Sur la sphère avec rayon d’unité, comme indiqué dans l’illustration suivante, la direction peut être spécifiée simplement avec thêta, l’angle autour de l’axe z dans la [direction de droite](coordinate-systems.md), et Phi, l’angle de z.</span><span class="sxs-lookup"><span data-stu-id="0efd1-131">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![illustration d’une sphère avec rayon unitaire](images/spherical-coordinates.png)

<span data-ttu-id="0efd1-133">Les équations suivantes montrent la relation entre les coordonnées cartésiennes (x, y, z) et sphériques (thêta, Phi) sur la sphère d’unité.</span><span class="sxs-lookup"><span data-stu-id="0efd1-133">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="0efd1-134">Le thêta angulaire varie d’une plage de 0 à 2 pi, tandis que la valeur de Phi varie de 0 à pi.</span><span class="sxs-lookup"><span data-stu-id="0efd1-134">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![équations de la relation entre les coordonnées cartésiennes et sphériques](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="0efd1-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0efd1-136">Requirements</span></span>



| <span data-ttu-id="0efd1-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0efd1-137">Requirement</span></span> | <span data-ttu-id="0efd1-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="0efd1-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0efd1-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="0efd1-139">Header</span></span><br/>  | <dl> <span data-ttu-id="0efd1-140"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0efd1-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0efd1-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0efd1-141">Library</span></span><br/> | <dl> <span data-ttu-id="0efd1-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0efd1-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0efd1-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0efd1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0efd1-144">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="0efd1-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0efd1-145">Transfert de luminance précalculé (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0efd1-145">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
