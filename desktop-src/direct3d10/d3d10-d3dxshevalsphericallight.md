---
description: 'Fonction D3DXSHEvalSphericalLight (D3DX10. h) : évalue une lumière sphérique et retourne des données de l’harmonique sphérique spectral (SH).'
ms.assetid: e2a2b998-285a-46ef-99fe-ccc923013e9a
title: D3DXSHEvalSphericalLight, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalSphericalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1e509ea4695f143bd5399cbda004bcba53f514c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108557"
---
# <a name="d3dxshevalsphericallight-function-d3dx10h"></a><span data-ttu-id="5a8e2-103">D3DXSHEvalSphericalLight, fonction (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="5a8e2-103">D3DXSHEvalSphericalLight function (D3DX10.h)</span></span>

<span data-ttu-id="5a8e2-104">Évalue une lumière sphérique et retourne des données de l’harmonique sphérique spectral (SH).</span><span class="sxs-lookup"><span data-stu-id="5a8e2-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a8e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a8e2-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pPos,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="5a8e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a8e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a8e2-107">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a8e2-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a8e2-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a8e2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a8e2-109">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-109">Order of the SH evaluation.</span></span> <span data-ttu-id="5a8e2-110">La valeur doit être comprise entre D3DXSH \_ MINORDER et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="5a8e2-111">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="5a8e2-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="5a8e2-112">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="5a8e2-113">*pPos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a8e2-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a8e2-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a8e2-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5a8e2-115">Pointeur vers la position de la lumière.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="5a8e2-116">*Rayon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a8e2-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a8e2-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a8e2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a8e2-118">Rayon de la source de lumière sphérique.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="5a8e2-119">*RIntensity* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a8e2-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a8e2-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a8e2-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a8e2-121">Intensité rouge de la lumière.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="5a8e2-122">*GIntensity* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a8e2-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a8e2-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a8e2-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a8e2-124">Intensité verte de la lumière.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="5a8e2-125">*BIntensity* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a8e2-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a8e2-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a8e2-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a8e2-127">Intensité bleue de la lumière.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="5a8e2-128">*pROut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a8e2-128">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a8e2-129">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a8e2-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a8e2-130">Pointeur vers le vecteur de sortie SH pour le composant rouge.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="5a8e2-131">*pGOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a8e2-131">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a8e2-132">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a8e2-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a8e2-133">Pointeur vers le vecteur de sortie SH pour le composant vert.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="5a8e2-134">*pBOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a8e2-134">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a8e2-135">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a8e2-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a8e2-136">Pointeur vers le vecteur de sortie SH pour le composant bleu.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a8e2-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5a8e2-137">Return value</span></span>

<span data-ttu-id="5a8e2-138">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a8e2-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a8e2-139">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5a8e2-140">Si la fonction échoue, la valeur de retour peut être : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a8e2-141">Notes </span><span class="sxs-lookup"><span data-stu-id="5a8e2-141">Remarks</span></span>

<span data-ttu-id="5a8e2-142">Évalue une lumière sphérique et retourne des données SH spectrales.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="5a8e2-143">Il n’y a aucune normalisation de l’intensité de la lumière comme c’est le cas pour les lumières directionnelles. vous devez donc veiller à spécifier les inintensités.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-143">There is no normalization of the intensity of the light like there is for directional lights, so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="5a8e2-144">Cela permet de calculer trois échantillons spectraux. pROut est retourné, tandis que pGOut et pBOut peuvent être retournés.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-144">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="5a8e2-145">Sur la sphère avec rayon d’unité, comme indiqué dans l’illustration suivante, la direction peut être spécifiée simplement avec thêta, l’angle autour de l’axe z dans la direction de droite, et Phi, l’angle de z.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![illustration d’une sphère avec rayon unitaire](images/spherical-coordinates.png)

<span data-ttu-id="5a8e2-147">Les équations suivantes montrent la relation entre les coordonnées cartésiennes (x, y, z) et sphériques (thêta, Phi) sur la sphère d’unité.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="5a8e2-148">Le thêta angulaire varie d’une plage de 0 à 2 pi, tandis que la valeur de Phi varie de 0 à pi.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![équations de la relation entre les coordonnées cartésiennes et sphériques](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="5a8e2-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a8e2-150">Requirements</span></span>



| <span data-ttu-id="5a8e2-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a8e2-151">Requirement</span></span> | <span data-ttu-id="5a8e2-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a8e2-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a8e2-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a8e2-153">Header</span></span><br/>  | <dl> <span data-ttu-id="5a8e2-154"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a8e2-154"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a8e2-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a8e2-155">Library</span></span><br/> | <dl> <span data-ttu-id="5a8e2-156"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a8e2-156"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a8e2-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a8e2-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a8e2-158">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="5a8e2-158">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
