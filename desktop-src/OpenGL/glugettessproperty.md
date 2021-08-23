---
title: gluGetTessProperty, fonction (Glu. h)
description: La fonction gluGetTessProperty obtient une propriété d’objet de pavage.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- gluGetTessProperty fonction OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d12e7ca8099197b663893b1edcf04dd8fa98348fe4f6d3d324b54f33904e026a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554239"
---
# <a name="glugettessproperty-function"></a>gluGetTessProperty fonction)

La fonction **gluGetTessProperty** obtient une propriété d’objet de pavage.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tess* 
</dt> <dd>

Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*et* 
</dt> <dd>

Propriété dont la valeur doit être récupérée. Les valeurs suivantes sont valides : \_ \_ règle d’enroulement Tess Glu \_ , limite de Glu \_ Tess \_ \_ uniquement et \_ tolérance Glu Tess \_ .

</dd> <dt>

*value* 
</dt> <dd>

Pointeur vers l’emplacement où la valeur de la propriété nommée est écrite.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Utilisez **gluGetTessProperty** pour récupérer les propriétés stockées dans un objet pavage. Ces propriétés affectent la manière dont les objets de pavage sont interprétés et rendus. Pour plus d’informations sur ce que sont les propriétés et sur ce qu’elles font, consultez [**gluTessProperty**](glutessproperty.md).

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

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





