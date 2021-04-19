---
description: Définit les paramètres utilisés pour les calculs de frame tangent de maillage.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: Énumération D3DXTANGENT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 43e3c5ced0eee3366b85070ce89d19154d048ab4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522953"
---
# <a name="d3dxtangent-enumeration"></a><span data-ttu-id="f03f9-103">Énumération D3DXTANGENT</span><span class="sxs-lookup"><span data-stu-id="f03f9-103">D3DXTANGENT enumeration</span></span>

<span data-ttu-id="f03f9-104">Définit les paramètres utilisés pour les calculs de frame tangent de maillage.</span><span class="sxs-lookup"><span data-stu-id="f03f9-104">Defines settings used for mesh tangent frame computations.</span></span>

## <a name="syntax"></a><span data-ttu-id="f03f9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f03f9-105">Syntax</span></span>


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a><span data-ttu-id="f03f9-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="f03f9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f03f9-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ Wrap \_ U**</span><span class="sxs-lookup"><span data-stu-id="f03f9-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="f03f9-108">Les valeurs de coordonnée de texture de la direction u sont comprises entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="f03f9-108">Texture coordinate values in the u direction are between 0 and 1.</span></span> <span data-ttu-id="f03f9-109">Dans ce cas, un jeu de coordonnées de texture est choisi pour réduire le périmètre du triangle.</span><span class="sxs-lookup"><span data-stu-id="f03f9-109">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="f03f9-110">Consultez [habillage de texture (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="f03f9-110">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="f03f9-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ Wrap \_ V**</span><span class="sxs-lookup"><span data-stu-id="f03f9-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="f03f9-112">Les valeurs de coordonnée de texture dans la direction v sont comprises entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="f03f9-112">Texture coordinate values in the v direction are between 0 and 1.</span></span> <span data-ttu-id="f03f9-113">Dans ce cas, un jeu de coordonnées de texture est choisi pour réduire le périmètre du triangle.</span><span class="sxs-lookup"><span data-stu-id="f03f9-113">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="f03f9-114">Consultez [habillage de texture (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="f03f9-114">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="f03f9-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ enveloppe \_ UV**</span><span class="sxs-lookup"><span data-stu-id="f03f9-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="f03f9-116">Les valeurs de coordonnée de texture dans les directions v et v sont comprises entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="f03f9-116">Texture coordinate values in both u and v directions are between 0 and 1.</span></span> <span data-ttu-id="f03f9-117">Dans ce cas, un jeu de coordonnées de texture est choisi pour réduire le périmètre du triangle.</span><span class="sxs-lookup"><span data-stu-id="f03f9-117">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="f03f9-118">Consultez [habillage de texture (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="f03f9-118">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="f03f9-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ ne \_ normalisent pas les \_ partiels**</span><span class="sxs-lookup"><span data-stu-id="f03f9-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS**</span></span>
</dt> <dd>

<span data-ttu-id="f03f9-120">Ne normalisez pas les dérivées partielles en ce qui concerne les coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="f03f9-120">Do not normalize partial derivatives with respect to texture coordinates.</span></span> <span data-ttu-id="f03f9-121">Si elle n’est pas normalisée, l’échelle des dérivées partielles est proportionnelle à l’échelle du modèle 3D divisée par l’échelle du triangle dans l’espace (u, v).</span><span class="sxs-lookup"><span data-stu-id="f03f9-121">If not normalized, the scale of the partial derivatives is proportional to the scale of the 3D model divided by the scale of the triangle in (u, v) space.</span></span> <span data-ttu-id="f03f9-122">Cette valeur de mise à l’échelle fournit une mesure du degré d’étirement de la texture dans une direction donnée.</span><span class="sxs-lookup"><span data-stu-id="f03f9-122">This scale value provides a measure of how much the texture is stretched in a given direction.</span></span> <span data-ttu-id="f03f9-123">La longueur du vecteur résultant est une somme pondérée des longueurs des dérivées partielles.</span><span class="sxs-lookup"><span data-stu-id="f03f9-123">The resulting vector length is a weighted sum of the lengths of the partial derivatives.</span></span>

</dd> <dt>

<span data-ttu-id="f03f9-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT ne pas faire la \_ \_ orthogonalisation**</span><span class="sxs-lookup"><span data-stu-id="f03f9-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT\_DONT\_ORTHOGONALIZE**</span></span>
</dt> <dd>

<span data-ttu-id="f03f9-125">Ne transformez pas les coordonnées de texture en coordonnées cartésiennes orthogonales.</span><span class="sxs-lookup"><span data-stu-id="f03f9-125">Do not transform texture coordinates to orthogonal Cartesian coordinates.</span></span> <span data-ttu-id="f03f9-126">S’exclut mutuellement avec D3DXTANGENT \_ orthogonale \_ de \_ vous et D3DXTANGENT \_ orthogonale \_ de \_ V.</span><span class="sxs-lookup"><span data-stu-id="f03f9-126">Mutually exclusive with D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="f03f9-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT \_ orthogonaliser \_ à partir de \_ V**</span><span class="sxs-lookup"><span data-stu-id="f03f9-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V**</span></span>
</dt> <dd>

