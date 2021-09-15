---
title: fonction glColorSubTableEXT (GL. h)
description: La fonction glColorSubTableEXT spécifie une partie de la palette de la texture ciblée à remplacer.
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- glColorSubTableEXT fonction OpenGL
topic_type:
- apiref
api_name:
- glColorSubTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff6f4b88a355c25df40a847912d4e3352bd87962
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311833"
---
# <a name="glcolorsubtableext-function"></a>glColorSubTableEXT fonction)

La fonction **glColorSubTableEXT** spécifie une partie de la palette de la texture ciblée à remplacer.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glColorSubTableEXT(
         GLenum  target,
         GLsizei start,
         GLsizei count,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Texture de palette cible dont la palette doit être modifiée. Doit être une TEXTURE \_ 1D ou une texture \_ 2D.

</dd> <dt>

*start* 
</dt> <dd>

Entrée d’index de la palette de départ de la palette à modifier.

</dd> <dt>

*count* 
</dt> <dd>

Nombre d’entrées d’index de palette de la palette à modifier à partir du *début*. Le paramètre *Count* détermine la plage d’entrées d’index de palette qui sont modifiées.

</dd> <dt>

*format* 
</dt> <dd>

Format des données de pixels. Les constantes symboliques suivantes sont acceptées.




| Valeur | Signification | 
|-------|---------|
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl><dt><strong>GL_RGBA</strong></dt></dl> | Chaque pixel est un groupe de quatre composants dans l’ordre suivant : rouge, vert, bleu, alpha. Le format RVBA est déterminé de la façon suivante : <br /><ol><li>La fonction <strong>glColorSubTableEXT</strong> convertit les valeurs à virgule flottante directement en un format interne avec une précision non spécifiée. Les valeurs entières signées sont mappées de façon linéaire au format interne, de sorte que la valeur entière représentable la plus positive correspond à 1,0, et la valeur représentable la plus négative correspond à-1,0. Les données entières non signées sont mappées de la même façon : la plus grande valeur entière correspond à 1,0, et zéro est mappé à 0,0.</li><li>La fonction <strong>glColorSubTableEXT</strong> multiplie les valeurs de couleur résultantes par GL_c_SCALE et les ajoute à GL_c_BIAS, où <em>c</em> est rouge, vert, bleu et alpha pour les composants de couleur respectifs. Les résultats sont ancrés à la plage [0, 1].</li><li>Si GL_MAP_COLOR a la <strong>valeur true</strong>, <strong>glColorSubTableEXT</strong> met à l’échelle chaque composant de couleur en fonction de la taille de la table de recherche GL_PIXEL_MAP_c_TO_c, puis remplace le composant par la valeur qu’il référence dans cette table. <em>c</em> est R, G, B ou a, respectivement.</li><li>La fonction <strong>glColorSubTableEXT</strong> convertit les couleurs RVBA obtenues en fragments en attachant la coordonnée <em>z</em>et la coordonnée de texture de la position raster actuelle à chaque pixel, puis en affectant les coordonnées de la fenêtre <em>x</em> et <em>y</em> au <em>n</em>ième fragment, de telle sorte que<em>x</em>? = <em>x</em><sub>r</sub>  +  <em>n</em> mod <em>largeur</em><br /><em>y</em>? = <em></em><sub>r</sub>  + <em>n/largeur</em> o<br /> où (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) est la position de la trame actuelle.<br /></li><li>Ces fragments de pixels sont ensuite traités comme les fragments générés par la pixellisation des points, des lignes ou des polygones. La fonction <strong>glColorSubTableEXT</strong> applique le mappage de texture, le brouillard et toutes les opérations de fragment avant d’écrire les fragments dans le trame.</li></ol> | 
| <span id="GL_RED"></span><span id="gl_red"></span><dl><dt><strong>GL_RED</strong></dt></dl> | Chaque pixel est un composant rouge unique.<br /> La fonction <strong>glColorSubTableEXT</strong> convertit ce composant au format interne de la même façon que le composant rouge d’un pixel RVBA est, puis le convertit en pixel RVBA avec le vert et le bleu réglés sur 0,0 et alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl><dt><strong>GL_GREEN</strong></dt></dl> | Chaque pixel est un composant vert unique.<br /> La fonction <strong>glColorSubTableEXT</strong> convertit ce composant au format interne de la même façon que le composant vert d’un pixel RVBA est, puis le convertit en pixel RVBA avec rouge et bleu défini sur 0,0, et alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl><dt><strong>GL_BLUE</strong></dt></dl> | Chaque pixel est un composant bleu unique.<br /> La fonction <strong>glColorSubTableEXT</strong> convertit ce composant au format interne de la même façon que le composant bleu d’un pixel RVBA est, puis le convertit en pixel RVBA avec Red et Green défini sur 0,0, et alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl><dt><strong>GL_ALPHA</strong></dt></dl> | Chaque pixel est un composant alpha unique.<br /> La fonction <strong>glColorSubTableEXT</strong> convertit ce composant au format interne de la même façon que le composant alpha d’un pixel RVBA est, puis le convertit en un pixel RVBA avec rouge, vert et bleu défini sur 0,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl><dt><strong>GL_RGB</strong></dt></dl> | Chaque pixel est un groupe de trois composants dans cet ordre : rouge, vert, bleu.<br /> La fonction <strong>glColorSubTableEXT</strong> convertit chaque composant au format interne de la même façon que les composants rouge, vert et bleu d’un pixel RVBA. La triple couleur est convertie en un pixel RVBA avec alpha défini sur 1,0. Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.<br /> | 
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



| Nom                                                                                              | Signification                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl> | *Start* ou *Count* était un entier non valide.<br/>                                                                                 |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>  | la *cible*, le *format* ou le *type* n’était pas une valeur acceptée.<br/>                                                                    |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glColorSubTableEXT** spécifie des parties de la palette de la texture ciblée actuelle à remplacer. Contrairement à [**glColorTableEXT**](glcolortableext.md), vous ne pouvez pas spécifier le paramètre *target* comme une palette de texture de proxy.

> [!Note]  
> La fonction **glColorSubTableEXT** est une fonction d’extension qui ne fait pas partie de la bibliothèque OpenGL standard, mais qui fait partie de l' \_ extension de texture de palette ext GL \_ \_ . Pour vérifier si votre implémentation d’OpenGL prend en charge **glColorSubTableEXT**, appelez [**glGetString**](glgetstring.md)( \_ Extensions GL). Si elle retourne la \_ \_ texture de palette ext GL \_ , **glColorSubTableEXT** est pris en charge. Pour obtenir l’adresse de fonction d’une fonction d’extension, appelez [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





