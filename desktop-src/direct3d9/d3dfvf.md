---
description: Les constantes de format de vertex flexibles, ou codes de la Commission, sont utilisées pour décrire le contenu des vertex entrelacés dans un flux de données unique qui sera traité par le pipeline de fonction fixe.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a12b4f6008023a388bd204440a0b544db85c19
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999436"
---
# <a name="d3dfvf"></a><span data-ttu-id="96d43-103">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="96d43-103">D3DFVF</span></span>

<span data-ttu-id="96d43-104">Les constantes de format de vertex flexibles, ou codes de la Commission, sont utilisées pour décrire le contenu des vertex entrelacés dans un flux de données unique qui sera traité par le pipeline de fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="96d43-104">Flexible Vertex Format Constants, or FVF codes, are used to describe the contents of vertices interleaved in a single data stream that will be processed by the fixed-function pipeline.</span></span>

## <a name="vertex-data-flags"></a><span data-ttu-id="96d43-105">Indicateurs de données de vertex</span><span class="sxs-lookup"><span data-stu-id="96d43-105">Vertex Data Flags</span></span>

<span data-ttu-id="96d43-106">Les indicateurs suivants décrivent un format de vertex.</span><span class="sxs-lookup"><span data-stu-id="96d43-106">The following flags describe a vertex format.</span></span> <span data-ttu-id="96d43-107">Pour plus d’informations sur les formats de vertex, consultez [fonction fixe codes de la Commission du prix final (Direct3D 9)](fixed-function-fvf-codes.md).</span><span class="sxs-lookup"><span data-stu-id="96d43-107">For information regarding vertex formats, see [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span>



| <span data-ttu-id="96d43-108">\#définition</span><span class="sxs-lookup"><span data-stu-id="96d43-108">\#define</span></span>                            | <span data-ttu-id="96d43-109">Description</span><span class="sxs-lookup"><span data-stu-id="96d43-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="96d43-110">Ordre et type des données</span><span class="sxs-lookup"><span data-stu-id="96d43-110">Data order and type</span></span>                                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d43-111">\_Diffusion D3DFVF</span><span class="sxs-lookup"><span data-stu-id="96d43-111">D3DFVF\_DIFFUSE</span></span>                     | <span data-ttu-id="96d43-112">Le format vertex comprend un composant de couleur diffuse.</span><span class="sxs-lookup"><span data-stu-id="96d43-112">Vertex format includes a diffuse color component.</span></span>                                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="96d43-113">DWORD dans l’ordre ARVB.</span><span class="sxs-lookup"><span data-stu-id="96d43-113">DWORD in ARGB order.</span></span> <span data-ttu-id="96d43-114">Consultez [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="96d43-114">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="96d43-115">D3DFVF \_ normal</span><span class="sxs-lookup"><span data-stu-id="96d43-115">D3DFVF\_NORMAL</span></span>                      | <span data-ttu-id="96d43-116">Le format vertex comprend un vecteur normal de vertex.</span><span class="sxs-lookup"><span data-stu-id="96d43-116">Vertex format includes a vertex normal vector.</span></span> <span data-ttu-id="96d43-117">Cet indicateur ne peut pas être utilisé avec l' \_ indicateur D3DFVF XYZRHW.</span><span class="sxs-lookup"><span data-stu-id="96d43-117">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="96d43-118">float, float, float</span><span class="sxs-lookup"><span data-stu-id="96d43-118">float, float, float</span></span>                                                                                       |
| <span data-ttu-id="96d43-119">D3DFVF \_ psize</span><span class="sxs-lookup"><span data-stu-id="96d43-119">D3DFVF\_PSIZE</span></span>                       | <span data-ttu-id="96d43-120">Format de vertex spécifié en taille en points.</span><span class="sxs-lookup"><span data-stu-id="96d43-120">Vertex format specified in point size.</span></span> <span data-ttu-id="96d43-121">Cette taille est exprimée en unités d’espace de caméra pour les vertex qui ne sont pas transformés et allumés, et dans les unités d’espace de l’appareil pour les vertex transformés et allumés.</span><span class="sxs-lookup"><span data-stu-id="96d43-121">This size is expressed in camera space units for vertices that are not transformed and lit, and in device-space units for transformed and lit vertices.</span></span>                                                                                                                                                                          | <span data-ttu-id="96d43-122">float</span><span class="sxs-lookup"><span data-stu-id="96d43-122">float</span></span>                                                                                                     |
| <span data-ttu-id="96d43-123">D3DFVF \_ spéculaire</span><span class="sxs-lookup"><span data-stu-id="96d43-123">D3DFVF\_SPECULAR</span></span>                    | <span data-ttu-id="96d43-124">Le format vertex comprend un composant de couleur spéculaire.</span><span class="sxs-lookup"><span data-stu-id="96d43-124">Vertex format includes a specular color component.</span></span>                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="96d43-125">DWORD dans l’ordre ARVB.</span><span class="sxs-lookup"><span data-stu-id="96d43-125">DWORD in ARGB order.</span></span> <span data-ttu-id="96d43-126">Consultez [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="96d43-126">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="96d43-127">D3DFVF \_ xyz</span><span class="sxs-lookup"><span data-stu-id="96d43-127">D3DFVF\_XYZ</span></span>                         | <span data-ttu-id="96d43-128">Le format vertex comprend la position d’un vertex non transformé.</span><span class="sxs-lookup"><span data-stu-id="96d43-128">Vertex format includes the position of an untransformed vertex.</span></span> <span data-ttu-id="96d43-129">Cet indicateur ne peut pas être utilisé avec l' \_ indicateur D3DFVF XYZRHW.</span><span class="sxs-lookup"><span data-stu-id="96d43-129">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="96d43-130">float, float, float.</span><span class="sxs-lookup"><span data-stu-id="96d43-130">float, float, float.</span></span>                                                                                      |
| <span data-ttu-id="96d43-131">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="96d43-131">D3DFVF\_XYZRHW</span></span>                      | <span data-ttu-id="96d43-132">Le format vertex comprend la position d’un vertex transformé.</span><span class="sxs-lookup"><span data-stu-id="96d43-132">Vertex format includes the position of a transformed vertex.</span></span> <span data-ttu-id="96d43-133">Cet indicateur ne peut pas être utilisé avec les \_ indicateurs normaux D3DFVF XYZ ou D3DFVF \_ .</span><span class="sxs-lookup"><span data-stu-id="96d43-133">This flag cannot be used with the D3DFVF\_XYZ or D3DFVF\_NORMAL flags.</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="96d43-134">float, float, float, float.</span><span class="sxs-lookup"><span data-stu-id="96d43-134">float, float, float, float.</span></span>                                                                               |
| <span data-ttu-id="96d43-135">D3DFVF \_ XYZB1 à D3DFVF \_ XYZB5</span><span class="sxs-lookup"><span data-stu-id="96d43-135">D3DFVF\_XYZB1 through D3DFVF\_XYZB5</span></span> | <span data-ttu-id="96d43-136">Le format vertex contient des données de position et un nombre correspondant de valeurs de pondération (bêta) à utiliser pour les opérations de fusion de vertex multimatrix.</span><span class="sxs-lookup"><span data-stu-id="96d43-136">Vertex format contains position data, and a corresponding number of weighting (beta) values to use for multimatrix vertex blending operations.</span></span> <span data-ttu-id="96d43-137">À l’heure actuelle, Direct3D peut fusionner avec jusqu’à trois valeurs de pondération et quatre matrices de fusion.</span><span class="sxs-lookup"><span data-stu-id="96d43-137">Currently, Direct3D can blend with up to three weighting values and four blending matrices.</span></span> <span data-ttu-id="96d43-138">Pour plus d’informations sur l’utilisation des matrices de fusion, consultez la rubrique [fusion des vertex indexés (Direct3D 9)](indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="96d43-138">For more information about using blending matrices, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span> | <span data-ttu-id="96d43-139">1, 2 ou 3 valeurs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="96d43-139">1, 2, or 3 floats.</span></span> <span data-ttu-id="96d43-140">Quand D3DFVF \_ LASTBETA \_ UBYTE4 est utilisé, la dernière pondération de fusion est traitée comme une valeur DWORD.</span><span class="sxs-lookup"><span data-stu-id="96d43-140">When D3DFVF\_LASTBETA\_UBYTE4 is used, the last blending weight is treated as a DWORD.</span></span> |
| <span data-ttu-id="96d43-141">D3DFVF \_ XYZW</span><span class="sxs-lookup"><span data-stu-id="96d43-141">D3DFVF\_XYZW</span></span>                        | <span data-ttu-id="96d43-142">Le format vertex contient les données transformées et découpées (x, y, z, w).</span><span class="sxs-lookup"><span data-stu-id="96d43-142">Vertex format contains transformed and clipped (x, y, z, w) data.</span></span> <span data-ttu-id="96d43-143">ProcessVertices n’appelle pas l’Clipper, à la place de données en coordonnées de clip.</span><span class="sxs-lookup"><span data-stu-id="96d43-143">ProcessVertices does not invoke the clipper, instead outputting data in clip coordinates.</span></span> <span data-ttu-id="96d43-144">Cette constante est conçue pour et peut uniquement être utilisée avec le pipeline de vertex programmable.</span><span class="sxs-lookup"><span data-stu-id="96d43-144">This constant is designed for, and can only be used with, the programmable vertex pipeline.</span></span>                                                                                                                 | <span data-ttu-id="96d43-145">float, float, float, float</span><span class="sxs-lookup"><span data-stu-id="96d43-145">float, float, float, float</span></span>                                                                                |



 

## <a name="texture-flags"></a><span data-ttu-id="96d43-146">Indicateurs de texture</span><span class="sxs-lookup"><span data-stu-id="96d43-146">Texture Flags</span></span>

<span data-ttu-id="96d43-147">Les indicateurs suivants décrivent les indicateurs de texture utilisés par le pipeline de fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="96d43-147">The following flags describe texture flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="96d43-148">\#définition</span><span class="sxs-lookup"><span data-stu-id="96d43-148">\#define</span></span>                          | <span data-ttu-id="96d43-149">Description</span><span class="sxs-lookup"><span data-stu-id="96d43-149">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d43-150">D3DFVF \_ TEX0-D3DFVF \_ TEX8</span><span class="sxs-lookup"><span data-stu-id="96d43-150">D3DFVF\_TEX0 - D3DFVF\_TEX8</span></span>       | <span data-ttu-id="96d43-151">Nombre de jeux de coordonnées de texture pour ce vertex.</span><span class="sxs-lookup"><span data-stu-id="96d43-151">Number of texture coordinate sets for this vertex.</span></span> <span data-ttu-id="96d43-152">Les valeurs réelles de ces indicateurs ne sont pas séquentielles.</span><span class="sxs-lookup"><span data-stu-id="96d43-152">The actual values for these flags are not sequential.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="96d43-153">D3DFVF \_ TEXCOORDSIZEN (coordIndex)</span><span class="sxs-lookup"><span data-stu-id="96d43-153">D3DFVF\_TEXCOORDSIZEN(coordIndex)</span></span> | <span data-ttu-id="96d43-154">Définissez un jeu de données de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="96d43-154">Define a texture coordinate data set.</span></span> <span data-ttu-id="96d43-155">n indique la dimension des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="96d43-155">n indicates the dimension of the texture coordinates.</span></span> <span data-ttu-id="96d43-156">coordIndex indique le numéro d’index de la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="96d43-156">coordIndex indicates texture coordinate index number.</span></span> <span data-ttu-id="96d43-157">Consultez [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) , [coordonnées de texture et étapes de texture](texture-coordinates.md).</span><span class="sxs-lookup"><span data-stu-id="96d43-157">See [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) and [Texture coordinates and Texture Stages](texture-coordinates.md).</span></span> |



 

## <a name="mask-flags"></a><span data-ttu-id="96d43-158">Indicateurs de masque</span><span class="sxs-lookup"><span data-stu-id="96d43-158">Mask Flags</span></span>

<span data-ttu-id="96d43-159">Les indicateurs suivants décrivent les indicateurs de masque utilisés par le pipeline de fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="96d43-159">The following flags describe mask flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="96d43-160">\#définition</span><span class="sxs-lookup"><span data-stu-id="96d43-160">\#define</span></span>                             | <span data-ttu-id="96d43-161">Description</span><span class="sxs-lookup"><span data-stu-id="96d43-161">Description</span></span>                                           |
|--------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="96d43-162">\_Masque de position D3DFVF \_</span><span class="sxs-lookup"><span data-stu-id="96d43-162">D3DFVF\_POSITION\_MASK</span></span>               | <span data-ttu-id="96d43-163">Masque pour les bits de position.</span><span class="sxs-lookup"><span data-stu-id="96d43-163">Mask for position bits.</span></span>                               |
| <span data-ttu-id="96d43-164">D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2</span><span class="sxs-lookup"><span data-stu-id="96d43-164">D3DFVF\_RESERVED0, D3DFVF\_RESERVED2</span></span> | <span data-ttu-id="96d43-165">Valeurs de masque pour les bits réservés dans le prix de la Commission.</span><span class="sxs-lookup"><span data-stu-id="96d43-165">Mask values for reserved bits in the FVF.</span></span> <span data-ttu-id="96d43-166">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="96d43-166">Do not use.</span></span> |
| <span data-ttu-id="96d43-167">\_Masque D3DFVF TEXCOUNT \_</span><span class="sxs-lookup"><span data-stu-id="96d43-167">D3DFVF\_TEXCOUNT\_MASK</span></span>               | <span data-ttu-id="96d43-168">Valeur de masque pour les bits d’indicateur de texture.</span><span class="sxs-lookup"><span data-stu-id="96d43-168">Mask value for texture flag bits.</span></span>                     |



 

## <a name="miscellaneous-flags"></a><span data-ttu-id="96d43-169">Indicateurs divers</span><span class="sxs-lookup"><span data-stu-id="96d43-169">Miscellaneous Flags</span></span>

<span data-ttu-id="96d43-170">Les indicateurs suivants décrivent divers indicateurs utilisés par le pipeline de fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="96d43-170">The following flags describe a variety of flags used by the fixed-function pipeline.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96d43-171">#définition</span><span class="sxs-lookup"><span data-stu-id="96d43-171">#define</span></span></td>
<td><span data-ttu-id="96d43-172">Description</span><span class="sxs-lookup"><span data-stu-id="96d43-172">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96d43-173">D3DFVF_LASTBETA_D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="96d43-173">D3DFVF_LASTBETA_D3DCOLOR</span></span></td>
<td><span data-ttu-id="96d43-174">Le dernier champ bêta dans les données de position du vertex sera de type D3DCOLOR.</span><span class="sxs-lookup"><span data-stu-id="96d43-174">The last beta field in the vertex position data will be of type D3DCOLOR.</span></span> <span data-ttu-id="96d43-175">Les données des champs bêta sont utilisées avec l’apparence de palette de matrices pour spécifier des index de matrice.</span><span class="sxs-lookup"><span data-stu-id="96d43-175">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96d43-176">D3DFVF_LASTBETA_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="96d43-176">D3DFVF_LASTBETA_UBYTE4</span></span></td>
<td><span data-ttu-id="96d43-177">Le dernier champ bêta dans les données de position du vertex sera de type UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="96d43-177">The last beta field in the vertex position data will be of type UBYTE4.</span></span> <span data-ttu-id="96d43-178">Les données des champs bêta sont utilisées avec l’apparence de palette de matrices pour spécifier des index de matrice.</span><span class="sxs-lookup"><span data-stu-id="96d43-178">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>// Given the following vertex data definition: 
struct VERTEXPOSITION
{
   float pos[3];
   union 
   {
      float beta[5];
      struct
      {
         float weights[4];
         DWORD MatrixIndices;  // Used as UBYTEs
      }
   }
};</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="96d43-179">Étant donné que le prix final est déclaré comme suit : D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="96d43-179">Given the FVF is declared as: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span></span> <span data-ttu-id="96d43-180">Weight et MatrixIndices sont inclus dans la version bêta [5], où D3DFVF_LASTBETA_UBYTE4 indique d’interpréter le dernier DWORD de la version bêta [5] en tant que type UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="96d43-180">Weight and MatrixIndices are included in beta[5], where D3DFVF_LASTBETA_UBYTE4 says to interpret the last DWORD in beta[5] as type UBYTE4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96d43-181">D3DFVF_TEXCOUNT_SHIFT</span><span class="sxs-lookup"><span data-stu-id="96d43-181">D3DFVF_TEXCOUNT_SHIFT</span></span></td>
<td><span data-ttu-id="96d43-182">Nombre de bits par lequel décaler une valeur entière qui identifie le nombre de coordonnées de texture pour un vertex.</span><span class="sxs-lookup"><span data-stu-id="96d43-182">The number of bits by which to shift an integer value that identifies the number of texture coordinates for a vertex.</span></span> <span data-ttu-id="96d43-183">Cette valeur peut être utilisée comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="96d43-183">This value might be used as shown below.</span></span>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>DWORD dwNumTextures = 1;  // Vertex has only one set of coordinates.

// Shift the value for use when creating a 
//   flexible vertex format (FVF) combination.
dwFVF = dwNumTextures << D3DFVF_TEXCOUNT_SHIFT;

// Now, create an FVF combination using the shifted value.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

### <a name="examples"></a><span data-ttu-id="96d43-184">Exemples</span><span class="sxs-lookup"><span data-stu-id="96d43-184">Examples</span></span>

<span data-ttu-id="96d43-185">Les exemples suivants illustrent d’autres combinaisons courantes d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="96d43-185">The following examples show other common flag combinations.</span></span>


```
// Untransformed vertex for lit, untextured, Gouraud-shaded content.
dwFVF = ( D3DFVF_XYZ | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for unlit, untextured, Gouraud-shaded 
//   content with diffuse material color specified per vertex.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for light-map-based lighting.
dwFVF = ( D3DFVF_XYZ | D3DFVF_TEX2 );
```




```
// Transformed vertex for light-map-based lighting with shared rhw.
dwFVF = ( D3DFVF_XYZRHW | D3DFVF_TEX2 );
```




```
// Heavyweight vertex for unlit, colored content with two 
//   sets of texture coordinates.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE | 
          D3DFVF_SPECULAR | D3DFVF_TEX2 );
```



## <a name="constant-information"></a><span data-ttu-id="96d43-186">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="96d43-186">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="96d43-187">En-tête</span><span class="sxs-lookup"><span data-stu-id="96d43-187">Header</span></span>                   | <span data-ttu-id="96d43-188">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="96d43-188">d3d9types.h</span></span> |
| <span data-ttu-id="96d43-189">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="96d43-189">Minimum operating system</span></span> | <span data-ttu-id="96d43-190">Windows 98</span><span class="sxs-lookup"><span data-stu-id="96d43-190">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="96d43-191">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96d43-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96d43-192">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="96d43-192">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="96d43-193">Correction des codes de fonction de la Commission (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="96d43-193">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
</dt> <dt>

[<span data-ttu-id="96d43-194">Fusion géométrique (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="96d43-194">Geometry Blending (Direct3D 9)</span></span>](geometry-blending.md)
</dt> </dl>

 

 



