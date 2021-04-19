---
title: gluCylinder, fonction (Glu. h)
description: La fonction gluCylinder dessine un cylindre.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- gluCylinder fonction OpenGL
topic_type:
- apiref
api_name:
- gluCylinder
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fd201d1ddd720501715d1ead08d94bab72f7b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106531619"
---
# <a name="glucylinder-function"></a>gluCylinder fonction)

La fonction **gluCylinder** dessine un cylindre.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluCylinder(
   GLUquadric *qobj,
   GLdouble   baseRadius,
   GLdouble   topRadius,
   GLdouble   height,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*qobj* 
</dt> <dd>

Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*baseRadius* 
</dt> <dd>

Rayon de la bouteille à *z* = 0.

</dd> <dt>

*Rayon* 
</dt> <dd>

Rayon de la bouteille à la   =  *hauteur* z.

</dd> <dt>

*height* 
</dt> <dd>

Hauteur du cylindre.

</dd> <dt>

*fraction* 
</dt> <dd>

Nombre de sous-divisions autour de l’axe z.

</dd> <dt>

*piles* 
</dt> <dd>

Nombre de sous-divisions le long de l’axe z.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **gluCylinder** dessine un cylindre orienté le long de l’axe z. La base du cylindre est placée à *z* = 0 et la hauteur en haut à *z*  =  . À l’instar d’une sphère, un cylindre est divisé autour de l’axe z en tranches et le long de l’axe z en piles.

Notez que si la valeur de la valeur de *rayon* est égale à zéro, cette routine générera un cône.

Si l’orientation est définie sur GLU \_ en dehors de (avec [**gluQuadricOrientation**](gluquadricorientation.md)), les normales générées pointent à l’extérieur de l’axe z. Dans le cas contraire, ils pointent vers l’axe z.

Si la texturation est activée (avec [**gluQuadricTexture**](gluquadrictexture.md)) : des coordonnées de texture sont générées de façon à ce que *t* s’étende de manière linéaire de 0,0 à *z* = 0 à 1,0 à   =  la *hauteur* z ; et *s* s’étendent de 0,0 à l’axe des y positif, à 0,25 à l’axe des x positif, à 0,5 à l’axe y négatif, à 0,75 à l’axe des x négatif, et à 1,0 à l’axe des y

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





