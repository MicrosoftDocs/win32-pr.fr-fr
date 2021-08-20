---
title: fonction glReadPixels (GL. h)
description: La fonction glReadPixels lit un bloc de pixels à partir du trame.
ms.assetid: 41fbad5c-b8ca-456d-bbfc-b48c176e15b0
keywords:
- glReadPixels fonction OpenGL
topic_type:
- apiref
api_name:
- glReadPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b03a90fcd6ee5179a900739c40e78f796c6340d9609f4cfbeb21e6a70156afe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937939"
---
# <a name="glreadpixels-function"></a>glReadPixels fonction)

La fonction **glReadPixels** lit un bloc de pixels à partir du trame.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glReadPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  format,
   GLenum  type,
   GLvoid  *pixels
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*x* 
</dt> <dd>

Coordonnée *x* de la fenêtre du premier pixel lu à partir du trame. Avec la coordonnée *y* , spécifie l’emplacement du coin inférieur gauche d’un bloc rectangulaire de pixels.

</dd> <dt>

*y* 
</dt> <dd>

Coordonnées de la fenêtre *y* du premier pixel lu à partir du trame. Avec la coordonnée *x* , spécifie l’emplacement du coin inférieur gauche d’un bloc rectangulaire de pixels.

</dd> <dt>

*width* 
</dt> <dd>

Largeur du rectangle de pixels.

</dd> <dt>

*height* 
</dt> <dd>

Hauteur du rectangle de pixels. Les paramètres de *largeur* et de *hauteur* de la valeur « 1 » correspondent à un seul pixel.

</dd> <dt>

*format* 
</dt> <dd>

Format des données de pixels. Les valeurs symboliques suivantes sont acceptées :



