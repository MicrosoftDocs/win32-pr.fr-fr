---
title: fonction glTexImage2D (GL. h)
description: La fonction glTexImage2D spécifie une image de texture à deux dimensions.
ms.assetid: e8b9c692-5239-47de-86eb-80c247c60e1d
keywords:
- glTexImage2D fonction OpenGL
topic_type:
- apiref
api_name:
- glTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba2d5bc6f966d9b10c0dadccb221086e64de827
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517335"
---
# <a name="glteximage2d-function"></a>glTexImage2D fonction)

La fonction **glTexImage2D** spécifie une image de texture à deux dimensions.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glTexImage2D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLsizei height,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Texture cible. Doit être une \_ texture GL \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Numéro de niveau de détail. Le niveau 0 est le niveau d’image de base. Le niveau *n* est la *n* ième image de réduction mipmap.

</dd> <dt>

*internalformat* 
</dt> <dd>

Nombre de composants de couleur dans la texture. Doit être 1, 2, 3 ou 4, ou l’une des constantes symboliques suivantes : GL \_ alpha, GL \_ alpha4, GL \_ ALPHA8, GL \_ ALPHA12, GL ALPHA16, luminance GL, GL LUMINANCE4, GL LUMINANCE8, GL LUMINANCE12, GL LUMINANCE16, GL luminance alpha, GL LUMINANCE4 alpha4, GL LUMINANCE6 alpha2 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ , GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 \_ alpha4, comptabilité GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL Intensity, GL INTENSITY4, GL INTENSITY8, GL INTENSITY12, GL INTENSITY16, GL R3 G3 B2, GL RGB, \_ GL RGB4 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ , GL RGB5, GL RGB8, GL RGB10, GL RGB12, GL RGB16, grand livre, GL RGBA2, GL RGBA4, GL RGB5 a1, GL RGBA8, GL RGB10 a2, GL RGBA12 ou GL RGBA16.

</dd> <dt>

*width* 
</dt> <dd>

Largeur de l’image de texture. Doit être 2 *n* + 2 (*Border*) pour un entier *n*.

</dd> <dt>

*height* 
</dt> <dd>

Hauteur de l’image de texture. Doit être 2 *<sup>m</sup>* + 2 (*bordure*) pour un entier *m*.

</dd> <dt>

*2S* 
</dt> <dd>

Largeur de la bordure. Doit être 0 ou 1.

</dd> <dt>

*format* 
</dt> <dd>

Format des données de pixels. Elle peut prendre l’une des neuf valeurs symboliques.



| Valeur                                                                                                                                                                         | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**\_index de couleur GL \_**</dt> </dl>             | Chaque élément est une valeur unique, un index de couleurs. Elle est convertie en virgule fixe (avec un nombre non spécifié de 0 bits à droite du point binaire), décalée vers la gauche ou vers la droite selon la valeur et le signe du décalage de l' \_ index GL \_ , puis ajoutée au décalage de l' \_ index GL \_ (voir [**glPixelTransfer**](glpixeltransfer.md)). L’index résultant est converti en un ensemble de composants de couleur à l’aide de la \_ carte de pixels GL \_ \_ i \_ à \_ R, de \_ \_ cartes de pixels GL \_ i \_ à \_ G, de mappage de \_ Pixel GL \_ \_ i \_ à \_ B et de carte de \_ pixels GL \_ \_ i \_ en \_ tables, et fixé à la plage \[ 0, 1 \] .<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ rouge**</dt> </dl>                                      | Chaque élément est un composant rouge unique. Il est converti en virgule flottante et assemblé en élément RVBA en joignant 0,0 pour le vert et le bleu, et 1,0 pour alpha. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).<br/>                                                                                                                                                                                               |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**\_vert GL**</dt> </dl>                                | Chaque élément est un composant vert unique. Il est converti en virgule flottante et assemblé en élément RVBA en joignant 0,0 pour le rouge et le bleu, et 1,0 pour alpha. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                        |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**\_bleu GL**</dt> </dl>                                   | Chaque élément est un composant bleu unique. Il est converti en virgule flottante et assemblé en élément RVBA en joignant 0,0 pour le rouge et le vert, et 1,0 pour alpha. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).<br/>                                                                                                                                                                                               |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ alpha**</dt> </dl>                                | Chaque élément est un composant rouge unique. Il est converti en virgule flottante et assemblé en élément RVBA en joignant 0,0 pour le rouge, le vert et le bleu. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                     |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**\_RGB GL**</dt> </dl>                                      | Chaque élément est un triple RVB. Il est converti en virgule flottante et assemblé en élément RVBA en joignant 1,0 pour alpha. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).<br/>                                                                                                                                                                                                                                    |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**GL \_ RVBA**</dt> </dl>                                   | Chaque élément est un élément RVBA complet. Elle est convertie en virgule flottante. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                                                                                                 |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt>**GL \_ BGR \_ ext**</dt> </dl>                         | Chaque pixel est un groupe de trois composants dans cet ordre : bleu, vert, rouge.<br/> GL \_ BGR \_ ext fournit un format qui correspond à la disposition de la mémoire des bitmaps indépendantes du périphérique (DIB) Windows. Par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.<br/>                                                                                                                                                                                                                                     |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt>**GL \_ BGRA \_ ext**</dt> </dl>                      | Chaque pixel est un groupe de quatre composants dans l’ordre suivant : bleu, vert, rouge, alpha. GL \_ BGRA \_ ext fournit un format qui correspond à la disposition de la mémoire des bitmaps indépendantes du périphérique (DIB) Windows. Par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.<br/>                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**LUMINANCE du GL \_**</dt> </dl>                    | Chaque élément est une valeur de luminance unique. Elle est convertie en virgule flottante, puis Assemblée en élément RVBA en répliquant la valeur de luminance trois fois pour le rouge, le vert et le bleu, et en joignant 1,0 pour alpha. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).<br/>                                                                                                                                         |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**\_luminance \_ alpha du GL**</dt> </dl> | Chaque élément est une paire luminance/alpha. Elle est convertie en virgule flottante, puis Assemblée en élément RVBA en répliquant la valeur de luminance trois fois pour le rouge, le vert et le bleu. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                 |



 

