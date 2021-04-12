---
description: Définit un ensemble de propriétés d’éclairage.
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: D3DLIGHT9, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 90e72fbb2bf4f1d74a74dc177346387b36eb25e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211817"
---
# <a name="d3dlight9-structure"></a><span data-ttu-id="af90b-103">D3DLIGHT9, structure</span><span class="sxs-lookup"><span data-stu-id="af90b-103">D3DLIGHT9 structure</span></span>

<span data-ttu-id="af90b-104">Définit un ensemble de propriétés d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="af90b-104">Defines a set of lighting properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="af90b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af90b-105">Syntax</span></span>


```C++
typedef struct D3DLIGHT9 {
  D3DLIGHTTYPE  Type;
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Ambient;
  D3DVECTOR     Position;
  D3DVECTOR     Direction;
  float         Range;
  float         Falloff;
  float         Attenuation0;
  float         Attenuation1;
  float         Attenuation2;
  float         Theta;
  float         Phi;
} D3DLIGHT9, *LPD3DLIGHT;
```



## <a name="members"></a><span data-ttu-id="af90b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="af90b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="af90b-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="af90b-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="af90b-108">Type : **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**</span><span class="sxs-lookup"><span data-stu-id="af90b-108">Type: **[**D3DLIGHTTYPE**](./d3dlighttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af90b-109">Type de la source de lumière.</span><span class="sxs-lookup"><span data-stu-id="af90b-109">Type of the light source.</span></span> <span data-ttu-id="af90b-110">Cette valeur est l’un des membres du type énuméré [**D3DLIGHTTYPE**](./d3dlighttype.md) .</span><span class="sxs-lookup"><span data-stu-id="af90b-110">This value is one of the members of the [**D3DLIGHTTYPE**](./d3dlighttype.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="af90b-111">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="af90b-111">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="af90b-112">Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="af90b-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af90b-113">Couleur diffuse émise par la lumière.</span><span class="sxs-lookup"><span data-stu-id="af90b-113">Diffuse color emitted by the light.</span></span> <span data-ttu-id="af90b-114">Ce membre est une structure [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="af90b-114">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="af90b-115">**Spéculaire**</span><span class="sxs-lookup"><span data-stu-id="af90b-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="af90b-116">Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="af90b-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af90b-117">Couleur spéculaire émise par la lumière.</span><span class="sxs-lookup"><span data-stu-id="af90b-117">Specular color emitted by the light.</span></span> <span data-ttu-id="af90b-118">Ce membre est une structure [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="af90b-118">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="af90b-119">**Ambiant**</span><span class="sxs-lookup"><span data-stu-id="af90b-119">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="af90b-120">Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="af90b-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af90b-121">Couleur ambiante émise par la lumière.</span><span class="sxs-lookup"><span data-stu-id="af90b-121">Ambient color emitted by the light.</span></span> <span data-ttu-id="af90b-122">Ce membre est une structure [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="af90b-122">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="af90b-123">**Position**</span><span class="sxs-lookup"><span data-stu-id="af90b-123">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="af90b-124">Type : **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="af90b-124">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af90b-125">Position de la lumière dans l’espace universel, spécifiée par une structure [**D3DVECTOR**](d3dvector.md) .</span><span class="sxs-lookup"><span data-stu-id="af90b-125">Position of the light in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="af90b-126">Ce membre n’a aucune signification pour les lumières directionnelles et est ignoré dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="af90b-126">This member has no meaning for directional lights and is ignored in that case.</span></span>

</dd> <dt>

<span data-ttu-id="af90b-127">**Sens**</span><span class="sxs-lookup"><span data-stu-id="af90b-127">**Direction**</span></span>
</dt> <dd>

<span data-ttu-id="af90b-128">Type : **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="af90b-128">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af90b-129">Direction de pointage de la lumière dans l’espace universel, spécifiée par une structure [**D3DVECTOR**](d3dvector.md) .</span><span class="sxs-lookup"><span data-stu-id="af90b-129">Direction that the light is pointing in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="af90b-130">Ce membre a une signification uniquement pour les directions et les lumières.</span><span class="sxs-lookup"><span data-stu-id="af90b-130">This member has meaning only for directional and spotlights.</span></span> <span data-ttu-id="af90b-131">Ce vecteur n’a pas besoin d’être normalisé, mais il doit avoir une longueur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="af90b-131">This vector need not be normalized, but it should have a nonzero length.</span></span>

