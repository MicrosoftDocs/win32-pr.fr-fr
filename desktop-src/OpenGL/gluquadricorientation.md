---
title: gluQuadricOrientation, fonction (Glu. h)
description: La fonction gluQuadricOrientation spécifie l’orientation à l’intérieur ou à l’extérieur pour Quadrics.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- gluQuadricOrientation fonction OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baa02c3b6d207cbcc2bf487f51c0e96dc2f2dd98748edc81efb58ac957fac4ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937625"
---
# <a name="gluquadricorientation-function"></a>gluQuadricOrientation fonction)

La fonction **gluQuadricOrientation** spécifie l’orientation à l’intérieur ou à l’extérieur pour Quadrics.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*quadObject* 
</dt> <dd>

Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*orientation* 
</dt> <dd>

Orientation souhaitée. Les valeurs suivantes sont valides.



| Valeur                                                                                                                                                   | Signification                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <dt>**GLU \_ en dehors**</dt> </dl> | Dessinez des Quadrics avec des normales pointant vers l’extérieur. Il s'agit de la valeur par défaut.<br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <dt>**GLU \_ dans**</dt> </dl>    | Dessinez des Quadrics avec des normales pointant vers l’intérieur.<br/>                             |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La fonction **gluQuadricOrientation** spécifie le type d’orientation souhaité pour Quadrics rendu avec **quadObject**. L’interprétation de l’extérieur et de l’intérieur dépend de l’quadric dessiné.

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
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





