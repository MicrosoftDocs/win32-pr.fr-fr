---
title: gluTessBeginPolygon, fonction (Glu. h)
description: Les fonctions gluTessBeginPolygon et gluTessEndPolygon délimitent une description de polygone. | gluTessBeginPolygon, fonction (Glu. h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- gluTessBeginPolygon fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34fad4c620890df109449b9a222d3355041ac77f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011466"
---
# <a name="glutessbeginpolygon-function"></a>gluTessBeginPolygon fonction)

Les fonctions **gluTessBeginPolygon** et [**gluTessEndPolygon**](glutessendpolygon.md) délimitent une description de polygone.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tess* 
</dt> <dd>

Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*\_données Polygon* 
</dt> <dd>

Pointeur vers une structure de données de polygone définie par le programmeur.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les fonctions **gluTessBeginPolygon** et [**gluTessEndPolygon**](glutessendpolygon.md) délimitent la définition d’un polygone qui n’est pas convexe. Dans chaque paire **gluTessBeginPolygon**  /  **gluTessEndPolygon** , incluez un ou plusieurs appels à [**gluTessBeginContour**](glutessbegincontour.md). Au sein de chaque profil, il y a zéro ou plusieurs appels à [**gluTessVertex**](glutessvertex.md). Les sommets spécifient un contour fermé (le dernier vertex de chaque contour est automatiquement lié au premier).

Le paramètre de *\_ données Polygon* est un pointeur vers une structure de données définie par le programmeur. Si les rappels appropriés sont spécifiés (voir [*gluTessCallback*](glutess.md)), ce pointeur est retourné à la fonction ou aux fonctions de rappel, ce qui en fait un moyen pratique de stocker les informations par polygone.

Quand vous appelez [**gluTessEndPolygon**](glutessendpolygon.md), le polygone est fractionné et les triangles résultants sont décrits par le biais de rappels. Pour obtenir une description des fonctions de rappel, consultez [*gluTessCallback*](glutess.md).

## <a name="examples"></a>Exemples

Les éléments suivants décrivent un quadrilatère avec un trou triangulaire :

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
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

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





