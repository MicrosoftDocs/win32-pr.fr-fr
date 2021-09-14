---
title: gluBeginCurve, fonction (Glu. h)
description: Les fonctions gluBeginCurve et gluEndCurve délimitent une définition de courbe B-spline rationnelle non uniforme (NURBS). | gluBeginCurve, fonction (Glu. h)
ms.assetid: f7f2e765-1a07-4faa-940c-9cb957dd54d4
keywords:
- gluBeginCurve fonction OpenGL
topic_type:
- apiref
api_name:
- gluBeginCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4e17bd88cfcb49801450ead865c437843d179b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119178"
---
# <a name="glubegincurve-function"></a>gluBeginCurve fonction)

Les fonctions **gluBeginCurve** et [**gluEndCurve**](gluendcurve.md) délimitent une définition de courbe B-spline rationnelle non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluBeginCurve(
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

Utilisez **gluBeginCurve** pour marquer le début d’une définition de courbe NURBS. Après avoir appelé **gluBeginCurve**, effectuez un ou plusieurs appels à [**gluNurbsCurve**](glunurbscurve.md) pour définir les attributs de la courbe. Exactement l’un des appels à **gluNurbsCurve** doit avoir un type de courbe GL \_ Map1 \_ vertex \_ 3 ou GL \_ Map1 \_ vertex \_ 4. Pour marquer la fin de la définition de courbe NURBS, appelez [**gluEndCurve**](gluendcurve.md).

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

 

 





