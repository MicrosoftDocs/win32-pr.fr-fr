---
description: Fonction D3DXSHEvalDirectionalLight (D3DX10. h)-évalue un éclairage directionnel et retourne les données spectrales sphériques spectrales.
ms.assetid: b5c657f5-d291-4e53-908c-670b29a1888a
title: D3DXSHEvalDirectionalLight, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirectionalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 551dad8081af2b0138be4758682d5a660f621141
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108597"
---
# <a name="d3dxshevaldirectionallight-function-d3dx10h"></a><span data-ttu-id="fef43-103">D3DXSHEvalDirectionalLight, fonction (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="fef43-103">D3DXSHEvalDirectionalLight function (D3DX10.h)</span></span>

<span data-ttu-id="fef43-104">Évalue un éclairage directionnel et retourne les données d’harmonique sphérique spectral (SH).</span><span class="sxs-lookup"><span data-stu-id="fef43-104">Evaluates a directional light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef43-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fef43-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="fef43-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fef43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fef43-107">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fef43-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fef43-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fef43-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fef43-109">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="fef43-109">Order of the SH evaluation.</span></span> <span data-ttu-id="fef43-110">La valeur doit être comprise entre D3DXSH \_ MINORDER et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="fef43-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="fef43-111">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="fef43-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="fef43-112">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="fef43-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="fef43-113">*pDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fef43-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fef43-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fef43-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fef43-115">Pointeur vers le vecteur de direction de l’axe (x, y, z) de l’hémisphère dans lequel évaluer les fonctions de base SH.</span><span class="sxs-lookup"><span data-stu-id="fef43-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="fef43-116">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="fef43-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fef43-117">*RIntensity* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fef43-117">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fef43-118">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fef43-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fef43-119">Intensité rouge de la lumière.</span><span class="sxs-lookup"><span data-stu-id="fef43-119">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="fef43-120">*GIntensity* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fef43-120">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fef43-121">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fef43-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fef43-122">Intensité verte de la lumière.</span><span class="sxs-lookup"><span data-stu-id="fef43-122">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="fef43-123">*BIntensity* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fef43-123">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fef43-124">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fef43-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fef43-125">Intensité bleue de la lumière.</span><span class="sxs-lookup"><span data-stu-id="fef43-125">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="fef43-126">*pROut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fef43-126">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fef43-127">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fef43-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fef43-128">Pointeur vers le vecteur de sortie SH pour le composant rouge.</span><span class="sxs-lookup"><span data-stu-id="fef43-128">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="fef43-129">*pGOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fef43-129">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fef43-130">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fef43-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fef43-131">Pointeur facultatif vers le vecteur de sortie SH pour le composant vert.</span><span class="sxs-lookup"><span data-stu-id="fef43-131">Optional pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="fef43-132">*pBOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fef43-132">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fef43-133">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fef43-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fef43-134">Pointeur facultatif vers le vecteur de sortie SH pour le composant bleu.</span><span class="sxs-lookup"><span data-stu-id="fef43-134">Optional pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fef43-135">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fef43-135">Return value</span></span>

<span data-ttu-id="fef43-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fef43-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fef43-137">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fef43-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fef43-138">Si la fonction échoue, la valeur de retour peut être : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fef43-138">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fef43-139">Notes </span><span class="sxs-lookup"><span data-stu-id="fef43-139">Remarks</span></span>

<span data-ttu-id="fef43-140">Le vecteur de sortie est calculé de sorte que si le rapport d’intensité R/G/B est égal à 1, le luminance de sortie résultant d’un point directement sous la lumière sur un objet diffus avec un albedo de 1 est 1,0.</span><span class="sxs-lookup"><span data-stu-id="fef43-140">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the resulting exit radiance of a point directly under the light on a diffuse object with an albedo of 1 would be 1.0.</span></span> <span data-ttu-id="fef43-141">Cela permet de calculer trois échantillons spectraux. pROut est retourné, tandis que pGOut et pBOut peuvent être retournés.</span><span class="sxs-lookup"><span data-stu-id="fef43-141">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="fef43-142">Sur la sphère avec rayon d’unité, comme indiqué dans l’illustration suivante, la direction peut être spécifiée simplement avec thêta, l’angle autour de l’axe z dans la direction de droite, et Phi, l’angle de z.</span><span class="sxs-lookup"><span data-stu-id="fef43-142">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![illustration d’une sphère avec rayon unitaire](images/spherical-coordinates.png)

<span data-ttu-id="fef43-144">Les équations suivantes montrent la relation entre les coordonnées cartésiennes (x, y, z) et sphériques (thêta, Phi) sur la sphère d’unité.</span><span class="sxs-lookup"><span data-stu-id="fef43-144">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="fef43-145">Le thêta angulaire varie d’une plage de 0 à 2 pi, tandis que la valeur de Phi varie de 0 à pi.</span><span class="sxs-lookup"><span data-stu-id="fef43-145">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![équations de la relation entre les coordonnées cartésiennes et sphériques](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="fef43-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fef43-147">Requirements</span></span>



| <span data-ttu-id="fef43-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fef43-148">Requirement</span></span> | <span data-ttu-id="fef43-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="fef43-149">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fef43-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="fef43-150">Header</span></span><br/>  | <dl> <span data-ttu-id="fef43-151"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="fef43-151"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="fef43-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fef43-152">Library</span></span><br/> | <dl> <span data-ttu-id="fef43-153"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fef43-153"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fef43-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fef43-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fef43-155">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="fef43-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
