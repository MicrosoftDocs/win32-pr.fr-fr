---
description: Définit la méthode de déclaration de vertex qui est une opération prédéfinie effectuée par le du paveur (ou toute routine de géométrie procédurale sur les données de vertex pendant le pavage).
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: Énumération D3DDECLMETHOD (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322730"
---
# <a name="d3ddeclmethod-enumeration"></a><span data-ttu-id="e10b7-103">Énumération D3DDECLMETHOD</span><span class="sxs-lookup"><span data-stu-id="e10b7-103">D3DDECLMETHOD enumeration</span></span>

<span data-ttu-id="e10b7-104">Définit la méthode de déclaration de vertex qui est une opération prédéfinie effectuée par le du paveur (ou toute routine de géométrie procédurale sur les données de vertex pendant le pavage).</span><span class="sxs-lookup"><span data-stu-id="e10b7-104">Defines the vertex declaration method which is a predefined operation performed by the tessellator (or any procedural geometry routine on the vertex data during tessellation).</span></span>

## <a name="syntax"></a><span data-ttu-id="e10b7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e10b7-105">Syntax</span></span>


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a><span data-ttu-id="e10b7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e10b7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e10b7-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="e10b7-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="e10b7-108">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e10b7-108">Default value.</span></span> <span data-ttu-id="e10b7-109">Le du paveur copie les données de vertex (données de spline pour les correctifs) telles quelles, sans calculs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e10b7-109">The tessellator copies the vertex data (spline data for patches) as is, with no additional calculations.</span></span> <span data-ttu-id="e10b7-110">Lorsque le du paveur est utilisé, cet élément est interpolé.</span><span class="sxs-lookup"><span data-stu-id="e10b7-110">When the tessellator is used, this element is interpolated.</span></span> <span data-ttu-id="e10b7-111">Sinon, les données de vertex sont copiées dans le registre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e10b7-111">Otherwise vertex data is copied into the input register.</span></span> <span data-ttu-id="e10b7-112">Le type d’entrée et de sortie peut être n’importe quelle valeur, mais sont toujours du même type.</span><span class="sxs-lookup"><span data-stu-id="e10b7-112">The input and output type can be any value, but are always the same type.</span></span>

</dd> <dt>

<span data-ttu-id="e10b7-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ partiel**</span><span class="sxs-lookup"><span data-stu-id="e10b7-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD\_PARTIALU**</span></span>
</dt> <dd>

<span data-ttu-id="e10b7-114">Calcule la tangente à un point du rectangle ou du carreau de triangle dans la direction U.</span><span class="sxs-lookup"><span data-stu-id="e10b7-114">Computes the tangent at a point on the rectangle or triangle patch in the U direction.</span></span> <span data-ttu-id="e10b7-115">Le type d’entrée peut être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="e10b7-115">The input type can be one of the following:</span></span>

-   <span data-ttu-id="e10b7-116">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="e10b7-116">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="e10b7-117">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="e10b7-117">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="e10b7-118">D3DDECLTYPE \_ float4</span><span class="sxs-lookup"><span data-stu-id="e10b7-118">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="e10b7-119">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="e10b7-119">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="e10b7-120">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="e10b7-120">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="e10b7-121">Le type de sortie est toujours D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="e10b7-121">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="e10b7-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ PARTIALV**</span><span class="sxs-lookup"><span data-stu-id="e10b7-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD\_PARTIALV**</span></span>
</dt> <dd>

<span data-ttu-id="e10b7-123">Calcule la tangente à un point du rectangle ou du carreau de triangle dans la direction V.</span><span class="sxs-lookup"><span data-stu-id="e10b7-123">Computes the tangent at a point on the rectangle or triangle patch in the V direction.</span></span> <span data-ttu-id="e10b7-124">Le type d’entrée peut être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="e10b7-124">The input type can be one of the following:</span></span>

-   <span data-ttu-id="e10b7-125">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="e10b7-125">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="e10b7-126">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="e10b7-126">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="e10b7-127">D3DDECLTYPE \_ float4</span><span class="sxs-lookup"><span data-stu-id="e10b7-127">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="e10b7-128">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="e10b7-128">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="e10b7-129">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="e10b7-129">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="e10b7-130">Le type de sortie est toujours D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="e10b7-130">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="e10b7-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ CROSSUV**</span><span class="sxs-lookup"><span data-stu-id="e10b7-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD\_CROSSUV**</span></span>
</dt> <dd>

<span data-ttu-id="e10b7-132">Calcule le normal à un point sur le rectangle ou le triangle en utilisant le produit croisé de deux tangentes.</span><span class="sxs-lookup"><span data-stu-id="e10b7-132">Computes the normal at a point on the rectangle or triangle patch by taking the cross product of two tangents.</span></span> <span data-ttu-id="e10b7-133">Le type d’entrée peut être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="e10b7-133">The input type can be one of the following:</span></span>

-   <span data-ttu-id="e10b7-134">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="e10b7-134">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="e10b7-135">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="e10b7-135">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="e10b7-136">D3DDECLTYPE \_ float4</span><span class="sxs-lookup"><span data-stu-id="e10b7-136">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="e10b7-137">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="e10b7-137">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="e10b7-138">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="e10b7-138">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="e10b7-139">Le type de sortie est toujours D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="e10b7-139">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="e10b7-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**\_UV D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="e10b7-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="e10b7-141">Copiez les valeurs U, V à un point sur le rectangle ou le correctif à triangle.</span><span class="sxs-lookup"><span data-stu-id="e10b7-141">Copy out the U, V values at a point on the rectangle or triangle patch.</span></span> <span data-ttu-id="e10b7-142">Cela aboutit à un float 2D.</span><span class="sxs-lookup"><span data-stu-id="e10b7-142">This results in a 2D float.</span></span> <span data-ttu-id="e10b7-143">Le type d’entrée doit être défini sur D3DDECLTYPE \_ inutilisé.</span><span class="sxs-lookup"><span data-stu-id="e10b7-143">The input type must be set to D3DDECLTYPE\_UNUSED.</span></span> <span data-ttu-id="e10b7-144">Le type de données de sortie est toujours D3DDECLTYPE \_ FLOAT2.</span><span class="sxs-lookup"><span data-stu-id="e10b7-144">The output data type is always D3DDECLTYPE\_FLOAT2.</span></span> <span data-ttu-id="e10b7-145">Le flux d’entrée et le décalage sont également inutilisés (mais doivent avoir la valeur 0).</span><span class="sxs-lookup"><span data-stu-id="e10b7-145">The input stream and offset are also unused (but must be set to 0).</span></span>

</dd> <dt>

<span data-ttu-id="e10b7-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**\_Recherche D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="e10b7-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD\_LOOKUP**</span></span>
</dt> <dd>

<span data-ttu-id="e10b7-147">Recherche d’une carte de déplacement.</span><span class="sxs-lookup"><span data-stu-id="e10b7-147">Look up a displacement map.</span></span> <span data-ttu-id="e10b7-148">Le type d’entrée peut être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="e10b7-148">The input type can be one of the following:</span></span>

-   <span data-ttu-id="e10b7-149">D3DDECLTYPE \_ FLOAT2</span><span class="sxs-lookup"><span data-stu-id="e10b7-149">D3DDECLTYPE\_FLOAT2</span></span>
-   <span data-ttu-id="e10b7-150">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="e10b7-150">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="e10b7-151">D3DDECLTYPE \_ float4</span><span class="sxs-lookup"><span data-stu-id="e10b7-151">D3DDECLTYPE\_FLOAT4</span></span>

<span data-ttu-id="e10b7-152">Seuls les composants. x et. y sont utilisés pour la recherche de la carte de texture.</span><span class="sxs-lookup"><span data-stu-id="e10b7-152">Only the .x and .y components are used for the texture map lookup.</span></span> <span data-ttu-id="e10b7-153">Le type de sortie est toujours D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="e10b7-153">The output type is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="e10b7-154">L’appareil doit prendre en charge le mappage de déplacement.</span><span class="sxs-lookup"><span data-stu-id="e10b7-154">The device must support displacement mapping.</span></span> <span data-ttu-id="e10b7-155">Pour plus d’informations sur le mappage de déplacement, consultez [mappage de déplacement (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="e10b7-155">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="e10b7-156">Cette constante est prise en charge uniquement par le pipeline programmable sur les données N-patch, si les N-patchs sont activés.</span><span class="sxs-lookup"><span data-stu-id="e10b7-156">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span>

</dd> <dt>

<span data-ttu-id="e10b7-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ LOOKUPPRESAMPLED**</span><span class="sxs-lookup"><span data-stu-id="e10b7-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD\_LOOKUPPRESAMPLED**</span></span>
</dt> <dd>

<span data-ttu-id="e10b7-158">Recherche d’une carte de décalage prééchantillonnée.</span><span class="sxs-lookup"><span data-stu-id="e10b7-158">Look up a presampled displacement map.</span></span> <span data-ttu-id="e10b7-159">Le type d’entrée doit être défini sur D3DDECLTYPE \_ inutilisé ; l’index de flux et le décalage de flux doivent avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="e10b7-159">The input type must be set to D3DDECLTYPE\_UNUSED; the stream index and the stream offset must be set to 0.</span></span> <span data-ttu-id="e10b7-160">Le type de sortie de cette opération est toujours D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="e10b7-160">The output type for this operation is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="e10b7-161">L’appareil doit prendre en charge le mappage de déplacement.</span><span class="sxs-lookup"><span data-stu-id="e10b7-161">The device must support displacement mapping.</span></span> <span data-ttu-id="e10b7-162">Pour plus d’informations sur le mappage de déplacement, consultez [mappage de déplacement (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="e10b7-162">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="e10b7-163">Cette constante est prise en charge uniquement par le pipeline programmable sur les données N-patch, si les N-patchs sont activés.</span><span class="sxs-lookup"><span data-stu-id="e10b7-163">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span> <span data-ttu-id="e10b7-164">Cette méthode peut être utilisée uniquement avec l' \_ exemple D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="e10b7-164">This method can be used only with D3DDECLUSAGE\_SAMPLE.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e10b7-165">Notes</span><span class="sxs-lookup"><span data-stu-id="e10b7-165">Remarks</span></span>

<span data-ttu-id="e10b7-166">Le du paveur examine la méthode pour déterminer les données à calculer à partir des données de vertex pendant le pavage.</span><span class="sxs-lookup"><span data-stu-id="e10b7-166">The tessellator looks at the method to determine what data to calculate from the vertex data during tessellation.</span></span> <span data-ttu-id="e10b7-167">Les données de maillage doivent utiliser la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e10b7-167">Mesh data should use the default value.</span></span> <span data-ttu-id="e10b7-168">Les correctifs peuvent utiliser n’importe quel autre type implémenté.</span><span class="sxs-lookup"><span data-stu-id="e10b7-168">Patches can use any of the other implemented types.</span></span>

<span data-ttu-id="e10b7-169">Les données de vertex sont déclarées avec un tableau de structures [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="e10b7-169">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="e10b7-170">Chaque élément du tableau contient une méthode de déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="e10b7-170">Each element in the array contains a vertex declaration method.</span></span>

<span data-ttu-id="e10b7-171">En plus de l’utilisation de D3DDECLMETHOD \_ par défaut, un maillage normal peut utiliser \_ des méthodes D3DDECLMETHOD Lookup et D3DDECLMETHOD \_ LOOKUPPRESAMPLED lorsque N-patchs sont activés.</span><span class="sxs-lookup"><span data-stu-id="e10b7-171">In addition to using D3DDECLMETHOD\_DEFAULT, a normal mesh can use D3DDECLMETHOD\_LOOKUP and D3DDECLMETHOD\_LOOKUPPRESAMPLED methods when N-patches are enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="e10b7-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e10b7-172">Requirements</span></span>



| <span data-ttu-id="e10b7-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e10b7-173">Requirement</span></span> | <span data-ttu-id="e10b7-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="e10b7-174">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e10b7-175">En-tête</span><span class="sxs-lookup"><span data-stu-id="e10b7-175">Header</span></span><br/> | <dl> <span data-ttu-id="e10b7-176"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e10b7-176"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e10b7-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e10b7-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10b7-178">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="e10b7-178">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




