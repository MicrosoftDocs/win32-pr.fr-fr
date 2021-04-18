---
title: gluBeginSurface, fonction (Glu. h)
description: Les fonctions gluBeginSurface et gluEndSurface délimitent une définition de surface de B-spline rationnelle (NURBS) non uniforme. | gluBeginSurface, fonction (Glu. h)
ms.assetid: 7189f05e-0c4d-4f82-8a82-a51fcc51b202
keywords:
- gluBeginSurface fonction OpenGL
topic_type:
- apiref
api_name:
- gluBeginSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd09030290f78fac987a52cddd977a502dda06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106543011"
---
# <a name="glubeginsurface-function"></a>gluBeginSurface fonction)

Les fonctions **gluBeginSurface** et [**gluEndSurface**](gluendsurface.md) délimitent une définition de surface de B-spline rationnelle ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluBeginSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nobj* 
</dt> <dd>

Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les fonctions **gluBeginSurface** et **gluEndSurface** marquent le début et la fin des définitions de la surface NURBS, qui sont définies avec des appels à **gluNurbsSurface**.

1.  Appelez **gluBeginSurface** pour marquer le début d’une définition de surface NURBS.
2.  Effectuez un ou plusieurs appels à **gluNurbsSurface** pour définir les attributs de la surface.

    Exactement l’un de ces appels à **gluNurbsSurface** doit avoir un type de surface de \_ map2 des vertex 1 \_ \_ ou GL \_ map2 \_ vertex \_ 4.

3.  Pour marquer la fin de la définition de la surface NURBS, appelez **gluEndSurface**.

Les fonctions [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md)et [**gluEndTrim**](gluendtrim.md) prennent en charge la suppression des surfaces NURBS.

Utilisez les évaluateurs OpenGL pour afficher la surface NURBS sous la forme d’un ensemble de polygones. Conserver l’état de l’évaluateur lors du rendu avec [**glPushAttrib**](glpushattrib.md)( \_ bit d’évaluation GL \_ ) et [**glPopAttrib**](glpopattrib.md).

## <a name="examples"></a>Exemples

Les fonctions suivantes affichent une surface NURBS texturée avec des normales ; les coordonnées de la texture et les normales sont également décrites comme des surfaces NURBS :

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
```

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

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluNurbsSurface**](glunurbssurface.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





