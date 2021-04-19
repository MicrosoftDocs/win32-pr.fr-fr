---
description: Identifie l’utilisation prévue des données de vertex.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: Énumération D3DDECLUSAGE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f3997aa38a7a97455b9f36d8afbee896ca9ae937
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545271"
---
# <a name="d3ddeclusage-enumeration"></a><span data-ttu-id="9a074-103">Énumération D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="9a074-103">D3DDECLUSAGE enumeration</span></span>

<span data-ttu-id="9a074-104">Identifie l’utilisation prévue des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="9a074-104">Identifies the intended use of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a074-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a074-105">Syntax</span></span>


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a><span data-ttu-id="9a074-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="9a074-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9a074-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**\_Position D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="9a074-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGE\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-108">Placez les données entre (-1,-1) et (1, 1).</span><span class="sxs-lookup"><span data-stu-id="9a074-108">Position data ranging from (-1,-1) to (1,1).</span></span> <span data-ttu-id="9a074-109">Utilisez \_ la position D3DDECLUSAGE avec un index d’utilisation de 0 pour spécifier une position non transformée pour le traitement de vertex de fonction fixe et le du paveur n-patch.</span><span class="sxs-lookup"><span data-stu-id="9a074-109">Use D3DDECLUSAGE\_POSITION with a usage index of 0 to specify untransformed position for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="9a074-110">Utilisez \_ la position D3DDECLUSAGE avec un index d’utilisation de 1 pour spécifier la position non transformée dans le nuanceur de sommets de fonction fixe pour l’interpolation de vertex.</span><span class="sxs-lookup"><span data-stu-id="9a074-110">Use D3DDECLUSAGE\_POSITION with a usage index of 1 to specify untransformed position in the fixed function vertex shader for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="9a074-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ BLENDWEIGHT**</span><span class="sxs-lookup"><span data-stu-id="9a074-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE\_BLENDWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-112">Fusion des données de poids.</span><span class="sxs-lookup"><span data-stu-id="9a074-112">Blending weight data.</span></span> <span data-ttu-id="9a074-113">Utilisez D3DDECLUSAGE \_ BLENDWEIGHT avec un index d’utilisation de 0 pour spécifier les pondérations de fusion utilisées dans la fusion de vertex indexée et non indexée.</span><span class="sxs-lookup"><span data-stu-id="9a074-113">Use D3DDECLUSAGE\_BLENDWEIGHT with a usage index of 0 to specify the blend weights used in indexed and nonindexed vertex blending.</span></span>

</dd> <dt>

<span data-ttu-id="9a074-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ BLENDINDICES**</span><span class="sxs-lookup"><span data-stu-id="9a074-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE\_BLENDINDICES**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-115">Fusion des données d’index.</span><span class="sxs-lookup"><span data-stu-id="9a074-115">Blending indices data.</span></span> <span data-ttu-id="9a074-116">Utilisez D3DDECLUSAGE \_ BLENDINDICES avec un index d’utilisation de 0 pour spécifier des index de matrice pour les pelures de palette indexées.</span><span class="sxs-lookup"><span data-stu-id="9a074-116">Use D3DDECLUSAGE\_BLENDINDICES with a usage index of 0 to specify matrix indices for indexed paletted skinning.</span></span>

</dd> <dt>

<span data-ttu-id="9a074-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ normal**</span><span class="sxs-lookup"><span data-stu-id="9a074-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-118">Données normales au vertex.</span><span class="sxs-lookup"><span data-stu-id="9a074-118">Vertex normal data.</span></span> <span data-ttu-id="9a074-119">Utilisez D3DDECLUSAGE \_ normal avec un index d’utilisation égal à 0 pour spécifier les normales aux sommets pour le traitement des vertex de fonction fixe et le du paveur n-patch.</span><span class="sxs-lookup"><span data-stu-id="9a074-119">Use D3DDECLUSAGE\_NORMAL with a usage index of 0 to specify vertex normals for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="9a074-120">Utilisez D3DDECLUSAGE \_ normal avec un index d’utilisation de 1 pour spécifier les normales aux sommets pour le traitement des vertex de fonction fixe pour l’interpolation de vertex.</span><span class="sxs-lookup"><span data-stu-id="9a074-120">Use D3DDECLUSAGE\_NORMAL with a usage index of 1 to specify vertex normals for fixed function vertex processing for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="9a074-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ psize**</span><span class="sxs-lookup"><span data-stu-id="9a074-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE\_PSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-122">Données de taille en points.</span><span class="sxs-lookup"><span data-stu-id="9a074-122">Point size data.</span></span> <span data-ttu-id="9a074-123">Utilisez D3DDECLUSAGE \_ psize avec un index d’utilisation de 0 pour spécifier l’attribut de taille de point utilisé par le moteur d’installation du rastériseur pour étendre un point à un quadruple pour la fonctionnalité point-Sprite.</span><span class="sxs-lookup"><span data-stu-id="9a074-123">Use D3DDECLUSAGE\_PSIZE with a usage index of 0 to specify the point-size attribute used by the setup engine of the rasterizer to expand a point into a quad for the point-sprite functionality.</span></span>

