---
title: gluEndCurve, fonction (Glu. h)
description: Les fonctions gluBeginCurve et gluEndCurve délimitent une définition de courbe B-spline rationnelle non uniforme (NURBS). | gluEndCurve, fonction (Glu. h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- gluEndCurve fonction OpenGL
topic_type:
- apiref
api_name:
- gluEndCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49f6c0c08bf31135ca82e87d2093ef3b57197955
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106540919"
---
# <a name="gluendcurve-function"></a>gluEndCurve fonction)

Les fonctions [**gluBeginCurve**](glubegincurve.md) et **gluEndCurve** délimitent une définition de courbe B-spline rationnelle non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluEndCurve(
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

Utilisez [**gluBeginCurve**](glubegincurve.md) pour marquer le début d’une définition de courbe NURBS. Après avoir appelé **gluBeginCurve**, effectuez un ou plusieurs appels à [**gluNurbsCurve**](glunurbscurve.md) pour définir les attributs de la courbe. Exactement l’un des appels à **gluNurbsCurve** doit avoir un type de courbe GL \_ Map1 \_ vertex \_ 3 ou GL \_ Map1 \_ vertex \_ 4. Pour marquer la fin de la définition de courbe NURBS, appelez **gluEndCurve**.

Les évaluateurs OpenGL permettent d’afficher la courbe NURBS sous la forme d’une série de segments de ligne. L’état de l’évaluateur est préservé pendant le rendu avec [**glPushAttrib**](glpushattrib.md) ( \_ bit d’évaluation GL \_ ) et [**glPopAttrib**](glpopattrib.md). Pour plus d’informations sur l’état exact que ces appels conservent, consultez **glPushAttrib**.

## <a name="examples"></a>Exemples

Les fonctions suivantes affichent une courbe NURBS texturée avec des normales ; les coordonnées de texture et les normales sont également spécifiées comme courbes NURBS :

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
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

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> </dl>

 

 





