---
title: gluTessEndPolygon, fonction (Glu. h)
description: Les fonctions gluTessBeginPolygon et gluTessEndPolygon délimitent une description de polygone. | gluTessEndPolygon, fonction (Glu. h)
ms.assetid: c9ae2075-59d7-4c1a-b720-0aa05954525c
keywords:
- gluTessEndPolygon fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65102f1627df682508725d46fc5fa299244e767c318382eacaf3585aa4a471e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061547"
---
# <a name="glutessendpolygon-function"></a>gluTessEndPolygon fonction)

Les fonctions [**gluTessBeginPolygon**](glutessbeginpolygon.md) et **gluTessEndPolygon** délimitent une description de polygone.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluTessEndPolygon(
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

## <a name="remarks"></a>Remarques

Les fonctions [**gluTessBeginPolygon**](glutessbeginpolygon.md) et **gluTessEndPolygon** délimitent la définition d’un polygone qui n’est pas convexe. Dans chaque paire **gluTessBeginPolygon**  /  **gluTessEndPolygon** , incluez un ou plusieurs appels à [**gluTessBeginContour**](glutessbegincontour.md). Au sein de chaque profil, il y a zéro ou plusieurs appels à [**gluTessVertex**](glutessvertex.md). Les sommets spécifient un contour fermé (le dernier vertex de chaque contour est automatiquement lié au premier).

Le paramètre de *\_ données Polygon* est un pointeur vers une structure de données définie par le programmeur. Si les rappels appropriés sont spécifiés (voir [*gluTessCallback*](glutess.md)), ce pointeur est retourné à la fonction ou aux fonctions de rappel, ce qui en fait un moyen pratique de stocker les informations par polygone.

Quand vous appelez **gluTessEndPolygon**, le polygone est fractionné et les triangles résultants sont décrits par le biais de rappels. Pour obtenir une description des fonctions de rappel, consultez [*gluTessCallback*](glutess.md).

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

 

 





