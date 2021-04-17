---
description: Évalue un éclairage directionnel et retourne les données d’harmonique sphérique spectral (SH).
ms.assetid: 6e2e9b02-13bb-4cef-ae9d-343fbf64e5d7
title: D3DXSHEvalDirectionalLight, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c78ee4059ed83b97e7ac1f392f857351df48ee7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104566576"
---
# <a name="d3dxshevaldirectionallight-function-d3dx9mathh"></a><span data-ttu-id="ae977-103">D3DXSHEvalDirectionalLight, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ae977-103">D3DXSHEvalDirectionalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="ae977-104">Évalue un [éclairage directionnel](light-types.md) et retourne les données d’harmonique sphérique spectral (SH).</span><span class="sxs-lookup"><span data-stu-id="ae977-104">Evaluates a [directional light](light-types.md) and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae977-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae977-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="ae977-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae977-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae977-107">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae977-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae977-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae977-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae977-109">Ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="ae977-109">Order of the SH evaluation.</span></span> <span data-ttu-id="ae977-110">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="ae977-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="ae977-111">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="ae977-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="ae977-112">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="ae977-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="ae977-113">*pDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae977-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae977-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ae977-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ae977-115">Pointeur vers le vecteur de direction de l’axe (x, y, z) de l’hémisphère dans lequel évaluer les fonctions de base SH.</span><span class="sxs-lookup"><span data-stu-id="ae977-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="ae977-116">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="ae977-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ae977-117">*RIntensity* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae977-117">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae977-118">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae977-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae977-119">Intensité rouge de la lumière.</span><span class="sxs-lookup"><span data-stu-id="ae977-119">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="ae977-120">*GIntensity* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae977-120">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae977-121">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae977-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae977-122">Intensité verte de la lumière.</span><span class="sxs-lookup"><span data-stu-id="ae977-122">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="ae977-123">*BIntensity* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae977-123">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae977-124">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae977-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae977-125">Intensité bleue de la lumière.</span><span class="sxs-lookup"><span data-stu-id="ae977-125">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="ae977-126">*pROut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae977-126">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae977-127">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ae977-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ae977-128">Pointeur vers le vecteur de sortie SH pour le composant rouge.</span><span class="sxs-lookup"><span data-stu-id="ae977-128">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="ae977-129">*pGOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae977-129">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae977-130">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ae977-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ae977-131">Pointeur facultatif vers le vecteur de sortie SH pour le composant vert.</span><span class="sxs-lookup"><span data-stu-id="ae977-131">Optional pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="ae977-132">*pBOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae977-132">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae977-133">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ae977-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ae977-134">Pointeur facultatif vers le vecteur de sortie SH pour le composant bleu.</span><span class="sxs-lookup"><span data-stu-id="ae977-134">Optional pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae977-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae977-135">Return value</span></span>

<span data-ttu-id="ae977-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae977-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae977-137">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ae977-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ae977-138">Si la fonction échoue, la valeur de retour peut être : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ae977-138">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae977-139">Notes</span><span class="sxs-lookup"><span data-stu-id="ae977-139">Remarks</span></span>

<span data-ttu-id="ae977-140">Le vecteur de sortie est calculé de sorte que si le rapport d’intensité R/G/B est égal à 1, le luminance de sortie résultant d’un point directement sous la lumière sur un objet diffus avec un albedo de 1 est 1,0.</span><span class="sxs-lookup"><span data-stu-id="ae977-140">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the resulting exit radiance of a point directly under the light on a diffuse object with an albedo of 1 would be 1.0.</span></span> <span data-ttu-id="ae977-141">Cela permet de calculer trois échantillons spectraux. *pROut* est retourné, tandis que *pGOut* et *pBOut* peuvent être retournés.</span><span class="sxs-lookup"><span data-stu-id="ae977-141">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="ae977-142">Sur la sphère avec rayon d’unité, comme indiqué dans l’illustration suivante, la direction peut être spécifiée simplement avec thêta, l’angle autour de l’axe z dans la [direction de droite](coordinate-systems.md), et Phi, l’angle de z.</span><span class="sxs-lookup"><span data-stu-id="ae977-142">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![illustration d’une sphère avec rayon unitaire](images/spherical-coordinates.png)

<span data-ttu-id="ae977-144">Les équations suivantes montrent la relation entre les coordonnées cartésiennes (x, y, z) et sphériques (thêta, Phi) sur la sphère d’unité.</span><span class="sxs-lookup"><span data-stu-id="ae977-144">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="ae977-145">Le thêta angulaire varie d’une plage de 0 à 2 pi, tandis que la valeur de Phi varie de 0 à pi.</span><span class="sxs-lookup"><span data-stu-id="ae977-145">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![équations de la relation entre les coordonnées cartésiennes et sphériques](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="ae977-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae977-147">Requirements</span></span>



| <span data-ttu-id="ae977-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae977-148">Requirement</span></span> | <span data-ttu-id="ae977-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae977-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae977-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae977-150">Header</span></span><br/>  | <dl> <span data-ttu-id="ae977-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae977-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ae977-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ae977-152">Library</span></span><br/> | <dl> <span data-ttu-id="ae977-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae977-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ae977-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae977-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae977-155">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="ae977-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ae977-156">Transfert de luminance précalculé (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ae977-156">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
