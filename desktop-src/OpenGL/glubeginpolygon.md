---
title: gluBeginPolygon, fonction (Glu. h)
description: Les fonctions gluBeginPolygon et gluEndPolygon délimitent une description de polygone. | gluBeginPolygon, fonction (Glu. h)
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- gluBeginPolygon fonction OpenGL
topic_type:
- apiref
api_name:
- gluBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60204e7d937b4686f3757b520c820886e168529e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119173"
---
# <a name="glubeginpolygon-function"></a>gluBeginPolygon fonction)

\[La fonction **gluBeginPolygon** est obsolète et n’est fournie qu’à des fins de compatibilité descendante. La fonction **gluBeginPolygon** est mappée à [**GluTessBeginPolygon**](glutessbeginpolygon.md) suivie de [**gluTessBeginContour**](glutessbegincontour.md).\]

Les fonctions **gluBeginPolygon** et [**gluEndPolygon**](gluendpolygon.md) délimitent une description de polygone.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluBeginPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tess* 
</dt> <dd>

Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Utilisez **gluBeginPolygon** et **gluEndPolygon** pour délimiter la définition d’un polygone qui n’est pas convexe.

1.  Appelez **gluBeginPolygon**.
2.  Définissez les contournements du polygone en appelant [**gluTessVertex**](glutessvertex.md) pour chaque vertex et [**gluNextContour**](glunextcontour.md) pour démarrer chaque nouveau contour.
3.  Appelez **gluEndPolygon** pour signaler la fin de la définition.

    Une fois **gluEndPolygon** appelé, le polygone est fractionné et les triangles résultants sont décrits par le biais de rappels. Pour obtenir une description des fonctions de rappel, consultez [*gluTessCallback*](glutess.md).

## <a name="examples"></a>Exemples

L’exemple suivant décrit un quadrilatère avec un trou triangulaire :

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);
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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluNextContour**](glunextcontour.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





