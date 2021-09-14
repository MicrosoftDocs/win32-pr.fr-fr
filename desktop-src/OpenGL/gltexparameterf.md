---
title: fonction glTexParameterf (GL. h)
description: Définit les paramètres de texture. | fonction glTexParameterf (GL. h)
ms.assetid: 20b9f2d5-66e1-41cd-9571-8caa38ef033d
keywords:
- glTexParameterf fonction OpenGL
topic_type:
- apiref
api_name:
- glTexParameterf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f749513757ee32f6fe468dadbe968b8657a06f3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233610"
---
# <a name="gltexparameterf-function"></a>glTexParameterf fonction)

Définit les paramètres de texture.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glTexParameterf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Texture cible, qui doit être une texture GL \_ \_ 1D ou une \_ texture GL \_ 2D.

</dd> <dt>

*pname* 
</dt> <dd>

Nom symbolique d’un paramètre de texture à valeur unique. Les symboles suivants sont acceptés dans *pname*.



| Valeur                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**filtre de la \_ texture GL \_ min. \_**</dt> </dl> | La fonction minimisation de la texture est utilisée chaque fois que le pixel qui est texturé est mappé à une zone supérieure à un élément de texture. Il existe six fonctions minimisation définies. Deux d’entre eux utilisent l’un des quatre éléments de texture les plus proches pour calculer la valeur de la texture. Les quatre autres utilisent des mipmaps.<br/> Un mipmap est un ensemble ordonné de tableaux représentant la même image à des résolutions progressivement inférieures. Si la texture contient des dimensions 2nx2<sup>m</sup> , il y a Max (n, m) + 1 des mipmaps. Le premier mipmap est la texture d’origine, avec les dimensions 2nx2<sup>m</sup>. Chaque mipmap suivant a des dimensions 2<sup>k</sup>1x2<sup>l</sup>1 où 2<sup>k</sup>x2<sup>l</sup> sont les dimensions du mipmap précédent, jusqu’à k = 0 ou l = 0. À ce stade, les des mipmaps suivantes comportent la dimension 1x2<sup>l</sup>1 ou 2<sup>k</sup>1x1 jusqu’au mipmap final, qui a une dimension 1x1. Les des mipmaps sont définis à l’aide de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md) avec l’argument de niveau de détail qui indique l’ordre des des mipmaps. Le niveau 0 est la texture d’origine. le niveau gras Max (n, m) est le mipmap de la dernière version 1x1.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**filtre de la \_ texture GL \_ \_**</dt> </dl> | La fonction d’agrandissement de la texture est utilisée lorsque le pixel en cours de texture est mappé à une zone inférieure ou égale à un élément de texture. Elle définit la fonction d’agrandissement de la texture sur la valeur GL la \_ plus proche ou le GL \_ linéaire.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**\_ \_ encapsuler la texture GL \_ S**</dt> </dl>             | Définit le paramètre de retour à la ligne pour les coordonnées de la texture sur GL \_ clamp ou GL \_ REPEAT. \_La fixation du GL fait que les coordonnées s sont ancrées à la plage \[ 0, 1 \] et est utile pour empêcher l’encapsulation des artefacts lors du mappage d’une image unique sur un objet. \_La répétition du GL provoque l’ignorance de la partie entière de la coordonnée s. OpenGL utilise uniquement la partie fractionnaire, créant ainsi un modèle répétitif. Les éléments de texture de bordure sont accessibles uniquement si l’habillage est défini sur la \_ fixation GL. Au départ, \_ \_ la \_ valeur S de la texture GL est définie sur la répétition du GL \_ .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**\_enveloppe de \_ la texture GL \_ T**</dt> </dl>             | Définit le paramètre de retour à la ligne pour la coordonnée de texture sur GL \_ clamp ou GL \_ REPEAT. Consultez la discussion sous les \_ enveloppes de la texture GL \_ \_ S. Initialement, \_ la texture \_ GL \_ T Wrap T est définie sur GL \_ REPEAT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*param* 
</dt> <dd>

Valeur de *pname*.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ \_énumération non valide**</dt> </dl>     | *target* ou *pname* ne faisait pas partie des valeurs définies acceptées, ou lorsque *param* aurait dû avoir une valeur de constante définie (basée sur la valeur de *pname*) et ne l’a pas fait.<br/> |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/>                                            |



## <a name="remarks"></a>Notes

Le mappage de texture est une technique qui applique une image sur la surface d’un objet comme si l’image était un cellophane de décalque ou de réduction. L’image est créée dans l’espace de texture, avec un système de coordonnées (*s*, *t*). Une texture est une image à une ou deux dimensions et un ensemble de paramètres qui déterminent la façon dont les échantillons sont dérivés de l’image.

La fonction **glTexParameter** assigne la ou les valeurs dans les paramètres au paramètre de texture spécifié comme pname. Le paramètre Target définit la texture cible, à savoir la texture GL \_ \_ 1D ou la \_ texture GL \_ 2D.

À mesure que d’autres éléments de texture sont échantillonnés dans le processus de minimisation, le nombre d’artefacts d’alias est apparent. Alors que les \_ fonctions de minimisation linéaires GL les plus proches et les plus proches \_ peuvent être plus rapides que les quatre autres, elles n’échantillonnent qu’un ou quatre éléments de texture pour déterminer la valeur de texture du pixel rendu et peuvent produire des modèles moire ou des transitions irrégulières. La valeur par défaut du \_ filtre de la texture GL \_ min est le \_ \_ MIPMAP linéaire le plus proche \_ \_ .

Supposons que la texturation est activée (en appelant [**glEnable**](glenable.md) avec \_ l’argument la texture GL \_ 1D ou la \_ texture GL \_ 2d) et \_ \_ \_ le filtre de la texture GL min est défini sur l’une des fonctions qui requièrent un mipmap. Si les dimensions des images de texture actuellement définies (avec des appels précédents à [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md)) ne suivent pas la séquence appropriée pour des mipmaps, ou si moins d’images de texture sont définies que nécessaire, ou si le jeu d’images de texture a des nombres différents de composants de texture, c’est comme si le mappage de texture était désactivé. Le filtrage linéaire accède aux quatre éléments de texture les plus proches uniquement dans les textures 2D. Dans les textures 1D, le filtrage linéaire accède aux deux éléments de texture les plus proches. La fonction suivante récupère des informations relatives à **glTexParameterf**, **glTexParameteri**, **glTexParameterfv** et **glTexParameteriv**.

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





