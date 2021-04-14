---
description: Calcule le produit scalaire de deux vecteurs d’harmoniques sphériques (SH).
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: D3DXSHDot, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a69ee929c889232cb29ff1b556dd08ab65a0d6d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394119"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a><span data-ttu-id="37c3b-103">D3DXSHDot, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="37c3b-103">D3DXSHDot function (D3dx9math.h)</span></span>

<span data-ttu-id="37c3b-104">Calcule le produit scalaire de deux vecteurs d’harmoniques sphériques (SH).</span><span class="sxs-lookup"><span data-stu-id="37c3b-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="37c3b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37c3b-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="37c3b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37c3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37c3b-107">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37c3b-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37c3b-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37c3b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37c3b-109">Ordre de l’évaluation de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="37c3b-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="37c3b-110">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="37c3b-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="37c3b-111">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="37c3b-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="37c3b-112">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="37c3b-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="37c3b-113">*PA* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37c3b-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37c3b-114">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="37c3b-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="37c3b-115">Pointeur vers le premier vecteur SH.</span><span class="sxs-lookup"><span data-stu-id="37c3b-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="37c3b-116">*PB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37c3b-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37c3b-117">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="37c3b-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="37c3b-118">Pointeur vers le deuxième vecteur SH.</span><span class="sxs-lookup"><span data-stu-id="37c3b-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37c3b-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37c3b-119">Return value</span></span>

<span data-ttu-id="37c3b-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37c3b-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37c3b-121">Résultats de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="37c3b-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="37c3b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="37c3b-122">Remarks</span></span>

<span data-ttu-id="37c3b-123">Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :</span><span class="sxs-lookup"><span data-stu-id="37c3b-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="37c3b-124">l est le degré de la fonction de base.</span><span class="sxs-lookup"><span data-stu-id="37c3b-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="37c3b-125">m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.</span><span class="sxs-lookup"><span data-stu-id="37c3b-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="37c3b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37c3b-126">Requirements</span></span>



| <span data-ttu-id="37c3b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37c3b-127">Requirement</span></span> | <span data-ttu-id="37c3b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="37c3b-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37c3b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="37c3b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="37c3b-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="37c3b-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="37c3b-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="37c3b-131">Library</span></span><br/> | <dl> <span data-ttu-id="37c3b-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37c3b-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="37c3b-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37c3b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37c3b-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="37c3b-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="37c3b-135">Transfert de luminance précalculé (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="37c3b-135">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
