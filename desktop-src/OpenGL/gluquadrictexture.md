---
title: gluQuadricTexture, fonction (Glu. h)
description: La fonction gluQuadricTexture spécifie si les Quadrics doivent être texturés.
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- gluQuadricTexture fonction OpenGL
topic_type:
- apiref
api_name:
- gluQuadricTexture
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbde88e0a878fd59e01ad0a450cf4cbe9831c4ad867c8029373586a8efe830eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937480"
---
# <a name="gluquadrictexture-function"></a>gluQuadricTexture fonction)

La fonction **gluQuadricTexture** spécifie si les Quadrics doivent être texturés.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*quadObject* 
</dt> <dd>

Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*textureCoords* 
</dt> <dd>

Indicateur qui spécifie si les coordonnées de texture doivent être générées. Les valeurs suivantes sont valides.



| Valeur                                                                                                                                          | Signification                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <dt>**GL \_ true**</dt> </dl>    | Générer des coordonnées de texture.<br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <dt>**GL- \_ faux**</dt> </dl> | Ne générez pas de coordonnées de texture. Il s'agit de la valeur par défaut.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La fonction **gluQuadricTexture** spécifie si les coordonnées de texture doivent être générées pour Quadrics rendu avec **quadObject**.

La manière dont les coordonnées de texture sont générées dépend du rendu quadric spécifique.

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
</dt> </dl>

 

 