</dd> <dt>

<span data-ttu-id="9a074-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ texcoord**</span><span class="sxs-lookup"><span data-stu-id="9a074-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE\_TEXCOORD**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-125">Données de coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="9a074-125">Texture coordinate data.</span></span> <span data-ttu-id="9a074-126">Utilisez D3DDECLUSAGE \_ texcoord, n pour spécifier des coordonnées de texture dans le traitement du vertex de fonction fixe et dans les nuanceurs de pixels antérieurs à PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="9a074-126">Use D3DDECLUSAGE\_TEXCOORD, n to specify texture coordinates in fixed function vertex processing and in pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="9a074-127">Elles peuvent être utilisées pour transmettre des données définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9a074-127">These can be used to pass user defined data.</span></span>

</dd> <dt>

<span data-ttu-id="9a074-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE \_ tangente**</span><span class="sxs-lookup"><span data-stu-id="9a074-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE\_TANGENT**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-129">Données de tangente de vertex.</span><span class="sxs-lookup"><span data-stu-id="9a074-129">Vertex tangent data.</span></span>

</dd> <dt>

<span data-ttu-id="9a074-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE \_ BInormal**</span><span class="sxs-lookup"><span data-stu-id="9a074-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE\_BINORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-131">Données binormales de vertex.</span><span class="sxs-lookup"><span data-stu-id="9a074-131">Vertex binormal data.</span></span>

</dd> <dt>

<span data-ttu-id="9a074-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ TESSFACTOR**</span><span class="sxs-lookup"><span data-stu-id="9a074-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE\_TESSFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-133">Valeur à virgule flottante positive unique.</span><span class="sxs-lookup"><span data-stu-id="9a074-133">Single positive floating point value.</span></span> <span data-ttu-id="9a074-134">Utilisez D3DDECLUSAGE \_ TESSFACTOR avec un index d’utilisation de 0 pour spécifier un facteur de pavage utilisé dans l’unité de pavage pour contrôler le taux de pavage.</span><span class="sxs-lookup"><span data-stu-id="9a074-134">Use D3DDECLUSAGE\_TESSFACTOR with a usage index of 0 to specify a tessellation factor used in the tessellation unit to control the rate of tessellation.</span></span> <span data-ttu-id="9a074-135">Pour plus d’informations sur le type de données, consultez D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="9a074-135">For more information about the data type, see D3DDECLTYPE\_FLOAT1.</span></span>

</dd> <dt>

<span data-ttu-id="9a074-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**\_Position D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="9a074-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE\_POSITIONT**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-137">Les données de vertex contiennent des données de position transformées allant de (0,0) à (largeur de la fenêtre d’affichage, hauteur de la fenêtre d’affichage).</span><span class="sxs-lookup"><span data-stu-id="9a074-137">Vertex data contains transformed position data ranging from (0,0) to (viewport width, viewport height).</span></span> <span data-ttu-id="9a074-138">Utilisez D3DDECLUSAGE \_ position avec un index d’utilisation égal à 0 pour spécifier la position transformée.</span><span class="sxs-lookup"><span data-stu-id="9a074-138">Use D3DDECLUSAGE\_POSITIONT with a usage index of 0 to specify transformed position.</span></span> <span data-ttu-id="9a074-139">Lorsqu’une déclaration contenant cette valeur est définie, le pipeline n’effectue pas de traitement de vertex.</span><span class="sxs-lookup"><span data-stu-id="9a074-139">When a declaration containing this is set, the pipeline does not perform vertex processing.</span></span>

</dd> <dt>

