---
title: fonction glDeleteTextures (GL. h)
description: La fonction glDeleteTextures supprime les textures nommées.
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- glDeleteTextures fonction OpenGL
topic_type:
- apiref
api_name:
- glDeleteTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408019d3bfe226c9e7ecdc2ea00182a0b11c78fa64a0210be658ded4556850cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617044"
---
# <a name="gldeletetextures-function"></a>glDeleteTextures fonction)

La fonction **glDeleteTextures** supprime les textures nommées.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glDeleteTextures(
         GLsizei n,
   const GLuint  *textures
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*n* 
</dt> <dd>

Nombre de textures à supprimer.

</dd> <dt>

*texture* 
</dt> <dd>

Tableau de textures à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | *n* était une valeur négative.<br/>                                                                                                  |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glDeleteTextures** supprime *n* textures nommées par les éléments du tableau *textures*. Une fois qu’une texture est supprimée, elle n’a pas de contenu ou de dimensionnalité, et son nom est libre en vue de sa réutilisation (par exemple, par **glGenTextures**). La fonction **glDeleteTextures** ignore les zéros et les noms qui ne correspondent pas aux textures existantes.

Si une texture actuellement liée est supprimée, la liaison revient à zéro (texture par défaut).

Vous ne pouvez pas inclure d’appels à **glDeleteTextures** dans des listes d’affichage.

> [!Note]  
> La fonction **glDeleteTextures** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.

 

La fonction suivante récupère des informations relatives à **glDeleteTextures**:

-   [**glIsTexture**](glistexture.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothèque<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glAreTexturesResident**](glaretexturesresident.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





