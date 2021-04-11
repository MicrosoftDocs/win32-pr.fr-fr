---
title: fonction glDrawPixels (GL. h)
description: La fonction glDrawPixels écrit un bloc de pixels dans le trame.
ms.assetid: c4eda64f-a75e-4e6d-984d-af49414b94d8
keywords:
- glDrawPixels fonction OpenGL
topic_type:
- apiref
api_name:
- glDrawPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25adc8ad28791086020a37d3a30651e169bfd07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103200"
---
# <a name="gldrawpixels-function"></a>glDrawPixels fonction)

La fonction **glDrawPixels** écrit un bloc de pixels dans le trame.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glDrawPixels(
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*width* 
</dt> <dd>

Dimension de largeur du rectangle de pixels qui sera écrite dans le trame.

</dd> <dt>

*height* 
</dt> <dd>

Dimension de hauteur du rectangle de pixels qui sera écrite dans le trame.

</dd> <dt>

*format* 
</dt> <dd>

Format des données de pixels. Les constantes symboliques acceptées sont les suivantes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt><strong>GL_COLOR_INDEX</strong></dt> </dl></td>
<td>Chaque pixel est une valeur unique, un index de couleurs. <br/>
<ol>
<li>La fonction <strong>glDrawPixels</strong> convertit chaque pixel en format à virgule fixe, avec un nombre non spécifié de bits à droite du point binaire, quel que soit le type de données de mémoire. Les valeurs à virgule flottante sont converties en valeurs à virgule fixe vraies. La fonction <strong>glDrawPixels</strong> convertit les données entières signées et non signées avec tous les bits de fraction définis sur zéro. La fonction convertit les données bitmap en 0,0 ou 1,0.</li>
<li>La fonction <strong>glDrawPixels</strong> décale chaque index à virgule fixe laissé par GL_INDEX_SHIFT bits et l’ajoute à GL_INDEX_OFFSET. Si GL_INDEX_SHIFT est négatif, le décalage est à droite. Dans les deux cas, zéro bits remplit les emplacements de bits non spécifiés dans le résultat.</li>
<li>En mode RVBA, <strong>glDrawPixels</strong> convertit l’index résultant en un pixel RVBA à l’aide des tables GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B et GL_PIXEL_MAP_I_TO_A. Dans le mode d’index des couleurs et GL_MAP_COLOR a la valeur true, l’index est remplacé par la valeur que <strong>glDrawPixels</strong> référence dans la table de recherche GL_PIXEL_MAP_I_TO_I.</li>
<li>Que le remplacement de la recherche de l’index soit effectué ou non, la partie entière de l’index est <strong>et</strong>Ed avec 2<sup>b</sup> - 1, où <em>b</em> est le nombre de bits dans une mémoire tampon d’index de couleurs.</li>
<li>Les index résultants ou les couleurs RVBA sont ensuite convertis en fragments en attachant les coordonnées z-coordonnée <em>z</em>et de texture de la position raster actuelle à chaque pixel, puis en affectant les coordonnées de la fenêtre <em>x</em> et <em>y</em> au <em>n</em>ième fragment, de telle sorte que <em>x</em>? = <em>x</em><sub>r</sub> + <em>n</em> mod <em>largeur</em><br/> <em>y</em>? = <em></em><sub>r</sub> + <em>n/largeur</em> o<br/> où (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) est la position de la trame actuelle.<br/></li>
<li>La fonction <strong>glDrawPixels</strong> traite ces fragments de pixel comme les fragments générés par la pixellisation des points, des lignes ou des polygones. Il applique le mappage de texture, le brouillard et toutes les opérations de fragment avant d’écrire les fragments dans le trame.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt><strong>GL_STENCIL_INDEX</strong></dt> </dl></td>
<td>Chaque pixel est une valeur unique, un index de stencil. <br/>
<ol>
<li>La fonction <strong>glDrawPixels</strong> la convertit au format à virgule fixe, avec un nombre non spécifié de bits à droite du point binaire, quel que soit le type de données de mémoire. Les valeurs à virgule flottante sont converties en valeurs à virgule fixe vraies. La fonction <strong>glDrawPixels</strong> convertit les données entières signées et non signées avec tous les bits de fraction définis sur zéro. Les données bitmap sont converties en 0,0 ou 1,0.</li>
<li>La fonction <strong>glDrawPixels</strong> décale chaque index à virgule fixe laissé par GL_INDEX_SHIFT bits et l’ajoute à GL_INDEX_OFFSET. Si GL_INDEX_SHIFT est négatif, le décalage est à droite. Dans les deux cas, zéro bits remplit les emplacements de bits non spécifiés dans le résultat.</li>
<li>Si GL_MAP_STENCIL a la valeur true, l’index est remplacé par la valeur que <strong>glDrawPixels</strong> référence dans la table de recherche GL_PIXEL_MAP_S_TO_S.</li>
<li>Que le remplacement de la recherche de l’index soit effectué ou non, la partie entière de l’index est ensuite <strong>et</strong>Ed avec 2<sup>b</sup> - 1, où <em>b</em> est le nombre de bits dans la mémoire tampon du stencil. Les index de stencil résultants sont ensuite écrits dans la mémoire tampon de stencil de telle sorte que le <em>n</em>ième index soit écrit dans l’emplacement <em>x</em>? = <em>x</em><sub>r</sub> + <em>n</em> mod <em>largeur</em><br/> <em>y</em>? = <em></em><sub>r</sub> + <em>n/largeur</em> o<br/> où (<em>x</em><sub>r</sub> , <em></em> y<sub>r</sub> ) est la position de la trame actuelle. Seul le test de propriété des pixels, le test de la ciseaux et le stencil writemask affectent ces écritures.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt><strong>GL_DEPTH_COMPONENT</strong></dt> </dl></td>
<td>Chaque pixel est un composant à profondeur unique. <br/>
<ol>
<li>La fonction <strong>glDrawPixels</strong> convertit les données en virgule flottante directement en un format à virgule flottante interne avec une précision non spécifiée. Les données entières signées sont mappées de façon linéaire au format à virgule flottante interne de telle sorte que la valeur entière représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0. Les données entières non signées sont mappées de la même façon : la plus grande valeur entière correspond à 1,0, et zéro est mappé à 0,0.</li>
<li>La fonction <strong>glDrawPixels</strong> multiplie la valeur de profondeur à virgule flottante résultante par GL_DEPTH_SCALE et l’ajoute à GL_DEPTH_BIAS. Le résultat est ancré à la plage [0, 1].</li>
<li>La fonction <strong>glDrawPixels</strong> convertit les composants de profondeur résultants en fragments en joignant la couleur de position raster actuelle ou l’index de couleur et les coordonnées de texture à chaque pixel, puis en affectant les coordonnées de la fenêtre <em>x</em> et <em>y</em> au <em>n</em> ième fragment de telle sorte que <em>x</em>? = <em></em>x<sub>r</sub> + <em>n</em> mod <em>largeur</em><br/> <em>y</em>? = <em></em><sub>r</sub> + <em>n/largeur</em> o<br/> où ( <em></em> x<sub>r</sub> ,<em>y</em><sub>r</sub> ) est la position de la trame actuelle.<br/></li>
<li>Ces fragments de pixels sont ensuite traités comme les fragments générés par la pixellisation des points, des lignes ou des polygones. La fonction <strong>glDrawPixels</strong> applique le mappage de texture, le brouillard et toutes les opérations de fragment avant d’écrire les fragments dans le trame.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt><strong>GL_RGBA</strong></dt> </dl></td>
<td>Chaque pixel est un groupe à quatre composants dans cet ordre : rouge, vert, bleu, alpha. <br/>
<ol>
<li>La fonction <strong>glDrawPixels</strong> convertit les valeurs à virgule flottante directement en un format à virgule flottante interne avec une précision non spécifiée. Les valeurs entières signées sont mappées de façon linéaire au format à virgule flottante interne de telle sorte que la valeur entière représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0. Les données entières non signées sont mappées de la même façon : la plus grande valeur entière correspond à 1,0, et zéro est mappé à 0,0.</li>
<li>La fonction <strong>glDrawPixels</strong> multiplie les valeurs de couleur de virgule flottante résultantes par GL_c_SCALE et les ajoute à GL_c_BIAS, où <em>c</em> est rouge, vert, bleu et alpha pour les composants de couleur respectifs. Les résultats sont ancrés à la plage [0, 1].</li>
<li>Si GL_MAP_COLOR a la valeur true, <strong>glDrawPixels</strong> met à l’échelle chaque composant de couleur en fonction de la taille de la table de recherche GL_PIXEL_MAP_c_TO_c, puis remplace le composant par la valeur qu’il référence dans cette table. <em>c</em> est R, G, B ou a, respectivement.</li>
<li>La fonction <strong>glDrawPixels</strong> convertit les couleurs RVBA obtenues en fragments en attachant la coordonnée <em>z</em>et la coordonnée de texture de la position raster actuelle à chaque pixel, puis en affectant les coordonnées de la fenêtre <em>x</em> et <em>y</em> au <em>n</em>ième fragment, de telle sorte que <em>x</em>? = <em>x</em><sub>r</sub> + <em>n</em> mod <em>largeur</em><br/> <em>y</em>? = <em>o</em><sub>r</sub> + <em>n/Width</em><br/> où (<em>x</em><sub>r</sub> ,<em>y</em><sub>r</sub> ) est la position de la trame actuelle.<br/></li>
<li>Ces fragments de pixels sont ensuite traités comme les fragments générés par la pixellisation des points, des lignes ou des polygones. La fonction <strong>glDrawPixels</strong> applique le mappage de texture, le brouillard et toutes les opérations de fragment avant d’écrire les fragments dans le trame.</li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Chaque pixel est un composant rouge unique.<br/> La fonction <strong>glDrawPixels</strong> convertit ce composant au format à virgule flottante interne de la même façon que le composant rouge d’un pixel RVBA est, puis le convertit en pixel RVBA avec le vert et le bleu réglés sur 0,0 et alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Chaque pixel est un composant vert unique.<br/> La fonction <strong>glDrawPixels</strong> convertit ce composant au format à virgule flottante interne de la même façon que le composant vert d’un pixel RVBA est, puis le convertit en pixel RVBA avec rouge et bleu défini sur 0,0 et alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Chaque pixel est un composant bleu unique.<br/> La fonction <strong>glDrawPixels</strong> convertit ce composant au format à virgule flottante interne de la même façon que le composant bleu d’un pixel RVBA est, puis le convertit en pixel RVBA avec Red et Green défini sur 0,0, et alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Chaque pixel est un composant alpha unique.<br/> La fonction <strong>glDrawPixels</strong> convertit ce composant au format à virgule flottante interne de la même façon que le composant alpha d’un pixel RVBA est, puis le convertit en pixel RVBA avec rouge, vert et bleu défini sur 0,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Chaque pixel est un groupe de trois composants dans cet ordre : rouge, vert, bleu. La fonction <strong>glDrawPixels</strong> convertit chaque composant au format à virgule flottante interne de la même façon que les composants rouge, vert et bleu d’un pixel RVBA. La triple couleur est convertie en un pixel RVBA avec alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt><strong>GL_LUMINANCE</strong></dt> </dl></td>
<td>Chaque pixel est un composant de luminance unique.<br/> La fonction <strong>glDrawPixels</strong> convertit ce composant au format à virgule flottante interne de la même façon que le composant rouge d’un pixel RVBA est, puis le convertit en pixel RVBA avec rouge, vert et bleu défini sur la valeur de luminance convertie, et alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt><strong>GL_LUMINANCE_ALPHA</strong></dt> </dl></td>
<td>Chaque pixel est un groupe de deux composants dans cet ordre : luminance, alpha.<br/> La fonction <strong>glDrawPixels</strong> convertit les deux composants au format à virgule flottante interne de la même façon que le composant rouge d’un pixel RVBA est, puis les convertit en un pixel RVBA avec rouge, vert et bleu défini sur la valeur de luminance convertie, et alpha défini sur la valeur alpha convertie. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Chaque pixel est un groupe de trois composants dans cet ordre : bleu, vert, rouge.<br/> GL_BGR_EXT fournit un format qui correspond à la disposition mémoire des bitmaps indépendants du périphérique Windows (DIB). Ainsi, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>Chaque pixel est un groupe de quatre composants dans l’ordre suivant : bleu, vert, rouge, alpha.<br/> GL_BGRA_EXT fournit un format qui correspond à la disposition mémoire des bitmaps indépendants du périphérique Windows (DIB). Ainsi, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*type* 
</dt> <dd>

Type de données pour les *pixels*. Voici les constantes symboliques acceptées et leurs significations.



| Valeur                                                                                                                                                                      | Signification                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**\_octet non signé GL \_**</dt> </dl>    | Entier 8 bits non signé<br/>                 |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**\_octet GL**</dt> </dl>                                | Entier 8 bits signé<br/>                   |
| <span id="GL_BITMAP"></span><span id="gl_bitmap"></span><dl> <dt>**\_bitmap GL**</dt> </dl>                          | Bits uniques dans les entiers 8 bits non signés<br/> |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**NON signé dans le GL \_ \_**</dt> </dl> | Entier 16 bits non signé<br/>                |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**\_abrégé GL**</dt> </dl>                             | Entier 16 bits signé<br/>                  |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**\_entier non signé GL \_**</dt> </dl>       | Entier 32 bits non signé<br/>                |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ int**</dt> </dl>                                   | Entier de 32 bits<br/>                         |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**valeur \_ float du GL**</dt> </dl>                             | Virgule flottante simple précision<br/>        |



 

</dd> <dt>

*pixels* 
</dt> <dd>

Pointeur vers les données de pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | La *largeur* ou la *hauteur* était négative.<br/>                                                                                                                                          |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | Le *format* ou le *type* n’était pas une valeur acceptée. <br/>                                                                                                                             |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | *format* : GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ alpha, GL \_ RGB, GL \_ RVBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminance ou GL \_ luminance \_ alpha, et OpenGL était en mode d’index des couleurs.<br/> |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *type* est \_ bitmap GL et le *format* n’est pas un index de couleur GL \_ ou un \_ \_ index de stencils GL \_ .<br/>                                                                                         |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | le *format* était \_ un \_ index de stencils GL et il n’existait pas de tampon de stencil.<br/>                                                                                                                  |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/>                                                        |


## <a name="remarks"></a>Notes

La fonction **glDrawPixels** lit les données de pixels de la mémoire et les écrit dans le trame par rapport à la position raster actuelle. Utilisez [**glRasterPos**](glrasterpos-functions.md) pour définir la position raster actuelle et utilisez [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument GL \_ Current \_ Raster \_ position pour interroger la position raster.

Plusieurs paramètres définissent l’encodage des données de pixels en mémoire et contrôlent le traitement des données de pixels avant leur placement dans le trame. Ces paramètres sont définis avec quatre fonctions : [**glPixelStore**](glpixelstore-functions.md), [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)et [**glPixelZoom**](glpixelzoom.md). Cette rubrique décrit les effets sur les **glDrawPixels** de nombreux paramètres spécifiés par ces quatre fonctions.

Les données sont lues à partir de *pixels* comme une séquence d’octets signés ou non signés, des entiers signés ou non signés, des entiers signés ou non signés, ou des valeurs à virgule flottante simple précision, en fonction du *type*. Chacun de ces octets, des shorts, des entiers ou des valeurs à virgule flottante est interprété comme un composant de couleur ou de profondeur, ou un index, en fonction du *format*. Les index sont toujours traités individuellement. Les composants de couleur sont traités comme des groupes d’une, deux, trois ou quatre valeurs, en fonction du *format*. Les index et les groupes de composants individuels sont appelés pixels. Si le *type* est \_ bitmap GL, les données doivent être des octets non signés et le *format* doit être un index de couleur GL \_ ou un \_ \_ index de stencils GL \_ . Chaque octet non signé est traité comme un pixel de 8 1 bits, l’ordonnancement des bits étant déterminé par la \_ première décompression \_ LSB \_ (voir [**glPixelStore**](glpixelstore-functions.md)).

Les pixels de *largeur* par *hauteur* sont lus à partir de la mémoire, en commençant aux *pixels* de l’emplacement. Par défaut, ces pixels proviennent d’emplacements de mémoire adjacents, sauf qu’une fois tous les pixels de la *largeur* lus, le pointeur de lecture est avancé jusqu’à la limite de 4 octets suivante. La fonction **glPixelStore** spécifie l’alignement de ligne sur 4 octets avec l' \_ alignement décompresser l’argument GL \_ , et vous pouvez lui affecter la valeur 1, 2, 4 ou 8 octets. Les autres paramètres de magasin de pixels spécifient des avances de pointeur de lecture différentes, avant la lecture du premier pixel et après la lecture de tous les pixels de *largeur* . La fonction **glPixelStore** opère sur chacun des pixels de *largeur par hauteur* qu’elle lit à partir de la mémoire de la même manière, en fonction des valeurs de plusieurs paramètres spécifiés par [**glPixelTransfer**](glpixeltransfer.md) et [**glPixelMap**](glpixelmap.md). Les détails de ces opérations, ainsi que la mémoire tampon cible dans laquelle les pixels sont dessinés, sont spécifiques au format des pixels, comme spécifié par le *format*.

La pixellisation décrite jusqu’à présent suppose des facteurs de zoom de pixel de 1,0. Si vous utilisez [**glPixelZoom**](glpixelzoom.md) pour modifier les facteurs de zoom de pixel *x* et *y* , les pixels sont convertis en fragments comme suit. Si (*XR, YR*) est la position de la trame actuelle, et qu’un pixel donné se trouve dans la *n* ième colonne et *m* énième ligne du rectangle de pixels, les fragments sont générés pour les pixels dont les centres se trouvent dans le rectangle avec des angles

(*x*<sub>r</sub>  +  *Zoom*? *n*, *y*<sub></sub>  +  *Zoom* r <sub>o</sub> *m*)

(*x*<sub>r</sub>  +  *Zoom*? (*n* + 1), *o*<sub>r</sub>  +  *Zoom*<sub>y</sub> (*m* + 1))

où *Zoom*? est la valeur de zoom \_ GL \_ X et *Zoom*<sub>y</sub> est la valeur de \_ Zoom GL \_ y.

Les fonctions suivantes récupèrent les informations relatives à **glDrawPixels**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ position

**glGet** avec argument GL \_ Current \_ Raster \_ position \_ valide

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothèque<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





