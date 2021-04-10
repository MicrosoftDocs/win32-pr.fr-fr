---
title: fonction glBitmap (GL. h)
description: La fonction glBitmap dessine une bitmap.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- glBitmap fonction OpenGL
topic_type:
- apiref
api_name:
- glBitmap
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb97bb16a1e3c4c29d1dfb1a5320c02f44404d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032966"
---
# <a name="glbitmap-function"></a>glBitmap fonction)

La fonction **glBitmap** dessine une bitmap.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glBitmap(
         GLSizei width,
         GLSizei height,
         GLfloat xorig,
         GLfloat yorig,
         GLfloat xmove,
         GLfloat ymove,
   const GLubyte *bitmap
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*width* 
</dt> <dd>

Largeur en pixels de l’image bitmap.

</dd> <dt>

*height* 
</dt> <dd>

Hauteur en pixels de l’image bitmap.

</dd> <dt>

*xorig* 
</dt> <dd>

Emplacement *x* de l’origine dans l’image bitmap. L’origine est mesurée à partir du coin inférieur gauche de la bitmap, avec des directions vers la droite et vers le haut étant les axes positifs.

</dd> <dt>

*yorig* 
</dt> <dd>

Emplacement *y* de l’origine dans l’image bitmap. L’origine est mesurée à partir du coin inférieur gauche de la bitmap, avec des directions vers la droite et vers le haut étant les axes positifs.

</dd> <dt>

*xmove* 
</dt> <dd>

Décalage *x* à ajouter à la position de la trame actuelle après le dessin de la bitmap.

</dd> <dt>

*ymove* 
</dt> <dd>

Décalage *y* à ajouter à la position de la trame actuelle après le dessin de la bitmap.

</dd> <dt>

*bitmap* 
</dt> <dd>

Adresse de l’image bitmap.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *largeur* ou la *hauteur* est négative.<br/>                                                                                           |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

Une image bitmap est une image binaire. Lorsqu’elle est dessinée, la bitmap est positionnée par rapport à la position actuelle du raster, et trame pixels correspondant aux 1s dans le bitmap sont écrits à l’aide de la couleur ou de l’index raster actuel. Les pixels de la mémoire tampon de trame correspondant aux zéros dans l’image bitmap ne sont pas modifiés.

L’image bitmap est interprétée comme des données image pour la fonction [**glDrawPixels**](gldrawpixels.md) , avec la *largeur* et la *hauteur* correspondant aux arguments Width et Height de cette fonction, et avec le *type* défini sur bitmap GL \_ et le *format* défini sur l’index de \_ couleurs GL \_ . Les modes que vous spécifiez à l’aide de [**glPixelStore**](glpixelstore-functions.md) affectent l’interprétation des données de l’image bitmap ; les modes que vous spécifiez à l’aide de [**glPixelTransfer**](glpixeltransfer.md) ne le sont pas.

Si la position raster actuelle n’est pas valide, **glBitmap** est ignoré. Dans le cas contraire, l’angle inférieur gauche de l’image bitmap est positionné aux coordonnées de la fenêtre suivante :

*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*?

*y*<sub>w</sub>  =  *o*<sub>r</sub> *y*?

Dans ces coordonnées, (*x*<sub>r</sub> , *y*<sub>r</sub> ) est la position raster et (*x*? , *y*? ) est l’origine de l’image bitmap. Les fragments sont ensuite générés pour chaque pixel correspondant à un 1 dans l’image bitmap. Ces fragments sont générés à l’aide de la coordonnée *z* de trame actuelle, de l’index de couleur ou de couleur et des coordonnées de texture raster actuelles. Ils sont ensuite traités comme s’ils avaient été générés à l’aide d’un point, d’une ligne ou d’un polygone, y compris le mappage de texture, le surlignage et toutes les opérations par fragment, telles que le test alpha et de profondeur.

Une fois que l’image bitmap a été dessinée, les coordonnées *x* et *y* de la position raster actuelle sont décalées par *xmove* et *ymove*. Aucune modification n’est apportée à la coordonnée *z* de la position du raster actuel ou aux coordonnées de couleur, d’index ou de texture raster actuelles.

Les fonctions suivantes récupèrent les informations relatives à la fonction **glBitmap** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ position

 

**glGet** avec argument GL \_ Current \_ Raster \_ couleur

 

**glGet** avec argument GL \_ Current \_ Raster \_ index

 

**glGet** avec argument de \_ la \_ texture de TRAMe actuelle du \_ GL \_

 

**glGet** avec argument GL \_ Current \_ Raster \_ position \_ valide

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

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> </dl>

 

 





