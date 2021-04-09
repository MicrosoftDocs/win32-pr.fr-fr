---
title: gluDisk, fonction (Glu. h)
description: La fonction gluDisk dessine un disque.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- gluDisk fonction OpenGL
topic_type:
- apiref
api_name:
- gluDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9a9e8b547790049c93360f060e944aafcea4511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032828"
---
# <a name="gludisk-function"></a>gluDisk fonction)

La fonction **gluDisk** dessine un disque.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*qobj* 
</dt> <dd>

Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*innerRadius* 
</dt> <dd>

Rayon interne du disque (peut être égal à zéro).

</dd> <dt>

*outerRadius* 
</dt> <dd>

Rayon externe du disque.

</dd> <dt>

*fraction* 
</dt> <dd>

Nombre de sous-divisions autour de l’axe z.

</dd> <dt>

*boucles* 
</dt> <dd>

Nombre de sonneries concentriques sur l’origine dans laquelle le disque est subdivisé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **gluDisk** restitue un disque sur le plan *z* = 0. Le disque a un rayon de *outerRadius* et contient un trou circulaire concentrique avec un rayon de *innerRadius*. Si *innerRadius* a la valeur 0, aucun trou n’est généré. Le disque est divisé autour de l’axe z en tranches (comme les tranches de pizzas), ainsi que sur l’axe z dans les anneaux (comme spécifié par les *tranches* et les *boucles*, respectivement).

En ce qui concerne l’orientation, le côté *z* positif du disque est considéré comme *extérieur* (voir [**gluQuadricOrientation**](gluquadricorientation.md)). Cela signifie que si l’orientation est définie sur GLU \_ en dehors de, les normales sont générées le long de l’axe z positif.

Si la texturation est activée (avec [**gluQuadricTexture**](gluquadrictexture.md)), des coordonnées de texture sont générées de façon linéaire, où *r*  =  *outerRadius*, la valeur de (*r*, 0, 0) est (1, 0,5); à (0, *r*, 0) il est (0,5, 1); à (-*r*, 0, 0) il est (0, 0,5); et à (0,-*r*, 0) il est (0,5, 0).

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

[**gluCylinder**](glucylinder.md)
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

 

 