| Valeur                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**\_index de couleur GL \_**</dt> </dl>                                                                                                                                                                                                                                                                                                               | Les index de couleurs sont lus à partir de la mémoire tampon de couleur sélectionnée par [**glReadBuffer**](glreadbuffer.md). Chaque index est converti en point fixe, déplacé à gauche ou à droite, en fonction de la valeur et du signe du décalage de l' \_ index GL \_ , puis ajouté au décalage de l' \_ index GL \_ . Si \_ \_ la couleur de la carte GL est \_ true pour le GL, les index sont remplacés par leurs mappages dans la table GL \_ pixel \_ Map \_ i \_ à \_ i.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt>**\_index de stencils GL \_**</dt> </dl>                                                                                                                                                                                                                                                                                                         | Les valeurs de stencil sont lues à partir de la mémoire tampon de stencil. Chaque index est converti en point fixe, déplacé à gauche ou à droite, en fonction de la valeur et du signe du décalage de l' \_ index GL \_ , puis ajouté au décalage de l' \_ index GL \_ . Si \_ le schéma \_ de la carte GL est \_ true pour le GL, les index sont remplacés par leurs mappages dans la table GL \_ pixel \_ Map \_ s \_ \_ .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt>**\_composant de profondeur du GL \_**</dt> </dl>                                                                                                                                                                                                                                                                                                   | Les valeurs de profondeur sont lues à partir de la mémoire tampon de profondeur. Chaque composant est converti en virgule flottante, de sorte que la valeur de profondeur minimale est mappée à 0,0 et que la valeur maximale est mappée à 1,0. Chaque composant est ensuite multiplié par l' \_ échelle de profondeur GL \_ , ajouté à \_ l’écart de profondeur GL \_ , et enfin ancré à la plage \[ 0, 1 \] .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_RED__GL_GREEN__GL_BLUE__GL_ALPHA__GL_RGB__GL_RGBA__GL_BGR_EXT__GL_BGRA_EXT__GL_LUMINANCE__GL_LUMINANCE_ALPHA"></span><span id="gl_red__gl_green__gl_blue__gl_alpha__gl_rgb__gl_rgba__gl_bgr_ext__gl_bgra_ext__gl_luminance__gl_luminance_alpha"></span><dl> <dt>**GL \_ Red, GL \_ vert, GL \_ Blue, GL \_ alpha, GL \_ RGB, GL \_ RVBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminance, GL \_ luminance \_ alpha**</dt> </dl> | Le traitement diffère selon que les tampons de couleurs stockent les index de couleurs ou les composants de couleur RVBA. Si des index de couleurs sont stockés, ils sont lus à partir de la mémoire tampon de couleur sélectionnée par [**glReadBuffer**](glreadbuffer.md). Chaque index est converti en point fixe, déplacé à gauche ou à droite, en fonction de la valeur et du signe du décalage de l' \_ index GL \_ , puis ajouté au décalage de l' \_ index GL \_ . Les index sont ensuite remplacés par les valeurs de rouge, vert, bleu et alpha obtenues par l’indexation de la \_ \_ carte de pixels GL \_ i \_ vers \_ R, la \_ \_ carte de pixel GL \_ i \_ à \_ G, la \_ \_ carte de pixels GL \_ i \_ à \_ B et \_ \_ la carte de pixels GL \_ i \_ en \_ tables. Si les composants de couleur RVBA sont stockés dans les tampons de couleur, ils sont lus à partir de la mémoire tampon de couleur sélectionnée par **glReadBuffer**. Chaque composant de couleur est converti en virgule flottante, de sorte que l’intensité de zéro correspond à 0,0 et aux mappages d’intensité complète à 1,0. Chaque composant est ensuite multiplié par la mise \_ \_ à l’échelle du GL c et ajouté au biais du GL \_ c \_ , où c est le GL \_ rouge, le GL \_ vert, le GL général \_ et le GL \_ alpha. Chaque composant est ancré à la plage \[ 0, 1 \] . Enfin, si \_ \_ la couleur de la carte GL est \_ true pour la comptabilité GL, chaque composant de couleur c est remplacé par le mappage de la table GL \_ pixel \_ Map \_ c \_ à \_ c, où c se présente de nouveau comme GL \_ Red, GL \_ Green, GL \_ Blue et GL \_ alpha. Chaque composant est mis à l’échelle en fonction de la taille de sa table correspondante avant l’exécution de la recherche. Enfin, les données inutiles sont ignorées. Par exemple, \_ le GL rouge ignore les composants vert, bleu et alpha, tandis que \_ le GL RGB ignore uniquement le composant alpha. La \_ luminance du GL calcule une valeur de composant unique comme la somme des composants rouge, vert et bleu, et \_ \_ la luminance alpha du GL fait de même, tout en conservant alpha comme seconde valeur.<br/> |



 

</dd> <dt>

*type* 
</dt> <dd>

Type de données des données de pixels. Il doit s’agir de l’une des valeurs suivantes.



| Type                | Masque d’index | Conversion de composant |
|---------------------|------------|----------------------|
| \_octet non signé GL \_  | 281        | (281) *c*             |
| \_octet GL            | 271        | \[(271) *c*-1 \] /2     |
| \_bitmap GL          | 1          | 1                    |
| NON signé dans le GL \_ \_ | 2 61       | (2 61) *c*            |
| \_abrégé GL           | 2 51       | \[(2 51) *c* 1 \] /2     |
| \_entier non signé GL \_\_ | 2 1       | (2 1) *c*            |
| GL \_ int             | 2 1      | \[(2 1) *c* 1 \] /2     |
| valeur \_ float du GL           | aucun       | *c*                  |



 

</dd> <dt>

*pixels* 
</dt> <dd>

Retourne les données de pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *format* ou le *type* n’était pas une valeur acceptée.<br/>                                                                              |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | La *largeur* ou la *hauteur* était négative.<br/>                                                                                   |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | le *format* est \_ l’index de couleurs GL \_ , et les mémoires tampons de couleur stockent les composants de couleur RVBA ou BGRA.<br/>                                 |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | le *format* était un \_ index de stencils GL \_ et il n’existait pas de tampon de stencil.<br/>                                                          |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | le *format* était \_ le \_ composant de profondeur GL et il n’existait pas de mémoire tampon de profondeur.<br/>                                                          |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |

