---
title: fonction glGetTexImage (GL. h)
description: La fonction glGetTexImage retourne une image de texture.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- glGetTexImage fonction OpenGL
topic_type:
- apiref
api_name:
- glGetTexImage
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b116bc4ae517d0767d794767ad5232d8537033d62a099a3906f9f2ca96a7166c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493749"
---
# <a name="glgetteximage-function"></a>glGetTexImage fonction)

La fonction **glGetTexImage** retourne une image de texture.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetTexImage(
   GLenum target,
   GLint  level,
   GLenum format,
   GLenum type,
   GLvoid *pixels
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Spécifie la texture à obtenir. La \_ texture GL \_ 1D et la \_ texture GL \_ 2D sont acceptées.

</dd> <dt>

*level* 
</dt> <dd>

Numéro de niveau de détail de l’image souhaitée. Le niveau 0 est le niveau d’image de base. Le niveau *n* est la *n* ième image de réduction mipmap.

</dd> <dt>

*format* 
</dt> <dd>

Format de pixel pour les données retournées. Les formats pris en charge sont GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ alpha, GL \_ RGB, GL \_ RVBA, GL \_ luminance, GL \_ BGR \_ ext, GL \_ BGRA \_ ext et GL \_ luminance \_ alpha.

</dd> <dt>

*type* 
</dt> <dd>

Type de pixel pour les données retournées. Les types pris en charge sont \_ octets non signés GL \_ , \_ octet GL, GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int et GL \_ float.

</dd> <dt>

*pixels* 
</dt> <dd>

Retourne l’image de texture. Doit être un pointeur vers un tableau du type spécifié par *type*.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | la *cible*, le *format* ou le *type* n’était pas une valeur acceptée.<br/>                                                                    |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | le *niveau* est inférieur à zéro ou supérieur au *Journal* 2 (*Max*), où *Max* est la valeur retournée de la taille de \_ texture max GL \_ \_ .<br/>      |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md) .<br/> |



## <a name="remarks"></a>Remarques

La fonction **glGetTexImage** retourne une image de texture en *pixels*. Le *paramètre Target* spécifie si l’image de texture souhaitée est spécifiée par [**glTexImage1D**](glteximage1d.md)**(** texture GL \_ \_ 1D **)** ou par [**glTexImage2D**](glteximage2d.md)**(** texture GL \_ \_ 2D **)**. Le paramètre *Level* spécifie le numéro de niveau de détail de l’image souhaitée. Les paramètres de *type* et de *format* spécifient le format et le type du tableau d’images souhaité. Pour obtenir une description des valeurs acceptables pour les paramètres de *type* et de *format* , consultez **glTexImage1D** et [**glDrawPixels**](gldrawpixels.md).

L’opération de **glGetTexImage** est mieux comprise en considérant que l’image de texture à quatre composants interne sélectionnée est une mémoire tampon RVBA de la taille de l’image. La sémantique des **glGetTexImage** est alors identique à celle de [**glReadPixels**](glreadpixels.md) appelée avec le même *format* et le même *type*, *si x* et *y* ont la valeur zéro, la *largeur* est égale à la largeur de l’image de texture (y compris la bordure si elle a été spécifiée) et la *hauteur* est définie sur une pour les images 1D, ou à la hauteur de l’image de texture (y compris la bordure, si elle a été spécifiée) pour les images 2D.

Étant donné que l’image de texture interne est une image RVBA, les formats de pixels de l' \_ index de couleur GL \_ , de l’index de \_ stencils GL \_ et de la profondeur du GL ne \_ \_ sont pas acceptés, et le type de pixel de la \_ bitmap GL n’est pas accepté.

Si l’image de texture sélectionnée ne contient pas quatre composants, les mappages suivants sont appliqués. Les textures à un seul composant sont traitées comme des tampons RVBA avec la couleur rouge définie sur la valeur à composant unique, et les valeurs vert, bleu et alpha définies sur zéro.

Les textures à deux composants sont traitées comme des tampons RVBA, avec le rouge défini sur la valeur du composant zéro, alpha défini sur la valeur du composant 1 et le vert et le bleu définis sur zéro. Enfin, les textures à trois composants sont traitées comme des tampons RVBA avec le rouge défini sur le composant zéro, le vert défini sur le composant 1, le bleu défini sur le deuxième composant et alpha défini sur zéro.

Pour déterminer la taille requise des *pixels*, utilisez [**glGetTexLevelParameter**](glgettexlevelparameter.md) pour déterminer les dimensions de l’image de texture interne, puis mettez à l’échelle le nombre requis de pixels par le stockage requis pour chaque pixel, en fonction du *format* et du *type*. Veillez à prendre en compte les paramètres de stockage en pixels, en particulier l' \_ alignement du Pack GL \_ .

Si une erreur est générée, aucune modification n’est apportée au contenu des *pixels*.

Les fonctions suivantes récupèrent les informations relatives à **glGetTexImage**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument with GL \_ Pack \_ alignment et autres

[**glGetTexLevelParameter**](glgettexlevelparameter.md) avec l’argument \_ largeur de la texture GL \_

**glGetTexLevelParameter** avec argument \_ taille de texture de la comptabilité \_

**glGetTexLevelParameter** avec argument GL \_ texture \_ Border

**glGetTexLevelParameter** avec les \_ composants de texture GL d’argument \_

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

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





