---
title: fonction glGenTextures (GL. h)
description: La fonction glGenTextures génère des noms de texture.
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- glGenTextures fonction OpenGL
topic_type:
- apiref
api_name:
- glGenTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204a5d4fb736a88cf615577f4c740cde15d75829
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942740"
---
# <a name="glgentextures-function"></a>glGenTextures fonction)

La fonction **glGenTextures** génère des noms de texture.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGenTextures(
   GLsizei n,
   GLuint  *textures
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*n* 
</dt> <dd>

Nombre de noms de texture à générer.

</dd> <dt>

*texture* 
</dt> <dd>

Pointeur vers le premier élément d’un tableau dans lequel les noms de texture générés sont stockés.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | *n* était une valeur négative.<br/>                                                                                                  |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glGenTextures** retourne *n* noms de texture dans le paramètre *textures* . Toutefois, les noms de texture ne sont pas nécessairement un ensemble contigu d’entiers. Toutefois, aucun des noms retournés ne peut être en cours d’utilisation juste avant l’appel de la fonction **glGenTextures** . Les textures générées supposent la dimensionnalité de la cible de texture à laquelle elles sont liées pour la première fois avec la fonction [**glBindTexture**](glbindtexture.md) . Les noms de texture retournés par **glGenTextures** ne sont pas retournés par les appels suivants à **glGenTextures** , sauf s’ils sont d’abord supprimés en appelant [**glDeleteTextures**](gldeletetextures.md).

Vous ne pouvez pas inclure des **glGenTextures** dans des listes d’affichage.

> [!Note]  
> La fonction **glGenTextures** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.

 

La fonction suivante récupère des informations relatives à **glGenTextures**:

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glDeleteTextures**](gldeletetextures.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





