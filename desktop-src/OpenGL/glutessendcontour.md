---
title: gluTessEndContour, fonction (Glu. h)
description: Les fonctions gluTessBeginContour et gluTessEndContour délimitent une description du contour. | gluTessEndContour, fonction (Glu. h)
ms.assetid: 115db079-cbcb-48e1-8bab-0eb4814afb82
keywords:
- gluTessEndContour fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessEndContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac53f3920476489a1453bb6b5dc1e01d650d4fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321993"
---
# <a name="glutessendcontour-function"></a>gluTessEndContour fonction)

Les fonctions [**gluTessBeginContour**](glutessbegincontour.md) et **gluTessEndContour** délimitent une description du contour.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluTessEndContour(
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

Les fonctions [**gluTessBeginContour**](glutessbegincontour.md) et **gluTessEndContour** délimitent la définition d’un contour de polygone. Au sein de chaque paire **gluTessBeginContour** / **gluTessEndContour** , il peut y avoir zéro ou plusieurs appels à [**gluTessVertex**](glutessvertex.md). Les sommets spécifient un contour fermé (le dernier vertex de chaque contour est automatiquement lié au premier). Vous pouvez appeler **gluTessBeginContour** uniquement entre [**gluTessBeginPolygon**](glutessbeginpolygon.md) et [**gluTessEndPolygon**](glutessendpolygon.md).

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

 

 





