---
title: fonction glGetTexLevelParameteriv (GL. h)
description: Les fonctions glGetTexLevelParameterfv et glGetTexLevelParameteriv retournent des valeurs de paramètre de texture pour un niveau de détail spécifique. | fonction glGetTexLevelParameteriv (GL. h)
ms.assetid: 536d7bc9-1599-47ff-8559-374f96f1d5f3
keywords:
- glGetTexLevelParameteriv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a52830d673516d38512c0763603a30bf66ad9a564d186c6988c0634027eb1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359765"
---
# <a name="glgettexlevelparameteriv-function"></a>glGetTexLevelParameteriv fonction)

Les fonctions [**glGetTexLevelParameterfv**](glgettexlevelparameterfv.md) et **glGetTexLevelParameteriv** retournent des valeurs de paramètre de texture pour un niveau de détail spécifique.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetTexLevelParameteriv(
   GLenum target,
   GLint  level,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Nom symbolique de la texture cible : la texture GL \_ \_ 1D, la texture \_ GL \_ 2D, la \_ texture du proxy GL \_ \_ 1D ou la \_ texture du proxy GL \_ \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Numéro de niveau de détail de l’image souhaitée. Le niveau 0 est le niveau d’image de base. Le niveau *n* est la *n* ième image de réduction mipmap.

</dd> <dt>

*pname* 
</dt> <dd>

Nom symbolique d’un paramètre de texture. Les noms de paramètres suivants sont acceptés.



| Valeur                                                                                                                                                                                                  | Signification                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <dt>**largeur de la \_ texture GL \_**</dt> </dl>                                | Le paramètre *params* retourne une valeur unique contenant la largeur de l’image de texture. Cette valeur comprend la bordure de l’image de texture.<br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <dt>**hauteur de la \_ texture GL \_**</dt> </dl>                             | Le paramètre *params* retourne une valeur unique contenant la hauteur de l’image de texture. Cette valeur comprend la bordure de l’image de texture.<br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <dt>**\_ \_ format interne de la texture GL \_**</dt> </dl> | Le paramètre *params* retourne une valeur unique qui décrit le format Texel de la texture.<br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <dt>**bordure de la \_ texture GL \_**</dt> </dl>                             | Le paramètre *params* retourne une valeur unique : la largeur en pixels de la bordure de l’image de texture.<br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <dt>**taille de la texture GL en \_ \_ rouge \_**</dt> </dl>                      | La résolution de stockage interne du composant rouge d’une Texel. La résolution choisie par OpenGL sera une correspondance proche de la résolution demandée par l’utilisateur avec l’argument Component de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).<br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <dt>**\_ \_ taille verte de la texture GL \_**</dt> </dl>                | Résolution de stockage interne de la composante verte d’un Texel. La résolution choisie par OpenGL sera une correspondance proche de la résolution demandée par l’utilisateur avec l’argument Component de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).<br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <dt>**\_ \_ taille bleue de la texture GL \_**</dt> </dl>                   | Résolution de stockage interne de la composante bleue d’un Texel. La résolution choisie par OpenGL sera une correspondance proche de la résolution demandée par l’utilisateur avec l’argument Component de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).<br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <dt>**\_ \_ taille alpha de la texture GL \_**</dt> </dl>                | Résolution de stockage interne du composant alpha d’un Texel. La résolution choisie par OpenGL sera une correspondance proche de la résolution demandée par l’utilisateur avec l’argument Component de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).<br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <dt>**taille de luminance de la \_ texture GL \_ \_**</dt> </dl>    | Résolution de stockage interne de la composante luminance d’un Texel. La résolution choisie par OpenGL sera une correspondance proche de la résolution demandée par l’utilisateur avec l’argument Component de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).<br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <dt>**taille d’intensité de la \_ texture GL \_ \_**</dt> </dl>    | Résolution de stockage interne du composant d’intensité d’un Texel. La résolution choisie par OpenGL sera une correspondance proche de la résolution demandée par l’utilisateur avec l’argument Component de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).<br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <dt>**\_composants de texture GL \_**</dt> </dl>                 | Le paramètre *params* retourne une valeur unique : le nombre de composants dans l’image de texture.<br/>                                                                                                                                                                                          |



 

</dd> <dt>

*params* 
</dt> <dd>

Retourne les données demandées.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *target* ou *pname* n’est pas une valeur acceptée.<br/>                                                                             |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | le *niveau* est inférieur à zéro ou supérieur au *Journal* 2 *(max)*, où *Max* est la valeur retournée de la taille de \_ texture max GL \_ \_ .<br/>      |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glGetTexLevelParameter** retourne les valeurs des paramètres *de texture des paramètres pour* une valeur de niveau de détail spécifique, spécifiée comme *niveau*. Le paramètre *target* définit la texture cible, à savoir la \_ texture GL 1D, la texture \_ GL \_ \_ 2D, la texture du \_ proxy GL \_ \_ 1D ou la \_ \_ texture du proxy GL \_ 2D pour spécifier la texturation unidimensionnelle ou à deux dimensions. Le paramètre *pname* spécifie le paramètre de texture dont la valeur ou les valeurs seront retournées.

Si une erreur est générée, aucune modification n’est apportée au contenu des *paramètres*.

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

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





