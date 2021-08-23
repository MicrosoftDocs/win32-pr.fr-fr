---
title: fonction glFeedbackBuffer (GL. h)
description: La fonction glFeedbackBuffer contrôle le mode de feedback.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- glFeedbackBuffer fonction OpenGL
topic_type:
- apiref
api_name:
- glFeedbackBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e51a08dac2bbf55509d4964218fc4b844581c797220294464b84c05de5e05b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580199"
---
# <a name="glfeedbackbuffer-function"></a>glFeedbackBuffer fonction)

La fonction **glFeedbackBuffer** contrôle le mode de feedback.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glFeedbackBuffer(
   GLsizei size,
   GLenum  type,
   GLfloat *buffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*size* 
</dt> <dd>

Nombre maximal de valeurs qui peuvent être écrites dans la *mémoire tampon*.

</dd> <dt>

*type* 
</dt> <dd>

Constante symbolique qui décrit les informations qui seront retournées pour chaque vertex. Les constantes symboliques suivantes sont acceptées : GL \_ 2D, GL \_ 3D, GL \_ 3D \_ Color, GL \_ 3D texture Color \_ \_ et GL \_ 4D \_ Color \_ texture.

</dd> <dt>

*mémoire tampon* 
</dt> <dd>

Retourne les données de commentaires.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *type* n’est pas une valeur acceptée.<br/>                                                                                                                                                                           |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | la *taille* était négative.<br/>                                                                                                                                                                                        |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | **glFeedbackBuffer** a été appelé alors que le mode de rendu était \_ Commentaires sur le GL, ou [**glRenderMode**](glrendermode.md) a été appelé avec des commentaires sur l’argument GL \_ avant que **glFeedbackBuffer** n’ait été appelé au moins une fois.<br/> |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/>                                                                                  |



## <a name="remarks"></a>Remarques

La fonction **glFeedbackBuffer** contrôle les commentaires. Les commentaires, comme la sélection, sont un mode OpenGL. Le mode est sélectionné en appelant [**glRenderMode**](glrendermode.md) avec les commentaires sur le GL \_ . Lorsque OpenGL est en mode commentaires, aucun Pixel n’est généré par pixellisation. Au lieu de cela, les informations sur les primitives qui auraient été pixellisées sont renvoyées à l’application à l’aide de OpenGL.

La fonction **glFeedbackBuffer** a trois arguments :

-   *buffer* est un pointeur vers un tableau de valeurs à virgule flottante dans lequel les informations de commentaires sont placées.
-   *taille* indique la taille du tableau.
-   le *type* est une constante symbolique décrivant les informations qui sont renvoyées pour chaque vertex.

Vous devez émettre **glFeedbackBuffer** pour que le mode Commentaires soit activé (en appelant **glRenderMode** avec les commentaires sur l’argument GL \_ ). La définition \_ de commentaires sur le GL sans l’établissement de la mémoire tampon de commentaires, ou l’appel de **glFeedbackBuffer** alors que OpenGL est en mode commentaires, est une erreur.

Veillez à utiliser le mode Feedback en appelant [**glRenderMode**](glrendermode.md) avec une valeur de paramètre autre que le \_ Feedback GL. Lorsque vous effectuez cette opération alors que OpenGL est en mode commentaires, **glRenderMode** retourne le nombre d’entrées placées dans le tableau de commentaires. La valeur retournée n’est jamais supérieure à la *taille*. Si les données de commentaires requièrent plus d’espace que ce qui était disponible dans la *mémoire tampon*, **glRenderMode** retourne une valeur négative.

En mode commentaires, chaque primitive qui serait pixellisée génère un bloc de valeurs copiées dans le tableau de commentaires. Si vous procédez ainsi, le nombre d’entrées dépasse le maximum, **glFeedbackBuffer** écrit partiellement le bloc afin de remplir le tableau (s’il reste de la place) et définit un indicateur de dépassement de capacité. Chaque bloc commence par un code qui indique le type primitif, suivi de valeurs qui décrivent les vertex de la primitive et les données associées. La fonction **glFeedbackBuffer** écrit également des entrées pour les bitmaps et les rectangles de pixels. Des commentaires se produisent après l’élimination des polygones et l’interprétation [**glPolygonMode**](glpolygonmode.md) des polygones, de sorte que les polygones qui sont supprimés ne sont pas retournés dans la mémoire tampon de commentaires. Elle peut également se produire lorsque les polygones avec plus de trois bords sont divisés en triangles, si l’implémentation OpenGL affiche des polygones en effectuant cette décomposition.

Vous pouvez insérer un marqueur dans la mémoire tampon de commentaires avec [**glPassThrough**](glpassthrough.md).

Voici la grammaire des blocs de valeurs écrites dans la mémoire tampon de commentaires. Chaque primitive est indiquée avec une valeur d’identification unique suivie d’un certain nombre de vertex. Les entrées de polygone incluent une valeur entière indiquant le nombre de vertex qui suivent. Un vertex est renvoyé sous la forme d’un certain nombre de valeurs à virgule flottante, comme déterminé par le *type*. Les couleurs sont renvoyées sous forme de quatre valeurs en mode RVBA et d’une valeur en mode d’index des couleurs.

feedbackList < feedbackItem feedbackList \| feedbackItem

feedbackItem < point \| LineSegment \| Polygon \| bitmap \| pixelRectangle \| PassThru

point < sommet du jeton de \_ point GL \_

lineSegment < jeton de ligne GL vertex vertex de la \_ \_ \| ligne GL de \_ \_ réinitialisation du \_ jeton de sommet

Polygon < \_ jeton de polygone GL \_ n

polyspec < vertex vertex vertex vertex vertex \|

bitmap < vertex de jeton de \_ bitmap GL \_

pixelRectangle < GL-créer un vertex de jeton de pixel de \_ \_ \_ \| \_ copie GL \_ \_ de nuance de pixel

valeur de jeton de transmission de transfert de < du GL passThru \_ \_ \_

vertex < 2D \| 3D \| 3dColor \| 3dColorTexture \| 4dColorTexture

valeur de la valeur de < 2D

valeur de la valeur de la valeur de < 3D

3dColor < valeur de la valeur de valeur de valeur

3dColorTexture < valeur valeur valeur couleur Tex

4dColorTexture < valeur valeur valeur valeur couleur Tex

index de couleur < RVBA \|

valeur de valeur de valeur de la valeur de < RVBA

valeur de < d’index

valeur de valeur de valeur de valeur <

Le paramètre de *valeur* est un nombre à virgule flottante, et *n* est un entier à virgule flottante qui donne le nombre de vertex du polygone. Les éléments suivants sont des constantes à virgule flottante symboliques : \_ jeton de point GL \_ , jeton de \_ ligne GL \_ , jeton de \_ \_ réinitialisation de ligne GL \_ , jeton de \_ polygone GL \_ , jeton de \_ bitmap GL, jeton de texte \_ \_ de dessin GL \_ \_ , jeton de copie GL de \_ \_ pixel \_ et jeton de transfert de GL \_ \_ \_ . \_ \_ Le jeton de réinitialisation de ligne GL \_ est renvoyé chaque fois que le modèle de ligne stipple est réinitialisé. Les données retournées en tant que vertex dépendent du *type* de commentaires.

Le tableau suivant donne la correspondance entre le *type* et le nombre de valeurs par vertex ; *k* est 1 en mode d’index de couleurs et 4 en mode RVBA.



| Type                   | Coordinates        | Couleur | Texture | Nombre total de valeurs |
|------------------------|--------------------|-------|---------|------------------------|
| COMPTABILITÉ \_ 2D                 | *x*, *y*           |       |         | 2                      |
| \_3D GL                 | *x*, *y*, *z*      |       |         | 3                      |
| \_Couleur 3D \_ GL          | *x*, *y*, *z*      | *DK*   |         | 3 + *k*                |
| \_Texture de \_ couleur \_ 3D GL | *x*, *y*, *z*,     | *DK*   | 4       | 7 + *k*                |
| TEXTURE GL de \_ \_ couleur 4D \_ | *x*, *y*, *z*, *w* | *DK*   | 4       | 8 + *k*                |



 

Les coordonnées des sommets de commentaires sont exprimées en coordonnées de fenêtre, sauf *w*, qui est en coordonnées de clip. Les couleurs de commentaires sont claires, si l’éclairage est activé. Des coordonnées de texture de commentaires sont générées si la génération de coordonnées de texture est activée. Elles sont toujours transformées par la matrice de texture.

La fonction **glFeedbackBuffer** , lorsqu’elle est utilisée dans une liste d’affichage, n’est pas compilée dans la liste d’affichage, mais plutôt exécutée immédiatement.

La fonction suivante récupère des informations relatives à **glFeedbackBuffer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Render \_ mode

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPassThrough**](glpassthrough.md)
</dt> <dt>

[**glPolygonMode**](glpolygonmode.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





