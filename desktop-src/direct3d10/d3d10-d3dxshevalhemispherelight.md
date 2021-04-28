---
description: Fonction D3DXSHEvalHemisphereLight (D3DX10. h)-évalue une lumière qui est une interpolation linéaire entre deux couleurs sur la sphère.
ms.assetid: 7523ff42-c81d-4857-a50d-7efa213214b8
title: D3DXSHEvalHemisphereLight, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 355dae7b843d5acfbb842b7bd08c329bdaed4306
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108567"
---
# <a name="d3dxshevalhemispherelight-function-d3dx10h"></a><span data-ttu-id="bb4ac-103">D3DXSHEvalHemisphereLight, fonction (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="bb4ac-103">D3DXSHEvalHemisphereLight function (D3DX10.h)</span></span>

<span data-ttu-id="bb4ac-104">Évalue une lumière qui est une interpolation linéaire entre deux couleurs sur la sphère.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-104">Evaluates a light that is a linear interpolation between two colors over the sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb4ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb4ac-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="bb4ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb4ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb4ac-107">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb4ac-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb4ac-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb4ac-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb4ac-109">Ordre de l’évaluation de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="bb4ac-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="bb4ac-110">La valeur doit être comprise entre D3DXSH \_ MINORDER et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="bb4ac-111">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="bb4ac-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="bb4ac-112">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="bb4ac-113">*pDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb4ac-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb4ac-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb4ac-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bb4ac-115">Pointeur vers le vecteur de direction de l’axe (x, y, z) de l’hémisphère dans lequel évaluer les fonctions de base SH.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="bb4ac-116">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="bb4ac-117">En *haut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb4ac-117">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb4ac-118">Type : **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="bb4ac-118">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="bb4ac-119">Couleur du ciel.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-119">The sky color.</span></span>

</dd> <dt>

<span data-ttu-id="bb4ac-120">En *bas* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb4ac-120">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb4ac-121">Type : **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="bb4ac-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="bb4ac-122">Couleur de fond.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-122">The ground color.</span></span>

</dd> <dt>

<span data-ttu-id="bb4ac-123">*pROut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb4ac-123">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb4ac-124">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb4ac-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bb4ac-125">Pointeur vers le vecteur de sortie SH pour le composant rouge.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-125">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="bb4ac-126">*pGOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb4ac-126">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb4ac-127">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb4ac-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bb4ac-128">Pointeur vers le vecteur de sortie SH pour le composant vert.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-128">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="bb4ac-129">*pBOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb4ac-129">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb4ac-130">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb4ac-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bb4ac-131">Pointeur vers le vecteur de sortie SH pour le composant bleu.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-131">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb4ac-132">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bb4ac-132">Return value</span></span>

<span data-ttu-id="bb4ac-133">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb4ac-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb4ac-134">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bb4ac-135">Si la fonction échoue, la valeur de retour peut être : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-135">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb4ac-136">Notes </span><span class="sxs-lookup"><span data-stu-id="bb4ac-136">Remarks</span></span>

<span data-ttu-id="bb4ac-137">L’interpolation est effectuée de façon linéaire entre les deux points, et non pas sur la surface de la sphère (autrement dit, si l’axe était (0, 0, 1) elle est linéaire en Z, et non pas dans l’angle de l’azimut).</span><span class="sxs-lookup"><span data-stu-id="bb4ac-137">The interpolation is done linearly between the two points, not over the surface of the sphere (that is, if the axis was (0,0,1) it is linear in Z, not in the azimuthal angle).</span></span> <span data-ttu-id="bb4ac-138">La fonction d’éclairage sphérique qui en résulte est normalisée, de sorte qu’un point sur une surface parfaitement diffuse sans occultation et un point perpendiculaire dans la direction pDir entraînerait la sortie de luminance avec une valeur de 1 (si la couleur supérieure était blanche et la couleur inférieure était noire).</span><span class="sxs-lookup"><span data-stu-id="bb4ac-138">The resulting spherical lighting function is normalized so that a point on a perfectly diffuse surface with no shadowing and a normal pointed in the direction pDir would result in exit radiance with a value of 1 (if the top color was white and the bottom color was black).</span></span> <span data-ttu-id="bb4ac-139">Il s’agit d’un modèle très simple où Top représente l’intensité de « Sky » et Bottom représente l’intensité du « Ground ».</span><span class="sxs-lookup"><span data-stu-id="bb4ac-139">This is a very simple model where Top represents the intensity of the "sky" and Bottom represents the intensity of the "ground."</span></span>

<span data-ttu-id="bb4ac-140">Sur la sphère avec rayon d’unité, comme indiqué dans l’illustration suivante, la direction peut être spécifiée simplement avec thêta, l’angle autour de l’axe z dans la direction de droite, et Phi, l’angle de z.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-140">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![illustration d’une sphère avec rayon unitaire](images/spherical-coordinates.png)

<span data-ttu-id="bb4ac-142">Les équations suivantes montrent la relation entre les coordonnées cartésiennes (x, y, z) et sphériques (thêta, Phi) sur la sphère d’unité.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-142">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="bb4ac-143">Le thêta angulaire varie d’une plage de 0 à 2 pi, tandis que la valeur de Phi varie de 0 à pi.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-143">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![équations de la relation entre les coordonnées cartésiennes et sphériques](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="bb4ac-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb4ac-145">Requirements</span></span>



| <span data-ttu-id="bb4ac-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb4ac-146">Requirement</span></span> | <span data-ttu-id="bb4ac-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb4ac-147">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb4ac-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb4ac-148">Header</span></span><br/>  | <dl> <span data-ttu-id="bb4ac-149"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb4ac-149"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb4ac-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb4ac-150">Library</span></span><br/> | <dl> <span data-ttu-id="bb4ac-151"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb4ac-151"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb4ac-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb4ac-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb4ac-153">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="bb4ac-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
