---
title: fonction glCopyTexImage2D (GL. h)
description: La fonction glCopyTexImage2D copie les pixels du trame dans une image de texture à deux dimensions.
ms.assetid: 4b9d7be6-054d-4590-b3f0-a2a670786c4b
keywords:
- glCopyTexImage2D fonction OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d04a979e9bb026da904687506f3201d12c12c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311818"
---
# <a name="glcopyteximage2d-function"></a>glCopyTexImage2D fonction)

La fonction **glCopyTexImage2D** copie les pixels du trame dans une image de texture à deux dimensions.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glCopyTexImage2D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLint   border
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

*internalFormat* 
</dt> <dd>

Format interne et résolution des données de texture. Les valeurs 1, 2, 3 et 4 ne sont pas acceptées pour *internalFormat*. Le paramètre peut prendre l’une des valeurs symboliques suivantes.



| Constante                 | Bits R | Bits G | Bits B | Un bits | L bits | I bits |
|--------------------------|--------|--------|--------|--------|--------|--------|
| GL \_ alpha                |        |        |        |        |        |        |
| \_Alpha4 GL               |        |        |        | 4      |        |        |
| \_ALPHA8 GL               |        |        |        | 8      |        |        |
| \_ALPHA12 GL              |        |        |        | 12     |        |        |
| \_ALPHA16 GL              |        |        |        | 16     |        |        |
| LUMINANCE du GL \_            |        |        |        |        |        |        |
| \_LUMINANCE4 GL           |        |        |        |        | 4      |        |
| \_LUMINANCE8 GL           |        |        |        |        | 8      |        |
| \_LUMINANCE12 GL          |        |        |        |        | 12     |        |
| \_LUMINANCE16 GL          |        |        |        |        | 16     |        |
| \_luminance \_ alpha du GL     |        |        |        |        |        |        |
| GL \_ LUMINANCE4 \_ alpha4   |        |        |        | 4      | 4      |        |
| GL \_ LUMINANCE6 \_ alpha2   |        |        |        | 2      | 6      |        |
| GL \_ LUMINANCE8 \_ ALPHA8   |        |        |        | 8      | 8      |        |
| GL \_ LUMINANCE12 \_ alpha4  |        |        |        | 4      | 12     |        |
| GL \_ LUMINANCE12 \_ ALPHA12 |        |        |        | 12     | 12     |        |
| GL \_ LUMINANCE16 \_ ALPHA16 |        |        |        | 16     | 16     |        |
| intensité du GL \_            |        |        |        |        |        |        |
| \_INTENSITY4 GL           |        |        |        |        |        | 4      |
| \_INTENSITY8 GL           |        |        |        |        |        | 8      |
| \_INTENSITY12 GL          |        |        |        |        |        | 12     |
| \_INTENSITY16 GL          |        |        |        |        |        | 16     |
| \_RGB GL                  |        |        |        |        |        |        |
| GL \_ R3 \_ G3 \_ a2           | 3      | 3      | 2      |        |        |        |
| \_RGB4 GL                 | 4      | 4      | 4      |        |        |        |
| \_RGB5 GL                 | 5      | 5      | 5      |        |        |        |
| \_RGB8 GL                 | 8      | 8      | 8      |        |        |        |
| \_RGB10 GL                | 10     | 10     | 10     |        |        |        |
| \_RGB12 GL                | 12     | 12     | 12     |        |        |        |
| \_RGB16 GL                | 16     | 16     | 16     |        |        |        |
| GL \_ RVBA                 |        |        |        |        |        |        |
| \_RGBA2 GL                | 2      | 2      | 2      | 2      |        |        |
| \_RGBA4 GL                | 4      | 4      | 4      | 4      |        |        |
| GL \_ RGB5 \_ a1             | 5      | 5      | 5      | 1      |        |        |
| \_RGBA8 GL                | 8      | 8      | 8      | 8      |        |        |
| GL \_ RGB10 \_ a2            | 10     | 10     | 10     | 2      |        |        |
| \_RGBA12 GL               | 12     | 12     | 12     | 12     |        |        |
| \_RGBA16 GL               | 16     | 16     | 16     | 16     |        |        |



 

</dd> <dt>

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

Largeur de l’image de texture. Doit être \*  de 2 x 2 pour un entier *n*.

</dd> <dt>

*height* 
</dt> <dd>

Hauteur de l’image de texture. Doit être \*  de 2 x 2 pour un entier *n*.

</dd> <dt>

*2S* 
</dt> <dd>

Largeur de la bordure. Doit être égal à zéro ou égal à 1.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | la *cible* n’est pas une valeur acceptée.<br/>                                                                                                               |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | le *niveau* était inférieur à zéro ou supérieur à log2 *Max*, où *Max* est la valeur retournée de la \_ taille de texture max GL \_ \_ .<br/>                               |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *bordure* n’était pas égale à zéro ou 1.<br/>                                                                                                                       |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *largeur* était inférieure à zéro, supérieure à 2 + \_ taille maximale de la texture GL \_ \_ , ou la *largeur* ne peut pas être représentée sous la forme 2n + 2 \*  pour un entier *n*.<br/> |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/>                        |



## <a name="remarks"></a>Notes

La fonction **glCopyTexImage2D** définit une image de texture à deux dimensions à l’aide de pixels du trame actuel, plutôt qu’à partir de la mémoire principale comme c’est le cas pour [**glTexImage2D**](glteximage2d.md).

À l’aide du niveau de mipmap spécifié avec *Level*, les tableaux de texture sont définis comme un rectangle de pixels avec l’angle inférieur gauche situé aux coordonnées *x* et *y*, largeur égale à la *largeur* + (2 \* *bordure*) et une hauteur égale à *hauteur* + (2 \* *bordure*). Le format interne du tableau de texture est spécifié avec le paramètre *internalFormat* .

La fonction **glCopyTexImage2D** traite les pixels d’une ligne de la même façon que [**glCopyPixels**](glcopypixels.md) , sauf qu’avant la conversion finale des pixels, toutes les valeurs de composant de pixel sont ancrées à la plage \[ 0, 1 \] et converties au format interne de la texture pour le stockage dans le tableau de texture. L’ordonnancement des pixels est déterminé par des coordonnées *x* et *y* inférieures correspondant à des coordonnées de texture *s* et *t* inférieures. Si l’un des pixels dans une ligne spécifiée du trame actuel est en dehors de la fenêtre associée au contexte de rendu actuel, ses valeurs ne sont pas définies.

Vous ne pouvez pas inclure d’appels à **glCopyTexImage2D** dans des listes d’affichage.

> [!Note]  
> La fonction **glCopyTexImage2D** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.

 

La texturation n’a aucun effet dans le mode d’index des couleurs. Les fonctions [**glPixelStore**](glpixelstore-functions.md) et [**glPixelTransfer**](glpixeltransfer.md) affectent les images de texture exactement de la même façon qu’elles affectent [**glDrawPixels**](gldrawpixels.md).

La fonction suivante récupère des informations relatives à **glCopyTexImage2D**:

[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ 2D

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

[**glCopyTexImage1D**](glcopyteximage1d.md)
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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





