---
title: fonction glGetColorTableEXT (GL. h)
description: La fonction glGetColorTableEXT obtient les données de la table des couleurs de la palette de texture ciblée actuelle.
ms.assetid: 9169c4e1-a22e-48fe-bd45-4549c1a10ff0
keywords:
- glGetColorTableEXT fonction OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46593ac7b03781288d7d0d3932ced799dbbdfcff
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469626"
---
# <a name="glgetcolortableext-function"></a>glGetColorTableEXT fonction)

La fonction **glGetColorTableEXT** obtient les données de la table des couleurs de la palette de texture ciblée actuelle.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetColorTableEXT(
         GLenum target,
         GLenum format,
         GLenum type,
   const GLvoid *data
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Texture cible dont la palette doit être modifiée. Doit être une TEXTURE \_ 1D ou une texture \_ 2D.

</dd> <dt>

*format* 
</dt> <dd>

Format des données de pixels. Les constantes symboliques suivantes sont acceptées.




| Valeur | Signification | 
|-------|---------|
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl><dt><strong>GL_RGBA</strong></dt></dl> | Chaque pixel est un groupe de quatre composants dans l’ordre suivant : rouge, vert, bleu, alpha. Le format RVBA est déterminé de la façon suivante : <br /><ol><li>La fonction <strong>glGetColorTableEXT</strong> convertit les valeurs à virgule flottante directement en un format interne avec une précision non spécifiée. Les valeurs entières signées sont mappées de façon linéaire au format interne de telle sorte que la valeur entière représentable la plus positive corresponde à 1,0, et la valeur entière représentable la plus négative correspond à-1,0. Les données entières non signées sont mappées de la même façon : la plus grande valeur entière correspond à 1,0, et zéro est mappé à 0,0.</li><li>La fonction <strong>glGetColorTableEXT</strong> multiplie les valeurs de couleur résultantes par GL_c_SCALE et les ajoute à GL_c_BIAS, où <em>c</em> est rouge, vert, bleu et alpha pour les composants de couleur respectifs. Les résultats sont ancrés à la plage [0, 1].</li><li>Si GL_MAP_COLOR a la <strong>valeur true</strong>, <strong>glGetColorTableEXT</strong> met à l’échelle chaque composant de couleur en fonction de la taille de la table de recherche GL_PIXEL_MAP_c_TO_c, puis remplace le composant par la valeur qu’il référence dans cette table. <em>c</em> est R, G, B ou a, respectivement.</li><li>La fonction <strong>glGetColorTableEXT</strong> convertit les couleurs RVBA obtenues en fragments en attachant la coordonnée z et la coordonnée de texture de la position raster actuelle à chaque pixel, puis en affectant les coordonnées de la fenêtre <em>x</em> et <em>y</em> au <em>n</em>ième fragment, par exemple <em>x</em>? = <em>x</em><sub>r</sub>  +  <em>n</em> mod <em>largeur</em><br /><em>y</em>? = <em></em><sub>r</sub>  +  <em>n/largeur</em> o<br /> où (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) est la position de la trame actuelle.<br /></li><li>Ces fragments de pixels sont ensuite traités comme les fragments générés par la pixellisation des points, des lignes ou des polygones. La fonction <strong>glGetColorTableEXT</strong> applique le mappage de texture, le brouillard et toutes les opérations de fragment avant d’écrire les fragments dans le trame.</li></ol> | 
| <span id="GL_RED"></span><span id="gl_red"></span><dl><dt><strong>GL_RED</strong></dt></dl> | Chaque pixel est un composant rouge unique.<br /> La fonction <strong>glGetColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant rouge d’un pixel RVBA est, puis le convertit en pixel RVBA avec le vert et le bleu réglés sur 0,0 et alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl><dt><strong>GL_GREEN</strong></dt></dl> | Chaque pixel est un composant vert unique.<br /> La fonction <strong>glGetColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant vert d’un pixel RVBA est, puis le convertit en pixel RVBA avec rouge et bleu défini sur 0,0, et alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl><dt><strong>GL_BLUE</strong></dt></dl> | Chaque pixel est un composant bleu unique.<br /> La fonction <strong>glGetColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant bleu d’un pixel RVBA est, puis le convertit en pixel RVBA avec Red et Green défini sur 0,0, et alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl><dt><strong>GL_ALPHA</strong></dt></dl> | Chaque pixel est un composant alpha unique.<br /> La fonction <strong>glGetColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant alpha d’un pixel RVBA est, puis le convertit en un pixel RVBA avec rouge, vert et bleu défini sur 0,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl><dt><strong>GL_RGB</strong></dt></dl> | Chaque pixel est un groupe de trois composants dans cet ordre : rouge, vert, bleu.<br /> La fonction <strong>glGetColorTableEXT</strong> convertit chaque composant au format interne de la même façon que les composants rouge, vert et bleu d’un pixel RVBA. La triple couleur est convertie en un pixel RVBA avec alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl><dt><strong>GL_BGR_EXT</strong></dt></dl> | Chaque pixel est un groupe de trois composants dans cet ordre : bleu, vert, rouge.<br /> GL_BGR_EXT fournit un format qui correspond à la disposition mémoire des bitmaps indépendantes du périphérique (dib) de Microsoft Windows. ainsi, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.<br /> | 
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl><dt><strong>GL_BGRA_EXT</strong></dt></dl> | Chaque pixel est un groupe de quatre composants dans l’ordre suivant : bleu, vert, rouge, alpha.<br /> GL_BGRA_EXT fournit un format qui correspond à la disposition de la mémoire des Windows des bitmaps indépendantes du périphérique (dib). par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.<br /> | 




 

</dd> <dt>

*type* 
</dt> <dd>

Type de données pour les *données*. Voici les constantes symboliques acceptées et leurs significations.



| Valeur                                                                                                                                                                      | Signification                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**\_octet non signé GL \_**</dt> </dl>    | Entier 8 bits non signé<br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**\_octet GL**</dt> </dl>                                | Entier 8 bits signé<br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**NON signé dans le GL \_ \_**</dt> </dl> | Entier 16 bits non signé<br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**\_abrégé GL**</dt> </dl>                             | Entier 16 bits signé<br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**\_entier non signé GL \_**</dt> </dl>       | Entier 32 bits non signé<br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ int**</dt> </dl>                                   | Entier de 32 bits<br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**valeur \_ float du GL**</dt> </dl>                             | Valeur à virgule flottante simple précision<br/> |



 

</dd> <dt>

*data* 
</dt> <dd>

Pointe vers l’emplacement où les informations de table des couleurs retournées doivent être stockées. Chaque entrée de table des couleurs est stockée comme s’il s’agissait d’un pixel unique d’une texture 1D. Étant donné que toutes les textures ont une palette par défaut, **glGetColorTableEXT** retourne toujours les informations de palette même si les données de texture ne sont pas dans un format de palette.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | la *cible*, le *format* ou le *type* n’était pas une valeur acceptée.<br/>                                                                   |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glGetColorTableEXT** obtient les données de la table des couleurs réelles spécifiées par [**glColorTableEXT**](glcolortableext.md) et [**glColorSubTableEXT**](glcolorsubtableext.md).

La fonction **glGetColorTableEXT** est une fonction d’extension qui ne fait pas partie de la bibliothèque OpenGL standard, mais qui fait partie de l' \_ extension de texture de palette ext GL \_ \_ . Pour vérifier si votre implémentation d’OpenGL prend en charge **glGetColorTableEXT**, appelez [**glGetString**](glgetstring.md)( \_ Extensions GL). Si elle retourne la \_ \_ texture de palette ext GL \_ , **glGetColorTableEXT** est pris en charge. Pour obtenir l’adresse de fonction d’une fonction d’extension, appelez [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