</dd> <dt>

<span data-ttu-id="af90b-132">**Plage**</span><span class="sxs-lookup"><span data-stu-id="af90b-132">**Range**</span></span>
</dt> <dd>

<span data-ttu-id="af90b-133">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="af90b-133">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="af90b-134">Distance au-delà de laquelle la lumière n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="af90b-134">Distance beyond which the light has no effect.</span></span> <span data-ttu-id="af90b-135">La valeur maximale autorisée pour ce membre est la racine carrée de FLT \_ Max.</span><span class="sxs-lookup"><span data-stu-id="af90b-135">The maximum allowable value for this member is the square root of FLT\_MAX.</span></span> <span data-ttu-id="af90b-136">Ce membre n’affecte pas les lumières directionnelles.</span><span class="sxs-lookup"><span data-stu-id="af90b-136">This member does not affect directional lights.</span></span>

</dd> <dt>

<span data-ttu-id="af90b-137">**Atténuation**</span><span class="sxs-lookup"><span data-stu-id="af90b-137">**Falloff**</span></span>
</dt> <dd>

<span data-ttu-id="af90b-138">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="af90b-138">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="af90b-139">Diminution de l’éclairage entre le cône interne d’un projecteur (angle spécifié par thêta) et le bord extérieur du cône externe (angle spécifié par PHI).</span><span class="sxs-lookup"><span data-stu-id="af90b-139">Decrease in illumination between a spotlight's inner cone (the angle specified by Theta) and the outer edge of the outer cone (the angle specified by Phi).</span></span>

<span data-ttu-id="af90b-140">L’effet de l’atténuation sur l’éclairage est subtil.</span><span class="sxs-lookup"><span data-stu-id="af90b-140">The effect of falloff on the lighting is subtle.</span></span> <span data-ttu-id="af90b-141">En outre, une faible baisse des performances est provoquée par la mise en forme de la courbe décroissante.</span><span class="sxs-lookup"><span data-stu-id="af90b-141">Furthermore, a small performance penalty is incurred by shaping the falloff curve.</span></span> <span data-ttu-id="af90b-142">Pour ces raisons, la plupart des développeurs définissent cette valeur sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="af90b-142">For these reasons, most developers set this value to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="af90b-143">**Attenuation0**</span><span class="sxs-lookup"><span data-stu-id="af90b-143">**Attenuation0**</span></span>
</dt> <dd>

