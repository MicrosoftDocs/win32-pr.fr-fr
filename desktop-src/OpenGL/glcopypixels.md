---
title: fonction glCopyPixels (GL. h)
description: La fonction glCopyPixels copie les pixels dans le trame.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- glCopyPixels fonction OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43c399b4ce63f84c41bcb2d65140356ac20a6ddd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311825"
---
# <a name="glcopypixels-function"></a>glCopyPixels fonction)

La fonction **glCopyPixels** copie les pixels dans le trame.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*x* 
</dt> <dd>

Coordonnée du plan x de la fenêtre du coin inférieur gauche de la zone rectangulaire de pixels à copier.

</dd> <dt>

*y* 
</dt> <dd>

Coordonnée du plan y de la fenêtre du coin inférieur gauche de la zone rectangulaire de pixels à copier.

</dd> <dt>

*width* 
</dt> <dd>

Dimension de largeur de la zone rectangulaire de pixels à copier. Il ne doit pas être négatif.

</dd> <dt>

*height* 
</dt> <dd>

Dimension de la hauteur de la zone rectangulaire de pixels à copier. Il ne doit pas être négatif.

</dd> <dt>

*type* 
</dt> <dd>

Spécifie si **glCopyPixels** doit copier les valeurs de couleur, les valeurs de profondeur ou les valeurs de gabarit. Les constantes symboliques acceptées sont.




| Valeur | Signification | 
|-------|---------|
| <span id="GL_COLOR"></span><span id="gl_color"></span><dl><dt><strong>GL_COLOR</strong></dt></dl> | La fonction <strong>glCopyPixels</strong> lit les index ou les couleurs RVBA à partir de la mémoire tampon actuellement spécifiée comme mémoire tampon de la source de lecture (voir <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>). <br /> Si OpenGL est en mode d’index des couleurs :<br /><ol><li>Chaque index lu à partir de cette mémoire tampon est converti en un format à virgule fixe avec un nombre non spécifié de bits à droite du point binaire.</li><li>Chaque index est décalé vers la gauche de GL_INDEX_SHIFT bits et ajouté à GL_INDEX_OFFSET. Si GL_INDEX_SHIFT est négatif, le décalage est à droite. Dans les deux cas, zéro bits remplit les emplacements de bits non spécifiés dans le résultat.<br /></li><li>Si GL_MAP_COLOR a la valeur true, l’index est remplacé par la valeur qu’il référence dans la GL_PIXEL_MAP_I_TO_I de la table de recherche.</li><li>Que le remplacement de la recherche de l’index soit effectué ou non, la partie entière de l’index est ensuite <strong>et</strong>Ed avec 2<em><sup>b</sup></em> 1, où <em>b</em> est le nombre de bits dans une mémoire tampon d’index de couleurs.</li></ol>Si OpenGL est en mode RVBA :<br /><ol><li>Les composants rouge, vert, bleu et alpha de chaque pixel lu sont convertis en un format à virgule flottante interne avec une précision non spécifiée.</li><li>La conversion mappe la plus grande valeur de composant représentable à 1,0, et la valeur de composant zéro à 0,0.</li><li>Les valeurs de couleur à virgule flottante résultantes sont ensuite multipliées par GL_c_SCALE et ajoutées à GL_c_BIAS, où <em>c</em> est rouge, vert, bleu et alpha pour les composants de couleur respectifs.</li><li>Les résultats sont ancrés à la plage [0, 1].</li><li>Si GL_MAP_COLOR a la valeur true, chaque composant de couleur est mis à l’échelle en fonction de la taille de la table de recherche GL_PIXEL_MAP_c_TO_c, puis remplacé par la valeur qu’il référence dans cette table. <em>c</em> est R, G, B ou a, respectivement. Les index résultants ou les couleurs RVBA sont ensuite convertis en fragments en attachant la coordonnée <em>z</em>et les coordonnées de texture de la position de pixellisation actuelle à chaque pixel, puis en affectant les coordonnées de la fenêtre (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub>  +  <em>j</em>), où (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) est la position de la trame <em></em> actuelle et le pixel dans la ligne <em>j</em> Ces fragments de pixels sont ensuite traités comme les fragments générés par la pixellisation des points, des lignes ou des polygones. Le mappage de texture, le brouillard et toutes les opérations de fragment sont appliqués avant que les fragments soient écrits dans le trame.<br /></li></ol> | 
| <span id="GL_DEPTH"></span><span id="gl_depth"></span><dl><dt><strong>GL_DEPTH</strong></dt></dl> | Les valeurs de profondeur sont lues à partir de la mémoire tampon de profondeur et converties directement en un format à virgule flottante interne avec une précision non spécifiée. La valeur de profondeur à virgule flottante résultante est ensuite multipliée par GL_DEPTH_SCALE et ajoutée à GL_DEPTH_BIAS. Le résultat est ancré à la plage [0, 1]. <br /> Les composants de profondeur résultants sont ensuite convertis en fragments en joignant la couleur de position raster actuelle ou l’index de couleur et les coordonnées de texture à chaque pixel, puis en affectant les coordonnées de la fenêtre (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub>  +  <em>j</em>), où (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) est la position de la trame actuelle, et le pixel dans <em>la</em> ligne <em>j</em> . Ces fragments de pixels sont ensuite traités comme les fragments générés par la pixellisation des points, des lignes ou des polygones. Le mappage de texture, le brouillard et toutes les opérations de fragment sont appliqués avant que les fragments soient écrits dans le trame.<br /> | 
| <span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl><dt><strong>GL_STENCIL</strong></dt></dl> | Les index de stencil sont lus à partir de la mémoire tampon de stencil et convertis en un format à virgule fixe interne avec un nombre non spécifié de bits à droite du point binaire. Chaque index à virgule fixe est ensuite déplacé vers la gauche par GL_INDEX_SHIFT bits et ajouté à GL_INDEX_OFFSET. Si GL_INDEX_SHIFT est négatif, le décalage est à droite. Dans les deux cas, zéro bits remplit les emplacements de bits non spécifiés dans le résultat. Si GL_MAP_STENCIL a la valeur true, l’index est remplacé par la valeur qu’il référence dans la GL_PIXEL_MAP_S_TO_S de la table de recherche. Que le remplacement de la recherche de l’index soit effectué ou non, la partie entière de l’index est ensuite <strong>et</strong>Ed avec 2<sup>b</sup> -1, où <em>b</em> est le nombre de bits dans la mémoire tampon du stencil. Les index de stencil qui en résultent sont ensuite écrits dans la mémoire tampon de stencil de telle sorte que l’index lu à partir de l’emplacement <em>i</em> de la ligne <em>j</em> soit écrit dans l’emplacement (<em>x</em><sub>r</sub>  +  <em>i</em>, <em>y</em><sub>r</sub>  +  <em>j</em>), où (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) est la position raster actuelle. Seul le test de propriété en pixels, le test de ciseaux et le stencil writemask affectent ces écritures.<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *type* n’est pas une valeur acceptée.<br/>                                                                                          |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | La *largeur* ou la hauteur était négative.<br/>                                                                                     |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | le *type* était \_ profondeur GL et il n’existait pas de mémoire tampon de profondeur.<br/>                                                                        |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | le *type* était \_ stencil GL et il n’existait pas de tampon de stencil.<br/>                                                                    |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glCopyPixels** copie un rectangle de pixels aligné à l’écran, de l’emplacement trame spécifié vers une région relative à la position raster actuelle. Son fonctionnement est bien défini uniquement si la région source de pixel entière se trouve dans la partie exposée de la fenêtre. Les résultats des copies en dehors de la fenêtre, ou à partir des régions de la fenêtre qui ne sont pas exposées, sont dépendants du matériel et non définis.

