---
description: 'Fonction D3DXSHDot (D3DX10. h) : calcule le produit scalaire de deux vecteurs d’harmoniques sphériques (SH).'
ms.assetid: 30f0e858-4c31-4b25-9979-754d996a7d48
title: D3DXSHDot, fonction (D3DX10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ea3e839ff7a5fc038cf40a6402db4a358da8b39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108627"
---
# <a name="d3dxshdot-function-d3dx10h"></a><span data-ttu-id="df12a-103">D3DXSHDot, fonction (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="df12a-103">D3DXSHDot function (D3DX10.h)</span></span>

<span data-ttu-id="df12a-104">Calcule le produit scalaire de deux vecteurs d’harmoniques sphériques (SH).</span><span class="sxs-lookup"><span data-stu-id="df12a-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="df12a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df12a-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="df12a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df12a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df12a-107">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df12a-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df12a-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df12a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df12a-109">Ordre de l’évaluation de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="df12a-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="df12a-110">La valeur doit être comprise entre D3DXSH \_ MINORDER et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="df12a-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="df12a-111">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="df12a-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="df12a-112">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="df12a-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="df12a-113">*PA* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df12a-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df12a-114">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="df12a-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="df12a-115">Pointeur vers le premier vecteur SH.</span><span class="sxs-lookup"><span data-stu-id="df12a-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="df12a-116">*PB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df12a-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df12a-117">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="df12a-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="df12a-118">Pointeur vers le deuxième vecteur SH.</span><span class="sxs-lookup"><span data-stu-id="df12a-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df12a-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="df12a-119">Return value</span></span>

<span data-ttu-id="df12a-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df12a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df12a-121">Résultats de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="df12a-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="df12a-122">Notes </span><span class="sxs-lookup"><span data-stu-id="df12a-122">Remarks</span></span>

<span data-ttu-id="df12a-123">Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :</span><span class="sxs-lookup"><span data-stu-id="df12a-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="df12a-124">l est le degré de la fonction de base.</span><span class="sxs-lookup"><span data-stu-id="df12a-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="df12a-125">m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.</span><span class="sxs-lookup"><span data-stu-id="df12a-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="df12a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df12a-126">Requirements</span></span>



| <span data-ttu-id="df12a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df12a-127">Requirement</span></span> | <span data-ttu-id="df12a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="df12a-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df12a-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="df12a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="df12a-130"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="df12a-130"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="df12a-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="df12a-131">Library</span></span><br/> | <dl> <span data-ttu-id="df12a-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df12a-132"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df12a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df12a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df12a-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="df12a-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
