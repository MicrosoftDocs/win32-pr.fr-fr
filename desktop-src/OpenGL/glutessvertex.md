---
title: gluTessVertex, fonction (Glu. h)
description: La fonction gluTessVertex spécifie un sommet sur un polygone.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- gluTessVertex fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546bbad2be1205f62c7889fbb18f23d5b0e38b8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509294"
---
# <a name="glutessvertex-function"></a>gluTessVertex fonction)

La fonction **gluTessVertex** spécifie un sommet sur un polygone.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tess* 
</dt> <dd>

Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*coordonnées* 
</dt> <dd>

Emplacement du vertex.

</dd> <dt>

*data* 
</dt> <dd>

Pointeur retourné au programme avec le rappel de vertex (comme spécifié par [*gluTessCallback*](glutess.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **gluTessVertex** décrit un vertex sur un polygone que l’utilisateur définit. Les appels **gluTessVertex** successifs décrivent un contour fermé. Par exemple, pour décrire un quadrangulaires, appelez **gluTessVertex** quatre fois. Vous pouvez uniquement appeler **gluTessVertex** entre [**gluTessBeginContour**](glutessbegincontour.md) et [**gluTessEndContour**](glutessendcontour.md).

Le paramètre de *données* pointe normalement vers une structure contenant l’emplacement du vertex, ainsi que d’autres attributs par vertex tels que la couleur et la normale. Ce pointeur est retourné au programme par le biais du \_ rappel de vertex Glu après pavage (voir [*gluTessCallback*](glutess.md)).

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

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