</dd> <dt>

*type* 
</dt> <dd>

Type de données des données de pixels. Les valeurs symboliques suivantes sont acceptées : \_ octet non signé GL \_ , \_ octet GL, bitmap GL \_ , GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int et GL \_ float.

</dd> <dt>

*pixels* 
</dt> <dd>

Pointeur vers les données de l’image en mémoire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | la *cible* n’était pas une \_ texture GL \_ 2D.<br/>                                                                                                                                                                                |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *format* n’était pas une constante de *format* acceptée. Seules les constantes de format autres que l' \_ index du stencil GL et le composant de \_ \_ profondeur GL \_ sont acceptées. Pour obtenir la liste des valeurs possibles, consultez la description du paramètre *format* .<br/> |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *type* n’est pas une constante de *type* .<br/>                                                                                                                                                                                   |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *type* était \_ bitmap GL et le *format* n’était pas l’index de \_ couleur GL \_ .<br/>                                                                                                                                                        |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | le *niveau* était inférieur à zéro ou supérieur à log2 *Max*, où *Max* était la valeur retournée de la \_ taille de texture max GL \_ \_ .<br/>                                                                                                |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | *internalformat* n’était pas 1, 2, 3 ou 4.<br/>                                                                                                                                                                         |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *largeur* ou la hauteur est inférieure à zéro ou supérieure à 2 + la \_ taille de la texture GL maximum \_ \_ , ou elle ne peut pas être représentée sous la forme 2 *n* + 2 (bordure) pour une valeur entière de *n*.<br/>                                                  |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *bordure* n’est pas 0 ou 1.<br/>                                                                                                                                                                                            |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/>                                                                                          |



## <a name="remarks"></a>Notes

La fonction **glTexImage2D** spécifie une image de texture à deux dimensions. La texturation mappe une partie d’une *image de texture* spécifiée sur chaque primitive graphique pour laquelle la texturation est activée. La texturation à deux dimensions est activée et désactivée à l’aide de [**glEnable**](glenable.md) et **glDisable** avec l’argument GL \_ texture \_ 2D.

Les images de texture sont définies avec **glTexImage2D**. Les arguments décrivent les paramètres de l’image de texture, tels que la hauteur, la largeur, la largeur de la bordure, le nombre de niveaux de détail (voir [**glTexParameter**](gltexparameter-functions.md)) et le nombre de composants de couleur fournis. Les trois derniers arguments décrivent le mode de représentation de l’image en mémoire. Ces arguments sont identiques aux formats de pixels utilisés pour [**glDrawPixels**](gldrawpixels.md).

Les données sont lues à partir de *pixels* sous la forme d’une séquence d’octets signés ou non signés, de shorts ou de longs, ou de valeurs à virgule flottante simple précision, en fonction du *type*. Ces valeurs sont regroupées en jeux d’une, deux, trois ou quatre valeurs, selon le *format*, pour former des éléments. Si le *type* est \_ bitmap GL, les données sont considérées comme une chaîne d’octets non signés (et le *format* doit être un index de couleur GL \_ \_ ). Chaque octet de données est traité comme des éléments 8 1 bits, l’ordonnancement des bits étant déterminé par le \_ décompression GL \_ LSB en \_ premier (voir [**glPixelStore**](glpixelstore-functions.md)). Pour obtenir une description des valeurs acceptables pour le paramètre de *type* , consultez [**glDrawPixels**](gldrawpixels.md) .

Une image de texture peut avoir jusqu’à quatre composants par élément de texture, en fonction des *composants*. Une image de texture à un composant utilise uniquement le composant rouge de la couleur RVBA extraite des *pixels*. Une image à deux composants utilise les valeurs R et A. Une image à trois composants utilise les valeurs R, G et B. Une image à quatre composants utilise tous les composants RVBA.

La texturation n’a aucun effet dans le mode d’index des couleurs.

L’image de texture peut être représentée par les mêmes formats de données que les pixels d’une commande **glDrawPixels** , à ceci près que le \_ composant index du stencil GL \_ et profondeur du GL \_ \_ ne peut pas être utilisé. Les modes [**glPixelStore**](glpixelstore-functions.md) et [**glPixelTransfer**](glpixeltransfer.md) affectent les images de texture exactement comme elles affectent **glDrawPixels**.

Une image de texture avec une hauteur ou une largeur nulle indique la texture null. Si la texture null est spécifiée pour le niveau de détail 0, c’est comme si la texturation était désactivée.

Les fonctions suivantes récupèrent les informations relatives à **glTexImage2D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ 2D

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





