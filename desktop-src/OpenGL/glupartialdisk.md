---
title: gluPartialDisk, fonction (Glu. h)
description: La fonction gluPartialDisk dessine un arc de disque.
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- gluPartialDisk fonction OpenGL
topic_type:
- apiref
api_name:
- gluPartialDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 687738cce6bb311d7e8223877b716abdaef180340ab570f430659ee2e98458ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519439"
---
# <a name="glupartialdisk-function"></a>gluPartialDisk fonction)

La fonction **gluPartialDisk** dessine un arc de disque.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluPartialDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops,
   GLdouble   startAngle,
   GLdouble   sweepAngle
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

Rayon interne du disque partiel (peut être égal à zéro).

</dd> <dt>

*outerRadius* 
</dt> <dd>

Rayon externe du disque partiel.

</dd> <dt>

*fraction* 
</dt> <dd>

Nombre de sous-divisions autour de l’axe z.

</dd> <dt>

*boucles* 
</dt> <dd>

Nombre de sonneries concentriques sur l’origine dans laquelle le disque partiel est subdivisé.

</dd> <dt>

*startAngle* 
</dt> <dd>

Angle de départ, en degrés, de la partie disque.

</dd> <dt>

*sweepAngle* 
</dt> <dd>

Angle de balayage, en degrés, de la partie disque.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La fonction **gluPartialDisk** restitue un disque partiel sur le plan *z* = 0. Un disque partiel est similaire à un disque complet, sauf que seul le sous-ensemble du disque de *startAngle* à *startAngle*  +  *SweepAngle* est inclus (où 0 degré est le long de l’axe des y positif, 90 degrés sur l’axe x positif, 180 degrés sur l’axe y négatif et 270 degrés sur l’axe x négatif).

Le disque partiel a un rayon de *outerRadius* et contient un trou circulaire concentrique avec un rayon de *innerRadius*. Si *innerRadius* est égal à zéro, aucun trou n’est généré. Le disque partiel est divisé autour de l’axe z en tranches (comme les tranches de pizzas), ainsi que sur l’axe z dans les anneaux (comme spécifié par les *tranches* et les *boucles*, respectivement).

En ce qui concerne l’orientation, le côté z positif du disque partiel est considéré comme extérieur (voir [**gluQuadricOrientation**](gluquadricorientation.md)). Cela signifie que si l’orientation est définie sur GLU \_ en dehors de, les normales sont générées le long de l’axe z positif.

Si vous avez activé la texturation (avec [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** génère des coordonnées de texture linéairement, où *r*  =  *outerRadius*, la valeur de *(r*, 0, 0) est (1, 0,5); à (0, *r*, 0) il est (0,5, 1); à (*r*, 0, 0) il est (0, 0,5); et à (0, *r*, 0) il est (0,5, 0).

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

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





