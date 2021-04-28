---
description: 'D3DXSHScale, fonction (D3dx9math. h) : met à l’échelle un vecteur d’harmonique sphérique (SH). en d’autres termes, moue \[ i \] = PA \[ i \] \* Scale.'
ms.assetid: e7b08b55-e2e7-4f13-bbee-10b844d3ef91
title: D3DXSHScale, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6a91c3ea1cb49c4c501ab847cb63fe8a39d66665
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093857"
---
# <a name="d3dxshscale-function-d3dx9mathh"></a><span data-ttu-id="9c634-103">D3DXSHScale, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9c634-103">D3DXSHScale function (D3dx9math.h)</span></span>

<span data-ttu-id="9c634-104">Met à l’échelle un vecteur d’harmonique sphérique (SH); en d’autres termes, moue \[ i \] = PA \[ i \] \* Scale.</span><span class="sxs-lookup"><span data-stu-id="9c634-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c634-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c634-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pIn,
  _In_  const FLOAT *Scale
);
```



## <a name="parameters"></a><span data-ttu-id="9c634-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c634-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c634-107">*moue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9c634-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c634-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c634-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9c634-109">Pointeur vers les coefficients de sortie de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="9c634-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="9c634-110">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="9c634-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="9c634-111">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="9c634-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9c634-112">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c634-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c634-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c634-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c634-114">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="9c634-114">Order of the SH evaluation.</span></span> <span data-ttu-id="9c634-115">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="9c634-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="9c634-116">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="9c634-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="9c634-117">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="9c634-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="9c634-118">*code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c634-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c634-119">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9c634-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9c634-120">Pointeur vers le vecteur SH à mettre à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="9c634-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="9c634-121">Mise à l' *échelle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c634-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c634-122">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9c634-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9c634-123">Pointeur désignant la valeur de l’échelle.</span><span class="sxs-lookup"><span data-stu-id="9c634-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c634-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9c634-124">Return value</span></span>

<span data-ttu-id="9c634-125">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c634-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9c634-126">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="9c634-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c634-127">Notes </span><span class="sxs-lookup"><span data-stu-id="9c634-127">Remarks</span></span>

<span data-ttu-id="9c634-128">Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :</span><span class="sxs-lookup"><span data-stu-id="9c634-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="9c634-129">l est le degré de la fonction de base.</span><span class="sxs-lookup"><span data-stu-id="9c634-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="9c634-130">m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.</span><span class="sxs-lookup"><span data-stu-id="9c634-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c634-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c634-131">Requirements</span></span>



| <span data-ttu-id="9c634-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c634-132">Requirement</span></span> | <span data-ttu-id="9c634-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c634-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c634-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c634-134">Header</span></span><br/>  | <dl> <span data-ttu-id="9c634-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c634-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9c634-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9c634-136">Library</span></span><br/> | <dl> <span data-ttu-id="9c634-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c634-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9c634-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c634-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c634-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="9c634-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9c634-140">Transfert de luminance précalculé (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9c634-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
