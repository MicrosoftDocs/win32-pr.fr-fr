---
title: fonction glIsTexture (GL. h)
description: La fonction glIsTexture détermine si un nom correspond à une texture.
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
keywords:
- glIsTexture fonction OpenGL
topic_type:
- apiref
api_name:
- glIsTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db28b6892d5aa0e9eaf98aec50b02ad102db8ba549474c673c6c0d918d799d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493349"
---
# <a name="glistexture-function"></a>glIsTexture fonction)

La fonction **glIsTexture** détermine si un nom correspond à une texture.

## <a name="syntax"></a>Syntaxe


```C++
GLboolean WINAPI glIsTexture(
   GLuint texture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*motif* 
</dt> <dd>

Valeur qui est le nom d’une texture.

</dd> </dl>

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

Si le paramètre de *texture* est actuellement le nom d’une texture, la fonction **glIsTexture** retourne la \_ valeur GL true. La fonction **glIsTexture** retourne GL \_ false si la *texture* est égale à zéro. Elle retourne également \_ le GL false s’il s’agit d’une valeur différente de zéro qui n’est pas le nom d’une texture actuellement, ou si une erreur se produit.

Vous ne pouvez pas inclure d’appels à **glIsTexture** dans des listes d’affichage.

> [!Note]  
> La fonction **glIsTexture** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.

 

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





