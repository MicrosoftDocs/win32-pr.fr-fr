---
title: gluQuadricDrawStyle, fonction (Glu. h)
description: La fonction gluQuadricDrawStyle spécifie le style de dessin souhaité pour Quadrics.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- gluQuadricDrawStyle fonction OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a1b44b7894ea9762b450c5a5d6c2b022c5e02f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194360"
---
# <a name="gluquadricdrawstyle-function"></a>gluQuadricDrawStyle fonction)

La fonction **gluQuadricDrawStyle** spécifie le style de dessin souhaité pour Quadrics.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*quadObject* 
</dt> <dd>

Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*drawStyle* 
</dt> <dd>

Style de dessin souhaité. Les valeurs suivantes sont valides.



| Valeur                                                                                                                                                            | Signification                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <dt>**GLU \_ remplissage**</dt> </dl>                   | Les Quadrics sont rendus avec des primitives de polygone. Les polygones sont dessinés dans le sens inverse des aiguilles d’une déroute en ce qui concerne leurs normales (comme défini avec [**gluQuadricOrientation**](gluquadricorientation.md)).<br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <dt>**\_ligne Glu**</dt> </dl>                   | Les Quadrics sont rendus sous la forme d’un ensemble de lignes.<br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <dt>**\_silhouette Glu**</dt> </dl> | Les Quadrics sont rendus sous la forme d’un ensemble de lignes, sauf que les bords qui délimitent les visages coplanés ne sont pas dessinés.<br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <dt>**\_point Glu**</dt> </dl>                | Les Quadrics sont rendus sous la forme d’un ensemble de points.<br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **gluQuadricDrawStyle** spécifie le style de dessin pour Quadrics rendu avec **quadObject**.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





