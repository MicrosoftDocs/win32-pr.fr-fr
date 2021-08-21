---
title: fonction glTexParameteriv (GL. h)
description: Définit les paramètres de texture. | fonction glTexParameteriv (GL. h)
ms.assetid: c6381ee5-5323-4e11-9c32-bc70f25f8f4e
keywords:
- glTexParameterfv fonction OpenGL
topic_type:
- apiref
api_name:
- glTexParameterfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40df39c0d95d5719b0e066a1fadc089212619ecabf7868400e246001b69f579b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490039"
---
# <a name="gltexparameteriv-function"></a>glTexParameteriv fonction)

Définit les paramètres de texture.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glTexParameterfv(
         GLenum target,
         GLenum pname,
   const GLint  *params
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



| Valeur                                                                                                                                                                                         | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**filtre de la \_ texture GL \_ min. \_**</dt> </dl>       | La fonction minimisation de la texture est utilisée chaque fois que le pixel qui est texturé est mappé à une zone supérieure à un élément de texture. Il existe six fonctions minimisation définies. Deux d’entre eux utilisent l’un des quatre éléments de texture les plus proches pour calculer la valeur de la texture. Les quatre autres utilisent des mipmaps. <br/> Un mipmap est un ensemble ordonné de tableaux représentant la même image à des résolutions progressivement inférieures. Si la texture contient des dimensions 2nx2<sup>m</sup> , il y a Max (n, m) + 1 des mipmaps. Le premier mipmap est la texture d’origine, avec les dimensions 2nx2<sup>m</sup>. Chaque mipmap suivant a des dimensions 2<sup>k</sup>1x2<sup>l</sup>1 où 2<sup>k</sup>x2<sup>l</sup> sont les dimensions du mipmap précédent, jusqu’à k = 0 ou l = 0. À ce stade, les des mipmaps suivantes comportent la dimension 1x2<sup>l</sup>1 ou 2<sup>k</sup>1x1 jusqu’au mipmap final, qui a une dimension 1x1. Les des mipmaps sont définis à l’aide de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md) avec l’argument de niveau de détail qui indique l’ordre des des mipmaps. Le niveau 0 est la texture d’origine. le niveau gras Max (n, m) est le mipmap de la dernière version 1x1.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**filtre de la \_ texture GL \_ \_**</dt> </dl>       | La fonction d’agrandissement de la texture est utilisée lorsque le pixel en cours de texture est mappé à une zone inférieure ou égale à un élément de texture. Elle définit la fonction d’agrandissement de la texture sur la valeur GL la \_ plus proche ou le GL \_ linéaire.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**\_ \_ encapsuler la texture GL \_ S**</dt> </dl>                   | Définit le paramètre de retour à la ligne pour les coordonnées de la texture sur GL \_ clamp ou GL \_ REPEAT. \_La fixation du GL fait que les coordonnées s sont ancrées à la plage \[ 0, 1 \] et est utile pour empêcher l’encapsulation des artefacts lors du mappage d’une image unique sur un objet. \_La répétition du GL provoque l’ignorance de la partie entière de la coordonnée s. OpenGL utilise uniquement la partie fractionnaire, créant ainsi un modèle répétitif. Les éléments de texture de bordure sont accessibles uniquement si l’habillage est défini sur la \_ fixation GL. Au départ, \_ \_ la \_ valeur S de la texture GL est définie sur la répétition du GL \_ .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**\_enveloppe de \_ la texture GL \_ T**</dt> </dl>                   | Définit le paramètre de retour à la ligne pour la coordonnée de texture sur GL \_ clamp ou GL \_ REPEAT. Consultez la discussion sous les \_ enveloppes de la texture GL \_ \_ S. Initialement, \_ la texture \_ GL \_ T Wrap T est définie sur GL \_ REPEAT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**couleur de bordure de la \_ texture GL \_ \_**</dt> </dl> | Définit une couleur de bordure. Le paramètre *params* contient quatre valeurs qui composent la couleur RVBA de la bordure de texture. Les composants de couleur entier sont interprétés de manière linéaire de telle sorte que l’entier le plus positif est mappé à 1,0, et l’entier le plus négatif est mappé à 1,0. Les valeurs sont ancrées à la plage \[ 0, 1 \] quand elles sont spécifiées. Initialement, la couleur de la bordure est (0, 0, 0, 0).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**\_priorité de texture GL \_**</dt> </dl>              | Spécifie la priorité de résidence de la texture actuellement liée. Les valeurs autorisées sont comprises entre \[ 0 et 1 \] . Pour plus d’informations, consultez [**glPrioritizeTextures**](glprioritizetextures.md) et [**glBindTexture**](glbindtexture.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*params* 
</dt> <dd>

Pointeur vers un tableau où la valeur ou les valeurs d’pname sont stockées. Le paramètre params fournit une fonction pour minimisation la texture comme l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                               | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <dt>**GL \_ Le plus proche**</dt> </dl>                                             | Retourne la valeur de l’élément de texture qui est le plus proche (dans la distance Manhattan) au centre du pixel qui est texturé. <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <dt>**linéaire du GL \_**</dt> </dl>                                                   | Retourne la moyenne pondérée des quatre éléments de texture les plus proches du centre du pixel qui est texturé. Celles-ci peuvent inclure des éléments de texture de bordure, en fonction des valeurs des valeurs des \_ textures GL \_ \_ S, GL \_ texture \_ Wrap \_ T et sur le mappage exact. \_Le GL le plus proche est généralement plus rapide que \_ le GL linéaire, mais il peut produire des images texturées avec des arêtes plus nettes, car la transition entre les éléments de texture n’est pas aussi lisse. La valeur par défaut du \_ filtre GL texture \_ Mag \_ est \_ GL Linear.<br/> |
| <span id="GL_NEAREST_MIPMAP_NEAREST"></span><span id="gl_nearest_mipmap_nearest"></span><dl> <dt>**MIPMAP du GL le plus proche \_ \_ \_ le plus proche**</dt> </dl> | Choisit le mipmap qui correspond le mieux à la taille du pixel qui est texturé et utilise le critère du GL le plus \_ proche (l’élément de texture le plus proche du centre du pixel) pour produire une valeur de texture. <br/>                                                                                                                                                                                                                                                                                              |
| <span id="GL_LINEAR_MIPMAP_NEAREST"></span><span id="gl_linear_mipmap_nearest"></span><dl> <dt>**\_MIPMAP linéaire \_ GL \_ le plus proche**</dt> </dl>    | Choisit le mipmap qui correspond le mieux à la taille du pixel qui est texturé et utilise le \_ critère linéaire GL (une moyenne pondérée des quatre éléments de texture qui sont les plus proches du centre du pixel) pour produire une valeur de texture. <br/>                                                                                                                                                                                                                                                          |
| <span id="GL_NEAREST_MIPMAP_LINEAR"></span><span id="gl_nearest_mipmap_linear"></span><dl> <dt>**MIPMAP linéaire de la comptabilité la \_ plus proche \_ \_**</dt> </dl>    | Choisit les deux des mipmaps qui correspondent le plus à la taille du pixel qui est texturé et utilise le critère GL le plus \_ proche (l’élément de texture le plus proche du centre du pixel) pour produire une valeur de texture à partir de chaque mipmap. La valeur de texture finale est une moyenne pondérée de ces deux valeurs. <br/>                                                                                                                                                                                                       |
| <span id="GL_LINEAR_MIPMAP_LINEAR"></span><span id="gl_linear_mipmap_linear"></span><dl> <dt>**MIPMAP linéaire du GL du GL \_ \_ \_**</dt> </dl>       | Choisit les deux des mipmaps qui correspondent le plus à la taille du pixel qui est texturé et utilise le \_ critère linéaire GL (une moyenne pondérée des quatre éléments de texture qui sont les plus proches du centre du pixel) afin de produire une valeur de texture à partir de chaque mipmap. La valeur de texture finale est une moyenne pondérée de ces deux valeurs.<br/>                                                                                                                                                                    |



 

Le paramètre *params* fournit une fonction permettant d’agrandir la texture comme l’une des valeurs suivantes.



| Valeur                                                                                                                                                   | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <dt>**GL \_ Le plus proche**</dt> </dl> | Retourne la valeur de l’élément de texture qui est le plus proche (dans la distance Manhattan) au centre du pixel qui est texturé. <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <dt>**linéaire du GL \_**</dt> </dl>       | Retourne la moyenne pondérée des quatre éléments de texture les plus proches du centre du pixel qui est texturé. Celles-ci peuvent inclure des éléments de texture de bordure, en fonction des valeurs des valeurs des \_ textures GL \_ \_ S, GL \_ texture \_ Wrap \_ T et sur le mappage exact. \_Le GL le plus proche est généralement plus rapide que \_ le GL linéaire, mais il peut produire des images texturées avec des arêtes plus nettes, car la transition entre les éléments de texture n’est pas aussi lisse. La valeur par défaut du \_ filtre GL texture \_ Mag \_ est \_ GL Linear.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ \_énumération non valide**</dt> </dl>     | *target* ou *pname* ne faisait pas partie des valeurs définies acceptées, ou lorsque *param* aurait dû avoir une valeur de constante définie (basée sur la valeur de *pname*) et ne l’a pas fait.<br/> |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/>                                            |



## <a name="remarks"></a>Remarques

Le mappage de texture est une technique qui applique une image sur la surface d’un objet comme si l’image était un cellophane de décalque ou de réduction. L’image est créée dans l’espace de texture, avec un système de coordonnées (*s*, *t*). Une texture est une image à une ou deux dimensions et un ensemble de paramètres qui déterminent la façon dont les échantillons sont dérivés de l’image.

La fonction **glTexParameter** assigne la ou les valeurs dans les paramètres au paramètre de texture spécifié comme pname. Le paramètre Target définit la texture cible, à savoir la texture GL \_ \_ 1D ou la \_ texture GL \_ 2D.

À mesure que d’autres éléments de texture sont échantillonnés dans le processus de minimisation, le nombre d’artefacts d’alias est apparent. Alors que les \_ fonctions de minimisation linéaires GL les plus proches et les plus proches \_ peuvent être plus rapides que les quatre autres, elles n’échantillonnent qu’un ou quatre éléments de texture pour déterminer la valeur de texture du pixel rendu et peuvent produire des modèles moire ou des transitions irrégulières. La valeur par défaut du \_ filtre de la texture GL \_ min est le \_ \_ MIPMAP linéaire le plus proche \_ \_ .

Supposons que la texturation est activée (en appelant [**glEnable**](glenable.md) avec \_ l’argument la texture GL \_ 1D ou la \_ texture GL \_ 2d) et \_ \_ \_ le filtre de la texture GL min est défini sur l’une des fonctions qui requièrent un mipmap. Si les dimensions des images de texture actuellement définies (avec des appels précédents à [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md)) ne suivent pas la séquence appropriée pour des mipmaps, ou si moins d’images de texture sont définies que nécessaire, ou si le jeu d’images de texture a des nombres différents de composants de texture, c’est comme si le mappage de texture était désactivé. Le filtrage linéaire accède aux quatre éléments de texture les plus proches uniquement dans les textures 2D. Dans les textures 1D, le filtrage linéaire accède aux deux éléments de texture les plus proches. La fonction suivante récupère des informations relatives à **glTexParameterf**, **glTexParameteri**, **glTexParameterfv** et **glTexParameteriv**:

[**glGetTexParameter**](glgettexparameter.md)

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

[glTexEnv](gltexenv-functions.md)
</dt> <dt>

[glTexGen](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





