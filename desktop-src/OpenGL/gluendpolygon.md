---
title: gluEndPolygon, fonction (Glu. h)
description: Les fonctions gluBeginPolygon et gluEndPolygon délimitent une description de polygone. | gluEndPolygon, fonction (Glu. h)
ms.assetid: fdb8cc73-c6c3-4377-aa5b-36a79791e7a9
keywords:
- gluEndPolygon fonction OpenGL
topic_type:
- apiref
api_name:
- gluEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf69bfb16f9c83462bbe6b53c86f319b3d09623
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011479"
---
# <a name="gluendpolygon-function"></a>gluEndPolygon fonction)

\[La fonction **gluEndPolygon** est obsolète et n’est fournie qu’à des fins de compatibilité descendante. La fonction **gluEndPolygon** est mappée à **GluTessEndPolygon** suivie de **gluTessEndContour**.\]

Les fonctions [**gluBeginPolygon**](glubeginpolygon.md) et **gluEndPolygon** délimitent une description de polygone.

## <a name="syntax"></a>Syntaxe


```C++
void gluEndPolygon(
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

Utilisez [**gluBeginPolygon**](glubeginpolygon.md) et **gluEndPolygon** pour délimiter la définition d’un polygone qui n’est pas convexe.

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

 

 





