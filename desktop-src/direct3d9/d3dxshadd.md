---
description: 'Fonction D3DXSHAdd (D3dx9math. h) : ajoute deux vecteurs d’harmoniques sphériques (SH). en d’autres termes, moue \[ i \] = PA \[ i \] + PB \[ i \] .'
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: D3DXSHAdd, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7333d1803b9f7ea7b056ff78ffd053bd6086184b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117957"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a><span data-ttu-id="d9ef0-103">D3DXSHAdd, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d9ef0-103">D3DXSHAdd function (D3dx9math.h)</span></span>

<span data-ttu-id="d9ef0-104">Ajoute deux vecteurs d’harmoniques sphériques (SH). en d’autres termes, moue \[ i \] = PA \[ i \] + PB \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="d9ef0-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="d9ef0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9ef0-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="d9ef0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9ef0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9ef0-107">*moue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d9ef0-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9ef0-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9ef0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d9ef0-109">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="d9ef0-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="d9ef0-110">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="d9ef0-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="d9ef0-111">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="d9ef0-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d9ef0-112">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d9ef0-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9ef0-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9ef0-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9ef0-114">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="d9ef0-114">Order of the SH evaluation.</span></span> <span data-ttu-id="d9ef0-115">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="d9ef0-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="d9ef0-116">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="d9ef0-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="d9ef0-117">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="d9ef0-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="d9ef0-118">*PA* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d9ef0-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9ef0-119">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d9ef0-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d9ef0-120">Pointeur vers le premier vecteur SH.</span><span class="sxs-lookup"><span data-stu-id="d9ef0-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="d9ef0-121">*PB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d9ef0-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9ef0-122">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d9ef0-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d9ef0-123">Pointeur vers le deuxième vecteur SH.</span><span class="sxs-lookup"><span data-stu-id="d9ef0-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9ef0-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d9ef0-124">Return value</span></span>

<span data-ttu-id="d9ef0-125">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9ef0-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d9ef0-126">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="d9ef0-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9ef0-127">Notes </span><span class="sxs-lookup"><span data-stu-id="d9ef0-127">Remarks</span></span>

<span data-ttu-id="d9ef0-128">Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :</span><span class="sxs-lookup"><span data-stu-id="d9ef0-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="d9ef0-129">l est le degré de la fonction de base.</span><span class="sxs-lookup"><span data-stu-id="d9ef0-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="d9ef0-130">m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.</span><span class="sxs-lookup"><span data-stu-id="d9ef0-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9ef0-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9ef0-131">Requirements</span></span>



| <span data-ttu-id="d9ef0-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9ef0-132">Requirement</span></span> | <span data-ttu-id="d9ef0-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9ef0-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9ef0-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9ef0-134">Header</span></span><br/>  | <dl> <span data-ttu-id="d9ef0-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9ef0-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d9ef0-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d9ef0-136">Library</span></span><br/> | <dl> <span data-ttu-id="d9ef0-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9ef0-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d9ef0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9ef0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9ef0-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="d9ef0-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d9ef0-140">Transfert de luminance précalculé (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9ef0-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