## <a name="remarks"></a>Remarques

La fonction **glReadPixels** retourne des données de pixels à partir du trame, en commençant par le pixel dont l’angle inférieur gauche se trouve à l’emplacement (*x*, *y*), dans la mémoire du client à partir des *pixels* de l’emplacement. Plusieurs paramètres contrôlent le traitement des données de pixels avant qu’elles ne soient placées dans la mémoire du client. Ces paramètres sont définis avec trois commandes : [**glPixelStore**](glpixelstore-functions.md), [**glPixelTransfer**](glpixeltransfer.md)et [**glPixelMap**](glpixelmap.md). Cette rubrique décrit les effets sur les **glReadPixels** de la plupart des paramètres spécifiés par ces trois commandes.

La fonction **glReadPixels** retourne les valeurs de chaque pixel avec un angle inférieur gauche à (*x* + i, *y* + j) pour 0 = i < *largeur* et 0 = j < *hauteur*. Ce pixel est considéré comme le *premier* pixel de la ligne *j*. Les pixels sont retournés dans l’ordre des lignes de la plus petite à la ligne la plus élevée, de gauche à droite dans chaque ligne.

Les facteurs de décalage, de mise à l’échelle, de décalage et de recherche décrits ci-dessus sont tous spécifiés par [**glPixelTransfer**](glpixeltransfer.md). Le contenu de la table de recherche est spécifié par [**glPixelMap**](glpixelmap.md).

La dernière étape consiste à convertir les index ou les composants au format approprié, comme spécifié par *type*. Si le *format* est un index \_ de couleur GL ou un \_ \_ index de stencils GL \_ et que le type n’est pas de *type* GL \_ float, chaque index est masqué avec la valeur de masque indiquée dans le tableau suivant. Si le *type* est \_ float float, chaque index entier est converti en un format à virgule flottante simple précision.

Si le *format* est le GL \_ rouge, le GL \_ vert, le GL général, le GL \_ \_ alpha, le GL \_ RGB, le GL \_ RVBA, le GL \_ BGR \_ ext, le GL \_ BGRA \_ ext, \_ la luminance du GL ou le type de \_ luminance \_ alpha et le *type* ne sont pas des \_ valeurs GL float, chaque composant est multiplié par le multiplicateur indiqué dans le tableau précédent. Si le type est \_ float float, chaque composant est passé en tant que (ou converti au format à virgule flottante simple précision du client s’il est différent de celui utilisé par OpenGL).

Les valeurs de retour sont placées en mémoire comme suit. Si le *format* est \_ l' \_ index de couleur GL, l' \_ index de stencils GL \_ , le \_ \_ composant de profondeur GL, le GL rouge, le GL de GL, le GL général, le GL \_ \_ \_ \_ alpha ou \_ la luminance du GL, une valeur unique est retournée et les données du *premier* pixel de la ligne *j* sont placées à l’emplacement (*j* )*largeur*  +  *i*. \_Le GL RGB et GL \_ BGR \_ ext renvoient trois valeurs : GL \_ RVBA et GL \_ BGRA \_ ext retournent quatre valeurs, et \_ \_ la luminance alpha du GL retourne deux valeurs pour chaque pixel, avec toutes les valeurs correspondant à un seul pixel occupant de l’espace contigu en *pixels*. Stockage paramètres définis par [**glPixelStore**](glpixelstore-functions.md), tels que les \_ octets d’échange de packs gl \_ et les LSB de \_ \_ packs gl \_ \_ , affectent d’abord la façon dont les données sont écrites dans la mémoire. Pour obtenir une description, consultez [**glPixelStore**](glpixelstore-functions.md) .

Les valeurs des pixels qui se trouvent en dehors de la fenêtre connectée au contexte OpenGL actuel ne sont pas définies.

Si une erreur est générée, aucune modification n’est apportée au contenu des *pixels*.

La fonction suivante récupère des informations relatives à **glReadPixels**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ index \_ mode

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> </dl>

 

 





