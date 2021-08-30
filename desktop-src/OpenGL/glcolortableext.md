---
title: fonction glColorTableEXT (GL. h)
description: La fonction glColorTableEXT spécifie le format et la taille d’une palette pour les textures de palette ciblées.
ms.assetid: f3d7b1a1-97a5-47ef-a0ca-5e58acb86bb4
keywords:
- glColorTableEXT fonction OpenGL
topic_type:
- apiref
api_name:
- glColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f42a0be9d2cd9b39a86a9f55d776c61b25fa448
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475375"
---
# <a name="glcolortableext-function"></a>glColorTableEXT fonction)

La fonction **glColorTableEXT** spécifie le format et la taille d’une palette pour les textures de palette ciblées.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glColorTableEXT(
         GLenum  target,
         GLenum  internalFormat,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Texture cible dont la palette doit être modifiée. Doit être une TEXTURE \_ 1D, une texture \_ 2D, une texture de proxy \_ \_ 1D ou une texture de proxy \_ \_ 2D.

</dd> <dt>

*internalFormat* 
</dt> <dd>

Format interne et résolution de la palette. Ce paramètre peut prendre l’une des valeurs symboliques suivantes.



| Constante       | Format de base | Bits R | Bits G | Bits B | Un bits |
|----------------|-------------|--------|--------|--------|--------|
| GL \_ R3 \_ G3 \_ a2 | \_RGB GL     | 3      | 3      | 2      |        |
| \_RGB4 GL       | \_RGB GL     | 4      | 4      | 4      |        |
| \_RGB5 GL       | \_RGB GL     | 5      | 5      | 5      |        |
| \_RGB8 GL       | \_RGB GL     | 8      | 8      | 8      |        |
| \_RGB10 GL      | \_RGB GL     | 10     | 10     | 10     |        |
| \_RGB12 GL      | \_RGB GL     | 12     | 12     | 12     |        |
| \_RGB16 GL      | \_RGB GL     | 16     | 16     | 16     |        |
| \_RGBA2 GL      | GL \_ RVBA    | 2      | 2      | 2      | 2      |
| \_RGBA4 GL      | GL \_ RVBA    | 4      | 4      | 4      | 4      |
| GL \_ RGB5 \_ a1   | GL \_ RVBA    | 5      | 5      | 5      | 1      |
| \_RGBA8 GL      | GL \_ RVBA    | 8      | 8      | 8      | 8      |
| GL \_ RG10 \_ a2   | GL \_ RVBA    | 10     | 10     | 10     | 2      |
| \_RGB12 GL      | GL \_ RVBA    | 12     | 12     | 12     | 12     |
| \_RGBA16 GL     | GL \_ RVBA    | 16     | 16     | 16     | 16     |



 

</dd> <dt>

*width* 
</dt> <dd>

Taille de la palette. Doit être 2n = 1 pour un entier *n*.

</dd> <dt>

*format* 
</dt> <dd>

Format des données de pixels. Les constantes symboliques suivantes sont acceptées.




| Valeur | Signification | 
|-------|---------|
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl><dt><strong>GL_RGBA</strong></dt></dl> | Chaque pixel est un groupe de quatre composants dans cet ordre : rouge, vert, bleu, alpha. Le format RVBA est déterminé de la façon suivante : <br /><ol><li>La fonction <strong>glColorTableEXT</strong> convertit les valeurs à virgule flottante directement en un format interne avec une précision non spécifiée. Les valeurs entières signées sont mappées de façon linéaire au format interne de telle sorte que la valeur entière représentable la plus positive corresponde à 1,0, et la valeur entière représentable la plus négative correspond à-1,0. Les données entières non signées sont mappées de la même façon : la plus grande valeur entière correspond à 1,0, et zéro est mappé à 0,0.</li><li>La fonction <strong>glColorTableEXT</strong> multiplie les valeurs de couleur résultantes par GL_c_SCALE et les ajoute à GL_c_BIAS, où <em>c</em> est rouge, vert, bleu et alpha pour les composants de couleur respectifs. Les résultats sont ancrés à la plage [0, 1].</li><li>Si GL_MAP_COLOR a la <strong>valeur true</strong>, <strong>glColorTableEXT</strong> met à l’échelle chaque composant de couleur en fonction de la taille de la table de recherche GL_PIXEL_MAP_c_TO_c, puis remplace le composant par la valeur qu’il référence dans cette table. <em>c</em> est R, G, B ou a, respectivement.</li><li>La fonction <strong>glColorTableEXT</strong> convertit les couleurs RVBA obtenues en fragments en attachant la coordonnée <em>z</em>et la coordonnée de texture de la position raster actuelle à chaque pixel, puis en affectant les coordonnées de la fenêtre <em>x</em> et <em>y</em> au <em>n</em>ième fragment, de telle sorte que<em>x</em>? = <em>x</em><sub>r</sub>  +  <em>n</em> mod <em>largeur</em><br /><em></em>y? = <em></em><sub>r</sub>  + <em>n/largeur</em> o<br /> où (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) est la position de la trame actuelle.<br /></li><li>Ces fragments de pixels sont ensuite traités comme les fragments générés par la pixellisation des points, des lignes ou des polygones. La fonction <strong>glColorTableEXT</strong> applique le mappage de texture, le brouillard et toutes les opérations de fragment avant d’écrire les fragments dans le trame.</li></ol> | 
| <span id="GL_RED"></span><span id="gl_red"></span><dl><dt><strong>GL_RED</strong></dt></dl> | Chaque pixel est un composant rouge unique.<br /> La fonction <strong>glColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant rouge d’un pixel RVBA est, puis le convertit en pixel RVBA avec le vert et le bleu réglés sur 0,0 et alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl><dt><strong>GL_GREEN</strong></dt></dl> | Chaque pixel est un composant vert unique.<br /> La fonction <strong>glColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant vert d’un pixel RVBA est, puis le convertit en pixel RVBA avec rouge et bleu défini sur 0,0, et alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl><dt><strong>GL_BLUE</strong></dt></dl> | Chaque pixel est un composant bleu unique.<br /> La fonction <strong>glColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant bleu d’un pixel RVBA est, puis le convertit en pixel RVBA avec Red et Green défini sur 0,0, et alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl><dt><strong>GL_ALPHA</strong></dt></dl> | Chaque pixel est un composant alpha unique.<br /> La fonction <strong>glColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant alpha d’un pixel RVBA est, puis le convertit en un pixel RVBA avec rouge, vert et bleu défini sur 0,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl><dt><strong>GL_RGB</strong></dt></dl> | Chaque pixel est un groupe de trois composants dans cet ordre : rouge, vert, bleu.<br /> La fonction <strong>glColorTableEXT</strong> convertit chaque composant au format interne de la même façon que les composants rouge, vert et bleu d’un pixel RVBA. La triple couleur est convertie en un pixel RVBA avec alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl><dt><strong>GL_BGR_EXT</strong></dt></dl> | Chaque pixel est un groupe de trois composants dans cet ordre : bleu, vert, rouge.<br /> GL_BGR_EXT fournit un format qui correspond à la disposition de la mémoire des Windows des bitmaps indépendantes du périphérique (dib). par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.<br /> | 
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl><dt><strong>GL_BGRA_EXT</strong></dt></dl> | Chaque pixel est un groupe de quatre composants dans l’ordre suivant : bleu, vert, rouge, alpha.<br /> GL_BGRA_EXT fournit un format qui correspond à la disposition de la mémoire des Windows des bitmaps indépendantes du périphérique (dib). par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.<br /> | 




 

</dd> <dt>

*type* 
</dt> <dd>

Type de données pour les *données*. Les constantes symboliques suivantes sont acceptées : \_ octet non signé GL \_ , \_ octet GL, GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int et GL \_ float.

Le tableau suivant résume la signification des constantes valides pour le paramètre de *type* .



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

Pointeur vers les données de texture de palette. Les données sont traitées comme des pixels uniques d’une entrée de palette de texture 1D pour une entrée de palette.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *largeur* était un entier non valide.<br/>                                                                                            |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *target*, *internalFormat*, *format* ou *type* n’est pas une valeur acceptée.<br/>                                                 |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

Les textures de palette sont définies à l’aide d’une palette de couleurs et d’un ensemble de données d’image composé d’index pour les entrées de couleur d’une palette (une table des couleurs).

La fonction **glColorTableEXT** spécifie la palette de texture d’une texture ciblée. Il récupère les *données* de la mémoire et convertit les données comme si chaque entrée de palette était un pixel unique d’une texture 1D. La fonction **glColorTableEXT** décompresse et convertit les données et les convertit dans un format interne qui correspond le mieux au *format* donné.

Si la *largeur* d’une palette est supérieure à la plage d’index de couleurs dans les données de texture, certaines entrées de palette ne sont pas utilisées. Si la *largeur* d’une palette est inférieure à la plage des index de couleurs dans les données de texture, les bits les plus significatifs des données de texture sont ignorés et seul le nombre approprié de bits dans l’index est utilisé lors de l’accès à la palette. Lorsque vous spécifiez une *cible* de proxy à l’aide de la \_ texture \_ de proxy 1D ou \_ de la texture de proxy \_ 2D, la palette de la texture du proxy est redimensionnée et ses paramètres sont définis, mais aucune donnée n’est transférée ou accessible.

Lorsque le paramètre *cible* est \_ une texture \_ de proxy de GL \_ 1D ou \_ une texture de proxy GL \_ \_ 2D, et que l’implémentation ne prend pas en charge les valeurs spécifiées pour le *format* ou la *largeur*, **glColorTableEXT** peut ne pas réussir à créer la table de couleurs demandée. Dans ce cas, la table des couleurs est vide et tous les paramètres récupérés sont nuls. Vous pouvez déterminer si OpenGL prend en charge un format et une taille de table de couleur particuliers en appelant **glColorTableEXT** avec une cible de proxy, puis en appelant [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) ou [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) pour déterminer si le paramètre Width correspond à celui défini par **glColorTableEXT**. Si la largeur Récupérée est égale à zéro, la requête de la table de couleurs par **glColorTable** a échoué. Si la largeur Récupérée n’est pas égale à zéro, vous pouvez appeler **glColorTable** avec la cible réelle avec la texture \_ 1D ou texture \_ 2D pour définir la table des couleurs.

> [!Note]  
> La fonction **glColorTableEXT** est une fonction d’extension qui ne fait pas partie de la bibliothèque OpenGL standard, mais qui fait partie de l' \_ extension de texture de palette ext GL \_ \_ . Pour vérifier si votre implémentation d’OpenGL prend en charge **glColorTableEXT**, appelez [**glGetString**](glgetstring.md)( \_ Extensions GL). Si elle retourne la \_ \_ texture de palette ext GL \_ , **glColorTableEXT** est pris en charge. Pour obtenir l’adresse de fonction d’une fonction d’extension, appelez [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

 

Pour récupérer les données de la table des couleurs réelles spécifiées par la fonction **glColorTableEXT** , appelez [**glGetColorTableEXT**](glgetcolortableext.md). Pour récupérer les paramètres, tels que la *largeur* et le *format*, de la table de couleurs spécifiée par la fonction **GlColorTableEXT** , appelez la fonction **glGetColorTableParameterivEXT** ou **glGetColorTableParameterfvEXT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