<span data-ttu-id="f03f9-128">Calculez la dérivée partielle par rapport à la coordonnée de texture v indépendamment pour chaque vertex, puis calculez la dérivée partielle par rapport à vous en tant que produit croisé de la dérivée partielle par rapport à v et au vecteur normal.</span><span class="sxs-lookup"><span data-stu-id="f03f9-128">Compute the partial derivative with respect to texture coordinate v independently for each vertex, and then compute the partial derivative with respect to u as the cross product of the partial derivative with respect to v and the normal vector.</span></span> <span data-ttu-id="f03f9-129">L’exception s’exclut mutuellement avec D3DXTANGENT \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f03f9-129">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U.</span></span>

</dd> <dt>

<span data-ttu-id="f03f9-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT \_ orthogonaliser \_ à partir de \_ U**</span><span class="sxs-lookup"><span data-stu-id="f03f9-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U**</span></span>
</dt> <dd>

<span data-ttu-id="f03f9-131">Calculez la dérivée partielle par rapport à la coordonnée de texture u indépendamment pour chaque vertex, puis calculez la dérivée partielle par rapport à v comme produit croisé du vecteur normal et du dérivé partiel par rapport à vous.</span><span class="sxs-lookup"><span data-stu-id="f03f9-131">Compute the partial derivative with respect to texture coordinate u independently for each vertex, and then compute the partial derivative with respect to v as the cross product of the normal vector and the partial derivative with respect to u.</span></span> <span data-ttu-id="f03f9-132">L’exception s’exclut mutuellement avec D3DXTANGENT \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f03f9-132">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="f03f9-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT \_ poids \_ par \_ zone**</span><span class="sxs-lookup"><span data-stu-id="f03f9-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT\_WEIGHT\_BY\_AREA**</span></span>
</dt> <dd>

<span data-ttu-id="f03f9-134">Pondérez la direction du vecteur de vecteurs normaux ou dérivés partiels calculé en fonction des zones de triangles attachées à ce vertex.</span><span class="sxs-lookup"><span data-stu-id="f03f9-134">Weight the direction of the computed per-vertex normal or partial derivative vector according to the areas of triangles attached to that vertex.</span></span> <span data-ttu-id="f03f9-135">S’exclut mutuellement avec le poids de D3DXTANGENT \_ \_ égal à.</span><span class="sxs-lookup"><span data-stu-id="f03f9-135">Mutually exclusive with D3DXTANGENT\_WEIGHT\_EQUAL.</span></span>

</dd> <dt>

<span data-ttu-id="f03f9-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**Poids de D3DXTANGENT \_ \_ égal à**</span><span class="sxs-lookup"><span data-stu-id="f03f9-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT\_WEIGHT\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="f03f9-137">Calculez un vecteur normal de longueur unitaire pour chaque triangle du maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f03f9-137">Compute a unit-length normal vector for each triangle of the input mesh.</span></span> <span data-ttu-id="f03f9-138">S’exclut mutuellement avec le \_ poids \_ de D3DXTANGENT par \_ zone.</span><span class="sxs-lookup"><span data-stu-id="f03f9-138">Mutually exclusive with D3DXTANGENT\_WEIGHT\_BY\_AREA.</span></span>

</dd> <dt>

<span data-ttu-id="f03f9-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ vent- \_ PV**</span><span class="sxs-lookup"><span data-stu-id="f03f9-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT\_WIND\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="f03f9-140">Les vertex sont classés dans le sens des aiguilles d’une montre autour de chaque triangle.</span><span class="sxs-lookup"><span data-stu-id="f03f9-140">Vertices are ordered in a clockwise direction around each triangle.</span></span> <span data-ttu-id="f03f9-141">La direction du vecteur normal calculé est donc inversée 180 degrés à partir de la direction calculée à l’aide du classement des sommets dans le sens inverse des aiguilles d’une passe.</span><span class="sxs-lookup"><span data-stu-id="f03f9-141">The computed normal vector direction is therefore inverted 180 degrees from the direction computed using counterclockwise vertex ordering.</span></span>

</dd> <dt>

<span data-ttu-id="f03f9-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ calculer les \_ normales**</span><span class="sxs-lookup"><span data-stu-id="f03f9-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT\_CALCULATE\_NORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="f03f9-143">Calcule le vecteur normal par vertex pour chaque triangle du maillage d’entrée et ignore tous les vecteurs normaux déjà présents dans le maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f03f9-143">Compute the per-vertex normal vector for each triangle of the input mesh, and ignore any normal vectors already in the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f03f9-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ Générer \_ sur \_ place**</span><span class="sxs-lookup"><span data-stu-id="f03f9-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT\_GENERATE\_IN\_PLACE**</span></span>
</dt> <dd>

<span data-ttu-id="f03f9-145">Les résultats sont stockés dans le maillage d’entrée d’origine et le maillage de sortie n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="f03f9-145">The results are stored in the original input mesh, and the output mesh is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f03f9-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f03f9-146">Requirements</span></span>



| <span data-ttu-id="f03f9-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f03f9-147">Requirement</span></span> | <span data-ttu-id="f03f9-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="f03f9-148">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f03f9-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="f03f9-149">Header</span></span><br/> | <dl> <span data-ttu-id="f03f9-150"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f03f9-150"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f03f9-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f03f9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f03f9-152">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="f03f9-152">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="f03f9-153">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="f03f9-153">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




