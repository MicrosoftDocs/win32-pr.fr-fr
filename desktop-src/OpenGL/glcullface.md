---
title: fonction glCullFace (GL. h)
description: La fonction glCullFace spécifie si les facettes frontales ou les faces arrière peuvent être éliminées.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- glCullFace fonction OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941779"
---
# <a name="glcullface-function"></a>glCullFace fonction)

La fonction **glCullFace** spécifie si les facettes frontales ou les faces arrière peuvent être éliminées.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mode* 
</dt> <dd>

Spécifie si les facettes frontales ou les faces arrière sont des candidats pour l’élimination. Les constantes symboliques \_ Front-Front, GL \_ Back et GL \_ front \_ et \_ Back sont acceptées. La valeur par défaut est \_ back du GL.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *mode* n’était pas une valeur acceptée.<br/>                                                                                          |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glCullFace** spécifie si les facettes avant ou arrière sont éliminées (comme spécifié par le *mode*) lorsque l’élimination des facettes est activée. Vous activez et désactivez l’élimination des facettes à l’aide de [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument GL \_ Culling \_ . Les facettes sont des triangles, des quadrilatères, des polygones et des rectangles.

La fonction [**glFrontFace**](glfrontface.md) spécifie les facettes dans le sens des aiguilles d’une montre et de l’arrière-plan.

Si le *mode* est \_ recto- \_ \_ verso et arrière, aucune facette n’est dessinée, mais d’autres primitives, telles que des points et des lignes, sont dessinées.

Les fonctions suivantes récupèrent les informations relatives à **glCullFace**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Culling \_ \_ en mode visage

[**glIsEnabled**](glisenabled.md) avec argument GL \_ élimination \_ visage

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFrontFace**](glfrontface.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





