---
description: 'Fonction D3DXSHRotateZ (D3dx9math. h) : fait pivoter le vecteur d’harmonique sphérique (SH) dans l’axe z selon l’angle donné.'
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
ms.openlocfilehash: ed7db57dc3acedd1e65edab7377b525940ea10e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117847"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a><span data-ttu-id="b4eca-103">D3DXSHRotateZ, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b4eca-103">D3DXSHRotateZ function (D3dx9math.h)</span></span>

<span data-ttu-id="b4eca-104">Fait pivoter le vecteur d’harmonique sphérique (SH) dans l’axe z selon l’angle donné.</span><span class="sxs-lookup"><span data-stu-id="b4eca-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4eca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4eca-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="b4eca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4eca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4eca-107">*moue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b4eca-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4eca-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b4eca-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b4eca-109">Pointeur vers les coefficients de sortie de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="b4eca-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="b4eca-110">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="b4eca-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="b4eca-111">Ce pointeur ne doit pas être un alias avec *pin*.</span><span class="sxs-lookup"><span data-stu-id="b4eca-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="b4eca-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="b4eca-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b4eca-113">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4eca-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4eca-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4eca-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4eca-115">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="b4eca-115">Order of the SH evaluation.</span></span> <span data-ttu-id="b4eca-116">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="b4eca-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="b4eca-117">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="b4eca-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="b4eca-118">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="b4eca-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="b4eca-119">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4eca-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4eca-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4eca-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4eca-121">Angle de rotation en radians.</span><span class="sxs-lookup"><span data-stu-id="b4eca-121">Rotation angle in radians.</span></span> <span data-ttu-id="b4eca-122">La rotation est effectuée autour de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="b4eca-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="b4eca-123">*code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4eca-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4eca-124">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b4eca-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b4eca-125">Pointeur vers les coefficients SH pivotés.</span><span class="sxs-lookup"><span data-stu-id="b4eca-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4eca-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4eca-126">Return value</span></span>

<span data-ttu-id="b4eca-127">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b4eca-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b4eca-128">Pointeur vers les coefficients de sortie SH.</span><span class="sxs-lookup"><span data-stu-id="b4eca-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4eca-129">Notes </span><span class="sxs-lookup"><span data-stu-id="b4eca-129">Remarks</span></span>

<span data-ttu-id="b4eca-130">Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :</span><span class="sxs-lookup"><span data-stu-id="b4eca-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="b4eca-131">l est le degré de la fonction de base.</span><span class="sxs-lookup"><span data-stu-id="b4eca-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="b4eca-132">m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.</span><span class="sxs-lookup"><span data-stu-id="b4eca-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4eca-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4eca-133">Requirements</span></span>



| <span data-ttu-id="b4eca-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4eca-134">Requirement</span></span> | <span data-ttu-id="b4eca-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4eca-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4eca-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4eca-136">Header</span></span><br/>  | <dl> <span data-ttu-id="b4eca-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4eca-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b4eca-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b4eca-138">Library</span></span><br/> | <dl> <span data-ttu-id="b4eca-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4eca-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b4eca-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4eca-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4eca-141">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="b4eca-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b4eca-142">Transfert de luminance précalculé (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4eca-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
