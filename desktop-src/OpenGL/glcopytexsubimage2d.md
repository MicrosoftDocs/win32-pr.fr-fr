---
title: fonction glCopyTexSubImage2D (GL. h)
description: La fonction glCopyTexSubImage2D copie une sous-image d’une image de texture à deux dimensions à partir du trame.
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- glCopyTexSubImage2D fonction OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c966d031bb154b59cc54ae2e5d254347aa88d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384819"
---
# <a name="glcopytexsubimage2d-function"></a>glCopyTexSubImage2D fonction)

La fonction **glCopyTexSubImage2D** copie une sous-image d’une image de texture à deux dimensions à partir du trame.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glCopyTexSubImage2D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   yoffset,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Cible dans laquelle les données de l’image seront modifiées. Doit avoir la texture GL de valeur \_ \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Numéro de niveau de détail. Le niveau 0 est l’image de base. Le niveau *n* est la *n* ième image de réduction mipmap.

</dd> <dt>

*xoffset* 
</dt> <dd>

Décalage de Texel dans la direction *x* dans le tableau de texture.

</dd> <dt>

*yoffset* 
</dt> <dd>

Décalage de Texel dans la direction *y* dans le tableau de texture.

</dd> <dt>

*x* 
</dt> <dd>

Coordonnées du plan x de la fenêtre du coin inférieur gauche de la ligne de pixels à copier.

</dd> <dt>

*y* 
</dt> <dd>

Coordonnées du plan y de la fenêtre du coin inférieur gauche de la ligne de pixels à copier.

</dd> <dt>

*width* 
</dt> <dd>

Largeur de la sous-image de l’image de texture. La spécification d’une sous-image de texture avec une largeur nulle n’a aucun effet.

</dd> <dt>

*height* 
</dt> <dd>

Hauteur de la sous-image de l’image de texture. La spécification d’une sous-image de texture avec une largeur nulle n’a aucun effet.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | la *cible* n’est pas une valeur acceptée.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | le *niveau* était inférieur à zéro ou supérieur au *Journal* 2 (*Max*), où *Max* est la valeur retournée de la taille de \_ texture max GL \_ \_ .<br/>                                                                                                                                                                                          |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | *xoffset* était inférieur à *Border* ou (*xoffset*  +  *Width*) était supérieur à (  +  *Border*), *YOFFSET* était inférieur à *Border*, ou (*YOFFSET*  +  *Height*) était supérieur à (  +  *Border*), où *w* est la \_ largeur de la texture GL et la \_ *bordure* est la bordure de la \_ texture GL \_ . Notez que *w* comprend deux fois la largeur de la *bordure* .<br/> |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *largeur* était inférieure à la *bordure* ou *y* était inférieure à la *bordure*, où *Border* correspond à la largeur de la bordure du tableau de texture.<br/>                                                                                                                                                                                           |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | Le tableau de texture n’a pas été défini par une opération [**glTexImage1D**](glteximage1d.md) précédente.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/>                                                                                                                                                                                       |



## <a name="remarks"></a>Notes

La fonction **glCopyTexSubImage2D** remplace une partie rectangulaire d’une image de texture à deux dimensions par des pixels du trame actuel, plutôt qu’à partir de la mémoire principale comme c’est le cas pour [**glTexSubImage2D**](gltexsubimage2d.md).

Un rectangle de pixels commençant par les coordonnées de fenêtre *x* et *y* et avec la *largeur* et la *hauteur* des dimensions remplace la partie du tableau de texture par les index *xoffset* à *xoffset* + (*Width* -1), les index *YOFFSET* à *YOFFSET* + (*Width* -1) au niveau du mipmap spécifié par *Level*. Le rectangle de destination dans le tableau de texture ne peut pas inclure de texels à l’extérieur du tableau de texture spécifié à l’origine.

La fonction **glCopyTexSubImage2D** traite les pixels d’une ligne de la même façon que [**glCopyPixels**](glcopypixels.md), sauf qu’avant la conversion finale des pixels, toutes les valeurs de composant de pixel sont ancrées à la plage \[ 0, 1 \] et converties au format interne de la texture pour le stockage dans le tableau de texture. L’ordonnancement des pixels est déterminé par des coordonnées *x* inférieures correspondant à des coordonnées de texture inférieures. Si l’un des pixels dans une ligne spécifiée du trame actuel est en dehors de la fenêtre associée au contexte de rendu actuel, ses valeurs ne sont pas définies.

Si l’un des pixels du rectangle spécifié du trame actuel est en dehors de la fenêtre de lecture associée au contexte de rendu actuel, les valeurs obtenues pour ces pixels ne sont pas définies. Aucune modification n’est apportée au paramètre de *internalFormat*, de *largeur*, de *hauteur* ou de *bordure* du tableau de texture spécifié ou aux valeurs texels en dehors de la sous-image de texture spécifiée.

Vous ne pouvez pas inclure d’appels à **glCopyTexSubImage2D** dans des listes d’affichage.

> [!Note]  
> La fonction **glCopyTexSubImage2D** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.

 

La texturation n’a aucun effet dans le mode d’index des couleurs. Les fonctions [**glPixelStore**](glpixelstore-functions.md) et [**glPixelTransfer**](glpixeltransfer.md) affectent les images de texture exactement comme elles affectent la façon dont les pixels sont dessinés à l’aide de [**glDrawPixels**](gldrawpixels.md).

Les fonctions suivantes récupèrent les informations relatives à **glCopyTexSubImage2D**:

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexSubImage1D**](glcopytexsubimage1d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