<span data-ttu-id="9a074-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**\_Couleur D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="9a074-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**D3DDECLUSAGE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-141">Les données de vertex contiennent une couleur diffuse ou spéculaire.</span><span class="sxs-lookup"><span data-stu-id="9a074-141">Vertex data contains diffuse or specular color.</span></span> <span data-ttu-id="9a074-142">Utilisez la \_ couleur D3DDECLUSAGE avec un index d’utilisation de 0 pour spécifier la couleur diffuse dans le nuanceur de sommets de fonction fixe et les nuanceurs de pixels avant PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="9a074-142">Use D3DDECLUSAGE\_COLOR with a usage index of 0 to specify the diffuse color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="9a074-143">Utilisez la \_ couleur D3DDECLUSAGE avec un index d’utilisation de 1 pour spécifier la couleur spéculaire dans le nuanceur de sommets de fonction fixe et les nuanceurs de pixels antérieurs à PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="9a074-143">Use D3DDECLUSAGE\_COLOR with a usage index of 1 to specify the specular color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="9a074-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**\_Brouillard D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="9a074-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE\_FOG**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-145">Les données de vertex contiennent des données de brouillard.</span><span class="sxs-lookup"><span data-stu-id="9a074-145">Vertex data contains fog data.</span></span> <span data-ttu-id="9a074-146">Utilisez \_ le brouillard D3DDECLUSAGE avec un index d’utilisation de 0 pour spécifier une valeur de fusion de brouillard utilisée après la fin de l’ombrage de pixel.</span><span class="sxs-lookup"><span data-stu-id="9a074-146">Use D3DDECLUSAGE\_FOG with a usage index of 0 to specify a fog blend value used after pixel shading finishes.</span></span> <span data-ttu-id="9a074-147">Cela s’applique aux nuanceurs de pixels antérieurs à la version PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="9a074-147">This applies to pixel shaders prior to version ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="9a074-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE \_ profondeur)**</span><span class="sxs-lookup"><span data-stu-id="9a074-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE\_DEPTH**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-149">Les données de vertex contiennent des données de profondeur.</span><span class="sxs-lookup"><span data-stu-id="9a074-149">Vertex data contains depth data.</span></span>

</dd> <dt>

<span data-ttu-id="9a074-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**\_Exemple D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="9a074-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**D3DDECLUSAGE\_SAMPLE**</span></span>
</dt> <dd>

<span data-ttu-id="9a074-151">Les données de vertex contiennent des exemples de données.</span><span class="sxs-lookup"><span data-stu-id="9a074-151">Vertex data contains sampler data.</span></span> <span data-ttu-id="9a074-152">Utilisez \_ l’exemple D3DDECLUSAGE avec un index d’utilisation de 0 pour spécifier la valeur de déplacement à rechercher.</span><span class="sxs-lookup"><span data-stu-id="9a074-152">Use D3DDECLUSAGE\_SAMPLE with a usage index of 0 to specify the displacement value to look up.</span></span> <span data-ttu-id="9a074-153">Il peut être utilisé uniquement avec D3DDECLUSAGE \_ LOOKUPPRESAMPLED ou D3DDECLUSAGE \_ Lookup.</span><span class="sxs-lookup"><span data-stu-id="9a074-153">It can be used only with D3DDECLUSAGE\_LOOKUPPRESAMPLED or D3DDECLUSAGE\_LOOKUP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a074-154">Notes</span><span class="sxs-lookup"><span data-stu-id="9a074-154">Remarks</span></span>

<span data-ttu-id="9a074-155">Les données de vertex sont déclarées avec un tableau de structures [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="9a074-155">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="9a074-156">Chaque élément du tableau contient un type d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="9a074-156">Each element in the array contains a usage type.</span></span>

<span data-ttu-id="9a074-157">Pour plus d’informations sur les déclarations de vertex, consultez la rubrique [déclaration de vertex (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="9a074-157">For more information about vertex declarations, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a074-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a074-158">Requirements</span></span>



| <span data-ttu-id="9a074-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a074-159">Requirement</span></span> | <span data-ttu-id="9a074-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a074-160">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a074-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a074-161">Header</span></span><br/> | <dl> <span data-ttu-id="9a074-162"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a074-162"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a074-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a074-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a074-164">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="9a074-164">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="9a074-165">Déclaration de vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9a074-165">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 




