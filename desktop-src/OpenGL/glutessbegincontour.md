---
title: gluTessBeginContour, fonction (Glu. h)
description: Les fonctions gluTessBeginContour et gluTessEndContour délimitent une description du contour. | gluTessBeginContour, fonction (Glu. h)
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
keywords:
- gluTessBeginContour fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28efc96c977e5e0483b4f3d87e9ce840b985cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523144"
---
# <a name="glutessbegincontour-function"></a>gluTessBeginContour fonction)

Les fonctions **gluTessBeginContour** et [**gluTessEndContour**](glutessendcontour.md) délimitent une description du contour.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluTessBeginContour(
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

Les fonctions **gluTessBeginContour** et [**gluTessEndPolygon**](glutessendpolygon.md) délimitent la définition d’un contour de polygone. Au sein de chaque paire **gluTessBeginContour** / **gluTessEndPolygon** , il peut y avoir zéro ou plusieurs appels à [**gluTessVertex**](glutessvertex.md). Les sommets spécifient un contour fermé (le dernier vertex de chaque contour est automatiquement lié au premier). Vous pouvez appeler **gluTessBeginContour** uniquement entre [**gluTessBeginPolygon**](glutessbeginpolygon.md) et **gluTessEndPolygon**.

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

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





