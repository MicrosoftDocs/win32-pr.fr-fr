---
title: gluSphere, fonction (Glu. h)
description: La fonction gluSphere dessine une sphère.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- gluSphere fonction OpenGL
topic_type:
- apiref
api_name:
- gluSphere
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ff4833c705aae34fdb7830c264fee91414116
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416698"
---
# <a name="glusphere-function"></a>gluSphere fonction)

La fonction **gluSphere** dessine une sphère.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluSphere(
   GLUquadric *qobj,
   GLdouble   radius,
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

*service* 
</dt> <dd>

Rayon de la sphère.

</dd> <dt>

*fraction* 
</dt> <dd>

Nombre de sous-divisions autour de l’axe des z (comme les lignes de longitude).

</dd> <dt>

*piles* 
</dt> <dd>

Nombre de sous-divisions le long de l’axe z (comme les lignes de latitude).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **gluSphere** dessine une sphère du rayon donné centrée autour de l’origine. La sphère est divisée autour de l’axe z en tranches et le long de l’axe z en piles (comme les lignes de longitude et de latitude).

Si l’orientation est définie sur GLU \_ en dehors de (avec **gluQuadricOrientation**), les normales générées pointent à partir du centre de la sphère. Dans le cas contraire, ils pointent vers le centre de la sphère.

Si la texturation est activée (avec **gluQuadricTexture**) : des coordonnées de texture sont générées afin que *t* s’étende de 0,0 à *z* =-*RADIUS* à 1,0 au   =  *rayon* z (*t* augmente de façon linéaire sur les lignes longitudinales); et *s* vont de 0,0 sur l’axe des y positif, à 0,25 à l’axe des x positif, à 0,5 à l’axe y négatif, à 0,75 à l’axe des x négatif et à la valeur 1,0 sur l’axe des y positif.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**gluCylinder**](glucylinder.md)
</dt> <dt>

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





