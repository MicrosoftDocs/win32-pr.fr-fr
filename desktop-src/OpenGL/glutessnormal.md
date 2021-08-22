---
title: gluTessNormal, fonction (Glu. h)
description: La fonction gluTessNormal spécifie un normal pour un polygone.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- gluTessNormal fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2db848c6971fe2893f2bc2cd4ca33e96811dda0d44e81e8a852cd441a6478d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488469"
---
# <a name="glutessnormal-function"></a>gluTessNormal fonction)

La fonction **gluTessNormal** spécifie un normal pour un polygone.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tess* 
</dt> <dd>

Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*x* 
</dt> <dd>

Composant de coordonnée x d’un normal.

</dd> <dt>

*y* 
</dt> <dd>

Composant de coordonnée y d’un normal.

</dd> <dt>

*Lettre* 
</dt> <dd>

Composant de coordonnée z d’un normal.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La fonction **gluTessNormal** décrit un normal pour un polygone que vous définissez. Toutes les données d’entrée sont projetées sur un plan perpendiculaire à l’un des trois axes de coordonnées avant la polygonalisation, et tous les triangles de sortie sont orientés vers le sens inverse des aiguilles d’une dépassement en respectant la normale. (Pour obtenir l’orientation dans le sens des aiguilles d’une montre, inversez le signe de la normale fournie). Par exemple, si vous savez que tous les polygones se trouvent dans le plan x-y, appelez **gluTessNormal**(tess, 0,0, 0,0, 1,0) avant de restituer des polygones.

Si la normale fournie est (0,0, 0,0, 0,0) (valeur par défaut), la normale est déterminée comme suit :

1.  La direction de la normale, jusqu’à son signe, est trouvée en raccordant un plan aux sommets, sans tenir compte de la façon dont les sommets sont connectés. Il est prévu que les données d’entrée se trouvent approximativement dans le plan ; dans le cas contraire, la projection perpendiculaire à l’un des trois axes de coordonnées peut modifier la géométrie de manière substantielle.
2.  Le signe de la normale est choisi afin que la somme des zones signées de toutes les contournements d’entrée soit non négative (où un contour à gauche a une zone positive).

Le normal fourni persiste jusqu’à ce qu’un autre appel à **gluTessNormal** le modifie.

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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> </dl>

 

 