Les paramètres *x* et *y* spécifient les coordonnées de la fenêtre du coin inférieur gauche de la zone rectangulaire à copier. Les paramètres de *largeur* et de *hauteur* spécifient les dimensions de la zone rectangulaire à copier. La *largeur* et la *hauteur* ne doivent pas être négatives.

Plusieurs paramètres contrôlent le traitement des données de pixels pendant qu’elles sont copiées. Ces paramètres sont définis avec trois fonctions : [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)et [**glPixelZoom**](glpixelzoom.md). Cette rubrique décrit les effets sur les **glCopyPixels** de la plupart des paramètres spécifiés par ces trois fonctions, mais pas tous.

La fonction **glCopyPixels** copie les valeurs de chaque pixel avec l’angle inférieur gauche à (*x*  +  *i*, *y*  +  *j*) pour 0 = *i*  <  *largeur* et 0 =   <  *hauteur* j. Ce pixel est considéré comme le pixel *i* de la ligne *j* . Les pixels sont copiés dans l’ordre des lignes de la plus petite à la ligne la plus élevée, de gauche à droite dans chaque ligne.

Le paramètre de *type* spécifie si les données de couleur, de profondeur ou de gabarit doivent être copiées.

La pixellisation décrite jusqu’à présent suppose des facteurs de zoom de pixel de 1,0. Si vous utilisez [**glPixelZoom**](glpixelzoom.md) pour modifier les facteurs de zoom de pixel *x* et *y* , les pixels sont convertis en fragments comme suit. Si (*x*<sub>r</sub> , *y*<sub>r</sub> ) est la position raster actuelle et qu’un pixel donné se trouve à l’emplacement *i* sur la ligne *j* du rectangle de pixel source, des fragments sont générés pour les pixels dont les centres se trouvent dans le rectangle avec des angles à

(*x*<sub>r</sub>  +  *Zoom*? i, o <sub></sub>  +  *Zoom* r <sub>y</sub> *j*)

et

(*x*<sub>r</sub>  +  *Zoom*? (*i* + 1), *o*<sub>r</sub>  +  *Zoom*<sub>y</sub> (*j* + 1))

où *Zoom*? est la valeur de zoom \_ GL \_ X et *Zoom*<sub>y</sub> est la valeur de \_ Zoom GL \_ y.

Les modes spécifiés par [**glPixelStore**](glpixelstore-functions.md) n’ont aucun effet sur l’opération de **glCopyPixels**.

Les fonctions suivantes récupèrent les informations relatives à **glCopyPixels**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ position

**glGet** avec argument GL \_ Current \_ Raster \_ position \_ valide

Pour copier le pixel de couleur dans l’angle inférieur gauche de la fenêtre à la position de pixellisation actuelle, utilisez

**glCopyPixels**(0, 0, 1, 1, \_ couleur GL);

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothèque<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
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

[**glReadBuffer**](glreadbuffer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





