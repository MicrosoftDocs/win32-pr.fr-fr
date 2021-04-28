---
description: D3DXSHEvalConeLight fonction (D3DX10. h)-évalue une lumière qui est un cône d’intensité constante et retourne des données de l’harmonique sphérique spectral (SH).
ms.assetid: ad2b9c86-cf1a-426e-88e6-4c543519e002
title: D3DXSHEvalConeLight, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fc11e7bab4cbbd6c8a685b289d4bde476cd465ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108607"
---
# <a name="d3dxshevalconelight-function-d3dx10h"></a><span data-ttu-id="ccabd-103">D3DXSHEvalConeLight, fonction (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="ccabd-103">D3DXSHEvalConeLight function (D3DX10.h)</span></span>

<span data-ttu-id="ccabd-104">Évalue une lumière qui est un cône d’intensité constante et retourne des données d’harmonique sphérique spectral (SH).</span><span class="sxs-lookup"><span data-stu-id="ccabd-104">Evaluates a light that is a cone of constant intensity and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccabd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ccabd-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalConeLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="ccabd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ccabd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccabd-107">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccabd-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccabd-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccabd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccabd-109">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="ccabd-109">Order of the SH evaluation.</span></span> <span data-ttu-id="ccabd-110">La valeur doit être comprise entre D3DXSH \_ MINORDER et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="ccabd-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="ccabd-111">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="ccabd-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="ccabd-112">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="ccabd-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="ccabd-113">*pDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccabd-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccabd-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ccabd-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ccabd-115">Pointeur vers le vecteur de direction de l’axe (x, y, z) de l’hémisphère dans lequel évaluer les fonctions de base SH.</span><span class="sxs-lookup"><span data-stu-id="ccabd-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="ccabd-116">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="ccabd-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ccabd-117">*Rayon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccabd-117">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccabd-118">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccabd-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccabd-119">Rayon du cône en radians.</span><span class="sxs-lookup"><span data-stu-id="ccabd-119">Radius of cone in radians.</span></span>

</dd> <dt>

<span data-ttu-id="ccabd-120">*RIntensity* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccabd-120">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccabd-121">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccabd-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccabd-122">Intensité rouge de la lumière.</span><span class="sxs-lookup"><span data-stu-id="ccabd-122">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="ccabd-123">*GIntensity* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccabd-123">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccabd-124">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccabd-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccabd-125">Intensité verte de la lumière.</span><span class="sxs-lookup"><span data-stu-id="ccabd-125">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="ccabd-126">*BIntensity* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccabd-126">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccabd-127">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccabd-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccabd-128">Intensité bleue de la lumière.</span><span class="sxs-lookup"><span data-stu-id="ccabd-128">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="ccabd-129">*pROut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccabd-129">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccabd-130">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ccabd-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ccabd-131">Pointeur vers le vecteur de sortie SH pour le composant rouge.</span><span class="sxs-lookup"><span data-stu-id="ccabd-131">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="ccabd-132">*pGOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccabd-132">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccabd-133">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ccabd-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ccabd-134">Pointeur vers le vecteur de sortie SH pour le composant vert.</span><span class="sxs-lookup"><span data-stu-id="ccabd-134">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="ccabd-135">*pBOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccabd-135">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccabd-136">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ccabd-136">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ccabd-137">Pointeur vers le vecteur de sortie SH pour le composant bleu.</span><span class="sxs-lookup"><span data-stu-id="ccabd-137">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccabd-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ccabd-138">Return value</span></span>

<span data-ttu-id="ccabd-139">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ccabd-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ccabd-140">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ccabd-140">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ccabd-141">Si la fonction échoue, la valeur de retour peut être : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ccabd-141">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccabd-142">Notes </span><span class="sxs-lookup"><span data-stu-id="ccabd-142">Remarks</span></span>

<span data-ttu-id="ccabd-143">Évalue une lumière qui est un cône d’intensité constante et retourne des données SH spectrales.</span><span class="sxs-lookup"><span data-stu-id="ccabd-143">Evaluates a light that is a cone of constant intensity and returns spectral SH data.</span></span> <span data-ttu-id="ccabd-144">Le vecteur de sortie est calculé de sorte que si le rapport d’intensité R/G/B est égal à 1, le luminance de sortie d’un point situé directement sous la lumière (orienté dans la direction du cône sur un objet diffus avec un albedo de 1) est 1,0.</span><span class="sxs-lookup"><span data-stu-id="ccabd-144">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the exit radiance of a point directly under the light (oriented in the cone direction on a diffuse object with an albedo of 1) would be 1.0.</span></span> <span data-ttu-id="ccabd-145">Cela permet de calculer trois échantillons spectraux. pROut est retourné, tandis que pGOut et pBOut peuvent être retournés.</span><span class="sxs-lookup"><span data-stu-id="ccabd-145">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="ccabd-146">Sur la sphère avec rayon d’unité, comme indiqué dans l’illustration suivante, la direction peut être spécifiée simplement avec thêta, l’angle autour de l’axe z dans la direction de droite, et Phi, l’angle de z.</span><span class="sxs-lookup"><span data-stu-id="ccabd-146">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![illustration d’une sphère avec rayon unitaire](images/spherical-coordinates.png)

<span data-ttu-id="ccabd-148">Les équations suivantes montrent la relation entre les coordonnées cartésiennes (x, y, z) et sphériques (thêta, Phi) sur la sphère d’unité.</span><span class="sxs-lookup"><span data-stu-id="ccabd-148">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="ccabd-149">Le thêta angulaire varie d’une plage de 0 à 2 pi, tandis que la valeur de Phi varie de 0 à pi.</span><span class="sxs-lookup"><span data-stu-id="ccabd-149">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![équations de la relation entre les coordonnées cartésiennes et sphériques](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="ccabd-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ccabd-151">Requirements</span></span>



| <span data-ttu-id="ccabd-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccabd-152">Requirement</span></span> | <span data-ttu-id="ccabd-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccabd-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccabd-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="ccabd-154">Header</span></span><br/>  | <dl> <span data-ttu-id="ccabd-155"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccabd-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccabd-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ccabd-156">Library</span></span><br/> | <dl> <span data-ttu-id="ccabd-157"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccabd-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccabd-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccabd-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccabd-159">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="ccabd-159">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
