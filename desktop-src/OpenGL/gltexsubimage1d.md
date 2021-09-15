---
title: fonction glTexSubImage1D (GL. h)
description: La fonction glTexSubImage1D spécifie une partie d’une image de texture unidimensionnelle existante. Vous ne pouvez pas définir une nouvelle texture avec glTexSubImage1D.
ms.assetid: e5fcb1a3-96f8-47a6-a9a7-0061faaaa6ac
keywords:
- glTexSubImage1D fonction OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe5510221b738a81f428f9e982a2f9bb2c23588
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413677"
---
# <a name="gltexsubimage1d-function"></a>glTexSubImage1D fonction)

La fonction **glTexSubImage1D** spécifie une partie d’une image de texture unidimensionnelle existante. Vous ne pouvez pas définir une nouvelle texture avec **glTexSubImage1D**.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glTexSubImage1D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Texture cible. Doit être une \_ texture GL \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

Numéro de niveau de détail. Le niveau 0 est l’image de base. Le niveau *n* est la *n* ième image de réduction mipmap.

</dd> <dt>

*xoffset* 
</dt> <dd>

Décalage de Texel dans la direction *x* dans le tableau de texture.

</dd> <dt>

*width* 
</dt> <dd>

Largeur de la sous-image de texture.

</dd> <dt>

*format* 
</dt> <dd>

Format des données de pixels. Ce paramètre peut prendre l’une des valeurs symboliques suivantes.



| Valeur                                                                                                                                                                         | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**\_index de couleur GL \_**</dt> </dl>             | Chaque élément est une valeur unique, un index de couleurs. Elle est convertie au format à virgule fixe (avec un nombre non spécifié de 0 bits à droite du point binaire), décalée vers la gauche ou vers la droite, en fonction de la valeur et du signe du décalage de l' \_ index GL \_ , puis ajoutée au décalage de l' \_ index GL \_ (voir [**glPixelTransfer**](glpixeltransfer.md)). L’index résultant est converti en un ensemble de composants de couleur à l’aide de la \_ carte de pixels GL \_ \_ i \_ à \_ R, de \_ \_ cartes de pixels GL \_ i \_ à \_ G, de mappage de \_ Pixel GL \_ \_ i \_ à \_ B et de carte de \_ pixels GL \_ \_ i \_ en \_ tables, et fixé à la plage \[ 0, 1 \] .<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ rouge**</dt> </dl>                                      | Chaque élément est un composant rouge unique. Il est converti au format à virgule flottante et assemblé dans un élément RVBA en joignant 0,0 pour le vert et le bleu, et 1,0 pour alpha. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**\_vert GL**</dt> </dl>                                | Chaque élément est un composant vert unique. Il est converti au format à virgule flottante et assemblé dans un élément RVBA en joignant 0,0 pour le rouge et le bleu, et 1,0 pour alpha. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**\_bleu GL**</dt> </dl>                                   | Chaque élément est un composant bleu unique. Il est converti au format à virgule flottante et assemblé dans un élément RVBA en joignant 0,0 pour le rouge et le vert, et 1,0 pour alpha. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ alpha**</dt> </dl>                                | Chaque élément est un composant alpha unique. Il est converti au format à virgule flottante et assemblé dans un élément RVBA en joignant 0,0 pour le rouge, le vert et le bleu. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**\_RGB GL**</dt> </dl>                                      | Chaque élément est un triple RVB. Il est converti en virgule flottante et assemblé en élément RVBA en joignant 1,0 pour alpha. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).<br/>                                                                                                                                                                                                                                            |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**GL \_ RVBA**</dt> </dl>                                   | Chaque élément est un élément RVBA complet. Elle est convertie au format à virgule flottante. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).<br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**LUMINANCE du GL \_**</dt> </dl>                    | Chaque élément est une valeur de luminance unique. Elle est convertie au format à virgule flottante, puis Assemblée dans un élément RVBA en répliquant la valeur de luminance trois fois pour le rouge, le vert et le bleu, et en joignant 1,0 pour alpha. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**\_luminance \_ alpha du GL**</dt> </dl> | Chaque élément est une paire luminance/alpha. Il est converti au format à virgule flottante, puis assemblé en élément RVBA en répliquant la valeur de luminance trois fois pour le rouge, le vert et le bleu. Chaque composant est ensuite multiplié par l’échelle de l’échelle GL c signée du facteur \_ \_ d’échelle, ajouté à l’écart de pondération GL \_ c signé, et est ancré \_ à la plage \[ 0, 1 \] (voir **glPixelTransfer**).<br/>                                                                                                                                                                         |



 

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



| Nom                                                                                                  | Signification                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | la *cible* n’était pas la texture de la comptabilité \_ \_ 1D.<br/>                                                                                                                                                                                                                             |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *format* n’est pas une constante acceptée.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *type* n’est pas une constante acceptée.<br/>                                                                                                                                                                                                                          |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *type* était \_ bitmap GL et le *format* n’était pas l’index de \_ couleur GL \_ .<br/>                                                                                                                                                                                                  |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | le *niveau* était inférieur à zéro ou supérieur à log2 *Max*, où *Max* était la valeur retournée de la \_ taille de texture max GL \_ \_ .<br/>                                                                                                                                          |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | *xoffset* était inférieur à *b*, ou   +  la *largeur* de décalage était supérieure à *WB*, où *w* correspond à la \_ largeur de la texture GL \_ , et *b* à la largeur de la bordure de la \_ texture GL \_ de l’image de texture en cours de modification.<br/> Notez que *w* comprend deux fois la largeur de la bordure.<br/> |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *largeur* était inférieure à *b*, où *b* est la largeur de bordure du tableau de texture.<br/>                                                                                                                                                                            |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *bordure* n’était pas égale à zéro ou 1.<br/>                                                                                                                                                                                                                                   |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | Le tableau texure n’a pas été défini par une opération **glTexImage1D** précédente.<br/>                                                                                                                                                                                    |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/>                                                                                                                                    |



## <a name="remarks"></a>Notes

Une texture unidimensionnelle pour une primitive est activée à l’aide de [**glEnable**](glenable.md) et **glDisable** avec l’argument GL \_ texture \_ 1D. Pendant la texturation, une partie d’une image de texture spécifiée est mappée à chaque primitive activée. Vous utilisez la fonction **glTexSubImage1D** pour spécifier une sous-image contiguë d’une image de texture unidimensionnelle existante pour la texturation.

Les texels référencés par les *pixels* remplacent une région du tableau de texture existant par des index *x* de *xoffset* et *xoffset* + (*largeur* 1) inclus. Cette région ne peut pas inclure de texels en dehors de la plage du tableau de texture spécifié à l’origine.

La spécification d’une sous-image avec une *largeur* de zéro n’a aucun effet et ne génère pas d’erreur.

La texturation n’a aucun effet dans le mode d’index des couleurs.

En général, les images de texture peuvent être représentées par les mêmes formats de données que les pixels d’une commande [**glDrawPixels**](gldrawpixels.md) , à ceci près que le \_ \_ composant index de stencils GL et \_ profondeur GL \_ ne peut pas être utilisé. Les modes [**glPixelStore**](glpixelstore-functions.md) et [**glPixelTransfer**](glpixeltransfer.md) affectent les images de texture exactement comme elles affectent **glDrawPixels**.

Les fonctions suivantes récupèrent les informations relatives à **glTexSubImage1D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ 1D

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

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage1D**](glcopytexsubimage1d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