<span data-ttu-id="af90b-144">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="af90b-144">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="af90b-145">Valeur spécifiant la façon dont l’intensité de la lumière change sur la distance.</span><span class="sxs-lookup"><span data-stu-id="af90b-145">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="af90b-146">Les valeurs d’atténuation sont ignorées pour les lumières directionnelles.</span><span class="sxs-lookup"><span data-stu-id="af90b-146">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="af90b-147">Ce membre représente une constante d’atténuation.</span><span class="sxs-lookup"><span data-stu-id="af90b-147">This member represents an attenuation constant.</span></span> <span data-ttu-id="af90b-148">Pour plus d’informations sur l’atténuation, consultez [Propriétés de la lumière (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="af90b-148">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="af90b-149">Les valeurs valides pour cette plage de membres sont comprises entre 0,0 et Infinity.</span><span class="sxs-lookup"><span data-stu-id="af90b-149">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="af90b-150">Pour les lumières non directionnelles, les trois valeurs d’atténuation ne doivent pas être définies sur 0,0 en même temps.</span><span class="sxs-lookup"><span data-stu-id="af90b-150">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="af90b-151">**Attenuation1**</span><span class="sxs-lookup"><span data-stu-id="af90b-151">**Attenuation1**</span></span>
</dt> <dd>

<span data-ttu-id="af90b-152">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="af90b-152">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="af90b-153">Valeur spécifiant la façon dont l’intensité de la lumière change sur la distance.</span><span class="sxs-lookup"><span data-stu-id="af90b-153">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="af90b-154">Les valeurs d’atténuation sont ignorées pour les lumières directionnelles.</span><span class="sxs-lookup"><span data-stu-id="af90b-154">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="af90b-155">Ce membre représente une constante d’atténuation.</span><span class="sxs-lookup"><span data-stu-id="af90b-155">This member represents an attenuation constant.</span></span> <span data-ttu-id="af90b-156">Pour plus d’informations sur l’atténuation, consultez [Propriétés de la lumière (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="af90b-156">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="af90b-157">Les valeurs valides pour cette plage de membres sont comprises entre 0,0 et Infinity.</span><span class="sxs-lookup"><span data-stu-id="af90b-157">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="af90b-158">Pour les lumières non directionnelles, les trois valeurs d’atténuation ne doivent pas être définies sur 0,0 en même temps.</span><span class="sxs-lookup"><span data-stu-id="af90b-158">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="af90b-159">**Attenuation2**</span><span class="sxs-lookup"><span data-stu-id="af90b-159">**Attenuation2**</span></span>
</dt> <dd>

<span data-ttu-id="af90b-160">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="af90b-160">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="af90b-161">Valeur spécifiant la façon dont l’intensité de la lumière change sur la distance.</span><span class="sxs-lookup"><span data-stu-id="af90b-161">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="af90b-162">Les valeurs d’atténuation sont ignorées pour les lumières directionnelles.</span><span class="sxs-lookup"><span data-stu-id="af90b-162">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="af90b-163">Ce membre représente une constante d’atténuation.</span><span class="sxs-lookup"><span data-stu-id="af90b-163">This member represents an attenuation constant.</span></span> <span data-ttu-id="af90b-164">Pour plus d’informations sur l’atténuation, consultez [Propriétés de la lumière (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="af90b-164">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="af90b-165">Les valeurs valides pour cette plage de membres sont comprises entre 0,0 et Infinity.</span><span class="sxs-lookup"><span data-stu-id="af90b-165">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="af90b-166">Pour les lumières non directionnelles, les trois valeurs d’atténuation ne doivent pas être définies sur 0,0 en même temps.</span><span class="sxs-lookup"><span data-stu-id="af90b-166">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="af90b-167">**Thêta**</span><span class="sxs-lookup"><span data-stu-id="af90b-167">**Theta**</span></span>
</dt> <dd>

<span data-ttu-id="af90b-168">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="af90b-168">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="af90b-169">Angle, en radians, du cône interne d’une lumière, c’est-à-dire le cône entièrement éclairé.</span><span class="sxs-lookup"><span data-stu-id="af90b-169">Angle, in radians, of a spotlight's inner cone - that is, the fully illuminated spotlight cone.</span></span> <span data-ttu-id="af90b-170">Cette valeur doit être comprise entre 0 et la valeur spécifiée par Phi.</span><span class="sxs-lookup"><span data-stu-id="af90b-170">This value must be in the range from 0 through the value specified by Phi.</span></span>

</dd> <dt>

<span data-ttu-id="af90b-171">**Santé confidentielles**</span><span class="sxs-lookup"><span data-stu-id="af90b-171">**Phi**</span></span>
</dt> <dd>

<span data-ttu-id="af90b-172">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="af90b-172">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="af90b-173">Angle, en radians, définissant le bord extérieur du cône externe de la lumière.</span><span class="sxs-lookup"><span data-stu-id="af90b-173">Angle, in radians, defining the outer edge of the spotlight's outer cone.</span></span> <span data-ttu-id="af90b-174">Les points en dehors de ce cône ne sont pas allumés par la Spotlight.</span><span class="sxs-lookup"><span data-stu-id="af90b-174">Points outside this cone are not lit by the spotlight.</span></span> <span data-ttu-id="af90b-175">Cette valeur doit être comprise entre 0 et pi.</span><span class="sxs-lookup"><span data-stu-id="af90b-175">This value must be between 0 and pi.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af90b-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af90b-176">Requirements</span></span>



| <span data-ttu-id="af90b-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af90b-177">Requirement</span></span> | <span data-ttu-id="af90b-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="af90b-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af90b-179">En-tête</span><span class="sxs-lookup"><span data-stu-id="af90b-179">Header</span></span><br/> | <dl> <span data-ttu-id="af90b-180"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="af90b-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af90b-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af90b-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af90b-182">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="af90b-182">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="af90b-183">**GetLight**</span><span class="sxs-lookup"><span data-stu-id="af90b-183">**GetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[<span data-ttu-id="af90b-184">**SetLight**</span><span class="sxs-lookup"><span data-stu-id="af90b-184">**SetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
