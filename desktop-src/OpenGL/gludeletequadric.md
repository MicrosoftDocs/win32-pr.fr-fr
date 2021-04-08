---
title: gluDeleteQuadric, fonction (Glu. h)
description: La fonction gluDeleteQuadric détruit un objet quadric.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- gluDeleteQuadric fonction OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5ee85e943cd958e394efb191932393d228d948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742229"
---
# <a name="gludeletequadric-function"></a>gluDeleteQuadric fonction)

La fonction **gluDeleteQuadric** détruit un objet quadric.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*state* 
</dt> <dd>

Objet quadric à détruire (créé avec [**gluNewQuadric**](glunewquadric.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **gluDeleteQuadric** détruit l’objet quadric et libère toute mémoire qu’il utilisait. Une fois que vous avez appelé **gluDeleteQuadric**, vous ne pouvez plus utiliser l' *État* .

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

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





