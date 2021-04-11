---
description: Ajoute deux vecteurs d’harmoniques sphériques (SH). en d’autres termes, moue \[ i \] = PA \[ i \] + PB \[ i \] .
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: D3DXSHAdd, fonction (D3DX10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1750b473764daf030160adc42d258a1f911f5f16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211899"
---
# <a name="d3dxshadd-function-d3dx10h"></a><span data-ttu-id="f2fa2-103">D3DXSHAdd, fonction (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="f2fa2-103">D3DXSHAdd function (D3DX10.h)</span></span>

<span data-ttu-id="f2fa2-104">Ajoute deux vecteurs d’harmoniques sphériques (SH). en d’autres termes, moue \[ i \] = PA \[ i \] + PB \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="f2fa2-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="f2fa2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2fa2-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="f2fa2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2fa2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2fa2-107">*moue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2fa2-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fa2-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2fa2-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f2fa2-109">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="f2fa2-110">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="f2fa2-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="f2fa2-111">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f2fa2-112">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2fa2-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fa2-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2fa2-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2fa2-114">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-114">Order of the SH evaluation.</span></span> <span data-ttu-id="f2fa2-115">La valeur doit être comprise entre D3DXSH \_ MINORDER et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="f2fa2-116">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="f2fa2-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="f2fa2-117">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="f2fa2-118">*PA* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2fa2-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fa2-119">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2fa2-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f2fa2-120">Pointeur vers le premier vecteur SH.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="f2fa2-121">*PB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2fa2-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fa2-122">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2fa2-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f2fa2-123">Pointeur vers le deuxième vecteur SH.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2fa2-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2fa2-124">Return value</span></span>

<span data-ttu-id="f2fa2-125">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2fa2-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f2fa2-126">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2fa2-127">Notes</span><span class="sxs-lookup"><span data-stu-id="f2fa2-127">Remarks</span></span>

<span data-ttu-id="f2fa2-128">Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :</span><span class="sxs-lookup"><span data-stu-id="f2fa2-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="f2fa2-129">l est le degré de la fonction de base.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="f2fa2-130">m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2fa2-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2fa2-131">Requirements</span></span>



| <span data-ttu-id="f2fa2-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2fa2-132">Requirement</span></span> | <span data-ttu-id="f2fa2-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2fa2-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2fa2-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2fa2-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f2fa2-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2fa2-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2fa2-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f2fa2-136">Library</span></span><br/> | <dl> <span data-ttu-id="f2fa2-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2fa2-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2fa2-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2fa2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2fa2-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="f2fa2-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
