---
description: Fait pivoter le vecteur d’harmonique sphérique (SH) dans l’axe z selon l’angle donné.
ms.assetid: 1f471183-4c8e-4fa8-9a42-f6cc2bb1b0f2
title: D3DXSHRotateZ, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac13cff212aaabdd8a9586b88e3152779bcfaf85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394116"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a><span data-ttu-id="f57ef-103">D3DXSHRotateZ, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f57ef-103">D3DXSHRotateZ function (D3dx9math.h)</span></span>

<span data-ttu-id="f57ef-104">Fait pivoter le vecteur d’harmonique sphérique (SH) dans l’axe z selon l’angle donné.</span><span class="sxs-lookup"><span data-stu-id="f57ef-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="f57ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f57ef-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="f57ef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f57ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f57ef-107">*moue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f57ef-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f57ef-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f57ef-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f57ef-109">Pointeur vers les coefficients de sortie de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="f57ef-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="f57ef-110">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="f57ef-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="f57ef-111">Ce pointeur ne doit pas être un alias avec *pin*.</span><span class="sxs-lookup"><span data-stu-id="f57ef-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="f57ef-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="f57ef-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f57ef-113">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f57ef-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f57ef-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f57ef-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f57ef-115">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="f57ef-115">Order of the SH evaluation.</span></span> <span data-ttu-id="f57ef-116">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="f57ef-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="f57ef-117">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="f57ef-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="f57ef-118">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="f57ef-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="f57ef-119">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f57ef-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f57ef-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f57ef-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f57ef-121">Angle de rotation en radians.</span><span class="sxs-lookup"><span data-stu-id="f57ef-121">Rotation angle in radians.</span></span> <span data-ttu-id="f57ef-122">La rotation est effectuée autour de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="f57ef-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="f57ef-123">*code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f57ef-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f57ef-124">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f57ef-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f57ef-125">Pointeur vers les coefficients SH pivotés.</span><span class="sxs-lookup"><span data-stu-id="f57ef-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f57ef-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f57ef-126">Return value</span></span>

<span data-ttu-id="f57ef-127">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f57ef-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f57ef-128">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="f57ef-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="f57ef-129">Notes</span><span class="sxs-lookup"><span data-stu-id="f57ef-129">Remarks</span></span>

<span data-ttu-id="f57ef-130">Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :</span><span class="sxs-lookup"><span data-stu-id="f57ef-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="f57ef-131">l est le degré de la fonction de base.</span><span class="sxs-lookup"><span data-stu-id="f57ef-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="f57ef-132">m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.</span><span class="sxs-lookup"><span data-stu-id="f57ef-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="f57ef-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f57ef-133">Requirements</span></span>



| <span data-ttu-id="f57ef-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f57ef-134">Requirement</span></span> | <span data-ttu-id="f57ef-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="f57ef-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f57ef-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="f57ef-136">Header</span></span><br/>  | <dl> <span data-ttu-id="f57ef-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f57ef-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f57ef-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f57ef-138">Library</span></span><br/> | <dl> <span data-ttu-id="f57ef-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f57ef-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f57ef-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f57ef-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f57ef-141">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="f57ef-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f57ef-142">Transfert de luminance précalculé (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f57ef-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
