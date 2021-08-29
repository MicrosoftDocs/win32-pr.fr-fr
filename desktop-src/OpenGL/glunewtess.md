---
title: gluNewTess, fonction (Glu. h)
description: La fonction gluNewTess crée un objet pavage.
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
keywords:
- gluNewTess fonction OpenGL
topic_type:
- apiref
api_name:
- gluNewTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc0d11b18425431eadca22f3c541eecf0f3c194b8c6ce897932c33d1674b179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519579"
---
# <a name="glunewtess-function"></a>gluNewTess fonction)

La fonction **gluNewTess** crée un objet pavage.

## <a name="syntax"></a>Syntaxe


```C++
GLUtesselator* WINAPI gluNewTess(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="remarks"></a>Remarques

La fonction **gluNewTess** crée et retourne un pointeur vers un nouvel objet pavage. Fait référence à cet objet lors de l’appel de fonctions de pavage. Une valeur de retour de zéro signifie qu’il n’y a pas assez de mémoire à allouer à l’objet.

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

[**gluDeleteTess**](gludeletetess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> </dl>

 

 





