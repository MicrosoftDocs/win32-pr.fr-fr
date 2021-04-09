---
description: Fait pivoter le vecteur d’harmonique sphérique (SH) dans l’axe z selon l’angle donné.
ms.assetid: 7c4bec55-4a4c-4f7e-8849-1cac373a2340
title: D3DXSHRotateZ, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0348dd8dfed9b100f64c53427ca2b77dd48ccded
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953926"
---
# <a name="d3dxshrotatez-function-d3dx10h"></a><span data-ttu-id="6641c-103">D3DXSHRotateZ, fonction (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="6641c-103">D3DXSHRotateZ function (D3DX10.h)</span></span>

<span data-ttu-id="6641c-104">Fait pivoter le vecteur d’harmonique sphérique (SH) dans l’axe z selon l’angle donné.</span><span class="sxs-lookup"><span data-stu-id="6641c-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="6641c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6641c-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_       FLOAT Angle,
  _In_ const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="6641c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6641c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6641c-107">*moue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6641c-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6641c-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6641c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6641c-109">Pointeur vers les coefficients de sortie de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="6641c-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="6641c-110">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="6641c-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="6641c-111">Ce pointeur ne doit pas être un alias avec pIn.</span><span class="sxs-lookup"><span data-stu-id="6641c-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="6641c-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="6641c-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6641c-113">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6641c-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6641c-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6641c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6641c-115">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="6641c-115">Order of the SH evaluation.</span></span> <span data-ttu-id="6641c-116">La valeur doit être comprise entre D3DXSH \_ MINORDER et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="6641c-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="6641c-117">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="6641c-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="6641c-118">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="6641c-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="6641c-119">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6641c-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6641c-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6641c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6641c-121">Angle de rotation en radians.</span><span class="sxs-lookup"><span data-stu-id="6641c-121">Rotation angle in radians.</span></span> <span data-ttu-id="6641c-122">La rotation est effectuée autour de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="6641c-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="6641c-123">*code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6641c-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6641c-124">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6641c-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6641c-125">Pointeur vers les coefficients SH pivotés.</span><span class="sxs-lookup"><span data-stu-id="6641c-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6641c-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6641c-126">Return value</span></span>

<span data-ttu-id="6641c-127">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6641c-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6641c-128">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="6641c-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="6641c-129">Notes</span><span class="sxs-lookup"><span data-stu-id="6641c-129">Remarks</span></span>

<span data-ttu-id="6641c-130">Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :</span><span class="sxs-lookup"><span data-stu-id="6641c-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="6641c-131">l est le degré de la fonction de base.</span><span class="sxs-lookup"><span data-stu-id="6641c-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="6641c-132">m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.</span><span class="sxs-lookup"><span data-stu-id="6641c-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="6641c-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6641c-133">Requirements</span></span>



| <span data-ttu-id="6641c-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6641c-134">Requirement</span></span> | <span data-ttu-id="6641c-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="6641c-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6641c-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="6641c-136">Header</span></span><br/>  | <dl> <span data-ttu-id="6641c-137"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6641c-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6641c-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6641c-138">Library</span></span><br/> | <dl> <span data-ttu-id="6641c-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6641c-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6641c-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6641c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6641c-141">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="6641c-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
