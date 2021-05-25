---
description: Les constantes de format de vertex flexibles, ou codes de la Commission, sont utilisées pour décrire le contenu des vertex entrelacés dans un flux de données unique qui sera traité par le pipeline de fonction fixe.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a088dda530904c320720371c76601fd4fb254481
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343259"
---
# <a name="d3dfvf"></a>D3DFVF

Les constantes de format de vertex flexibles, ou codes de la Commission, sont utilisées pour décrire le contenu des vertex entrelacés dans un flux de données unique qui sera traité par le pipeline de fonction fixe.

## <a name="vertex-data-flags"></a>Indicateurs de données de vertex

Les indicateurs suivants décrivent un format de vertex. Pour plus d’informations sur les formats de vertex, consultez [fonction fixe codes de la Commission du prix final (Direct3D 9)](fixed-function-fvf-codes.md).



| \#définition                            | Description                                                                                                                                                                                                                                                                                                                                                             | Ordre et type des données                                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| \_Diffusion D3DFVF                     | Le format vertex comprend un composant de couleur diffuse.                                                                                                                                                                                                                                                                                                                       | DWORD dans l’ordre ARVB. Consultez [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ normal                      | Le format vertex comprend un vecteur normal de vertex. Cet indicateur ne peut pas être utilisé avec l' \_ indicateur D3DFVF XYZRHW.                                                                                                                                                                                                                                                                   | float, float, float                                                                                       |
| D3DFVF \_ psize                       | Format de vertex spécifié en taille en points. Cette taille est exprimée en unités d’espace de caméra pour les vertex qui ne sont pas transformés et allumés, et dans les unités d’espace de l’appareil pour les vertex transformés et allumés.                                                                                                                                                                          | float                                                                                                     |
| D3DFVF \_ spéculaire                    | Le format vertex comprend un composant de couleur spéculaire.                                                                                                                                                                                                                                                                                                                      | DWORD dans l’ordre ARVB. Consultez [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ xyz                         | Le format vertex comprend la position d’un vertex non transformé. Cet indicateur ne peut pas être utilisé avec l' \_ indicateur D3DFVF XYZRHW.                                                                                                                                                                                                                                                  | float, float, float.                                                                                      |
| D3DFVF \_ XYZRHW                      | Le format vertex comprend la position d’un vertex transformé. Cet indicateur ne peut pas être utilisé avec les \_ indicateurs normaux D3DFVF XYZ ou D3DFVF \_ .                                                                                                                                                                                                                                     | float, float, float, float.                                                                               |
| D3DFVF \_ XYZB1 à D3DFVF \_ XYZB5 | Le format vertex contient des données de position et un nombre correspondant de valeurs de pondération (bêta) à utiliser pour les opérations de fusion de vertex multimatrix. À l’heure actuelle, Direct3D peut fusionner avec jusqu’à trois valeurs de pondération et quatre matrices de fusion. Pour plus d’informations sur l’utilisation des matrices de fusion, consultez la rubrique [fusion des vertex indexés (Direct3D 9)](indexed-vertex-blending.md). | 1, 2 ou 3 valeurs à virgule flottante. Quand D3DFVF \_ LASTBETA \_ UBYTE4 est utilisé, la dernière pondération de fusion est traitée comme une valeur DWORD. |
| D3DFVF \_ XYZW                        | Le format vertex contient les données transformées et découpées (x, y, z, w). ProcessVertices n’appelle pas l’Clipper, à la place de données en coordonnées de clip. Cette constante est conçue pour et peut uniquement être utilisée avec le pipeline de vertex programmable.                                                                                                                 | float, float, float, float                                                                                |



 

## <a name="texture-flags"></a>Indicateurs de texture

Les indicateurs suivants décrivent les indicateurs de texture utilisés par le pipeline de fonction fixe.



| \#définition                          | Description                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFVF \_ TEX0-D3DFVF \_ TEX8       | Nombre de jeux de coordonnées de texture pour ce vertex. Les valeurs réelles de ces indicateurs ne sont pas séquentielles.                                                                                                                                                                           |
| D3DFVF \_ TEXCOORDSIZEN (coordIndex) | Définissez un jeu de données de coordonnées de texture. n indique la dimension des coordonnées de texture. coordIndex indique le numéro d’index de la coordonnée de texture. Consultez [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) , [coordonnées de texture et étapes de texture](texture-coordinates.md). |



 

## <a name="mask-flags"></a>Indicateurs de masque

Les indicateurs suivants décrivent les indicateurs de masque utilisés par le pipeline de fonction fixe.



| \#définition                             | Description                                           |
|--------------------------------------|-------------------------------------------------------|
| \_Masque de position D3DFVF \_               | Masque pour les bits de position.                               |
| D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2 | Valeurs de masque pour les bits réservés dans le prix de la Commission. Ne pas utiliser. |
| \_Masque D3DFVF TEXCOUNT \_               | Valeur de masque pour les bits d’indicateur de texture.                     |



 

## <a name="miscellaneous-flags"></a>Indicateurs divers

Les indicateurs suivants décrivent divers indicateurs utilisés par le pipeline de fonction fixe.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#définition</td>
<td>Description</td>
</tr>
<tr class="even">
<td>D3DFVF_LASTBETA_D3DCOLOR</td>
<td>Le dernier champ bêta dans les données de position du vertex sera de type D3DCOLOR. Les données des champs bêta sont utilisées avec l’apparence de palette de matrices pour spécifier des index de matrice.</td>
</tr>
<tr class="odd">
<td>D3DFVF_LASTBETA_UBYTE4</td>
<td>Le dernier champ bêta dans les données de position du vertex sera de type UBYTE4. Les données des champs bêta sont utilisées avec l’apparence de palette de matrices pour spécifier des index de matrice. <span data-codelanguage=""></span>
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

<p>Étant donné que le prix final est déclaré comme suit : D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4. Weight et MatrixIndices sont inclus dans la version bêta [5], où D3DFVF_LASTBETA_UBYTE4 indique d’interpréter le dernier DWORD de la version bêta [5] en tant que type UBYTE4.</p></td>
</tr>
<tr class="even">
<td>D3DFVF_TEXCOUNT_SHIFT</td>
<td>Nombre de bits par lequel décaler une valeur entière qui identifie le nombre de coordonnées de texture pour un vertex. Cette valeur peut être utilisée comme indiqué ci-dessous.
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



 

### <a name="examples"></a>Exemples

Les exemples suivants illustrent d’autres combinaisons courantes d’indicateurs.


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



## <a name="constant-information"></a>Informations constantes



| Condition requise                         | Valeur            |
|--------------------------|-------------|
| En-tête                   | d3d9types. h |
| Système d’exploitation minimal | Windows 98  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[Correction des codes de fonction de la Commission (Direct3D 9)](fixed-function-fvf-codes.md)
</dt> <dt>

[Fusion géométrique (Direct3D 9)](geometry-blending.md)
</dt> </dl>

 

 



