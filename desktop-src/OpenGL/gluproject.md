---
title: gluProject, fonction (Glu. h)
description: La fonction gluProject mappe les coordonnées d’objet aux coordonnées de la fenêtre.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- gluProject fonction OpenGL
topic_type:
- apiref
api_name:
- gluProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324f6c896c225453bfc8bf2ebb4b8619707c498c75e1309ea24fc6557cdd3deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488808"
---
# <a name="gluproject-function"></a>gluProject fonction)

La fonction **gluProject** mappe les coordonnées d’objet aux coordonnées de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
int WINAPI gluProject(
         GLdouble objx,
         GLdouble objy,
         GLdouble objz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *winx,
         GLdouble *winy,
         GLdouble *winz
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*objx* 
</dt> <dd>

Coordonnée de l’objet x.

</dd> <dt>

*objy* 
</dt> <dd>

Coordonnée de l’objet y.

</dd> <dt>

*objz* 
</dt> <dd>

Coordonnée de l’objet z.

</dd> <dt>

*modelMatrix* 
</dt> <dd>

Matrice modelview actuelle (à partir d’un appel [**glGetDoublev**](glgetdoublev.md) ).

</dd> <dt>

*projMatrix* 
</dt> <dd>

La matrice de projection actuelle (à partir d’un appel **glGetDoublev** ).

</dd> <dt>

*vue* 
</dt> <dd>

La fenêtre d’affichage actuelle (à partir d’un appel [**glGetIntegerv**](glgetintegerv.md) ).

</dd> <dt>

*winx* 
</dt> <dd>

Coordonnée x de la fenêtre calculée.

</dd> <dt>

*winy* 
</dt> <dd>

Coordonnée de la fenêtre y calculée.

</dd> <dt>

*winz* 
</dt> <dd>

Coordonnée de la fenêtre z calculée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est GL \_ true.

Si la fonction échoue, la valeur de retour est GL \_ false.

## <a name="remarks"></a>Remarques

La fonction **gluProject** transforme les coordonnées d’objet spécifiées en coordonnées de fenêtre à l’aide de *modelMatrix*, *projMatrix* et *Viewport*. Le résultat est stocké dans *Winx*, *winy* et *WINZ*.

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

[**glGetDoublev**](glgetdoublev.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluUnProject**](gluunproject.md)
</dt> </dl>

 

 





