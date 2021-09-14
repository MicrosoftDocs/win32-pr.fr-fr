---
title: gluUnProject, fonction (Glu. h)
description: La fonction gluUnProject mappe les coordonnées de la fenêtre aux coordonnées de l’objet.
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- gluUnProject fonction OpenGL
topic_type:
- apiref
api_name:
- gluUnProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45311171dd3d71c9e699953c049e0813f2df361
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011452"
---
# <a name="gluunproject-function"></a>gluUnProject fonction)

La fonction **gluUnProject** mappe les coordonnées de la fenêtre aux coordonnées de l’objet.

## <a name="syntax"></a>Syntaxe


```C++
int WINAPI gluUnProject(
         GLdouble winx,
         GLdouble winy,
         GLdouble winz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *objx,
         GLdouble *objy,
         GLdouble *objz
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*winx* 
</dt> <dd>

Coordonnée de fenêtre x à mapper.

</dd> <dt>

*winy* 
</dt> <dd>

Coordonnée de fenêtre y à mapper.

</dd> <dt>

*winz* 
</dt> <dd>

Coordonnée de fenêtre z à mapper.

</dd> <dt>

*modelMatrix* 
</dt> <dd>

Matrice modelview (à partir d’un appel [**glGetDoublev**](glgetdoublev.md) ).

</dd> <dt>

*projMatrix* 
</dt> <dd>

Matrice de projection (à partir d’un appel **glGetDoublev** ).

</dd> <dt>

*vue* 
</dt> <dd>

La fenêtre d’affichage (à partir d’un appel [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).

</dd> <dt>

*objx* 
</dt> <dd>

Coordonnée de l’objet x calculé.

</dd> <dt>

*objy* 
</dt> <dd>

Coordonnée de l’objet y calculé.

</dd> <dt>

*objz* 
</dt> <dd>

Coordonnée de l’objet z calculé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, la valeur de retour est GL \_ true.

Si la fonction échoue, la valeur de retour est GL \_ false.

## <a name="remarks"></a>Notes

La fonction **gluUnProject** mappe les coordonnées de fenêtre spécifiées en coordonnées d’objet à l’aide de *modelMatrix*, *projMatrix* et *Viewport*. Le résultat est stocké dans *objX*, *objy* et *objz*.

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

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetDoublev**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluProject**](gluproject.md)
</dt> </dl>

 

 





