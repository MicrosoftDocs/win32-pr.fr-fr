---
title: fonction glFrontFace (GL. h)
description: La fonction glFrontFace définit les polygones frontaux et de face arrière.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- glFrontFace fonction OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106fa40989f21e50eb738f1a218394e8e7e9b4bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942819"
---
# <a name="glfrontface-function"></a>glFrontFace fonction)

La fonction **glFrontFace** définit les polygones frontaux et de face arrière.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mode* 
</dt> <dd>

Orientation des polygones frontaux. \_Les wrappers en PV GL et GL \_ sont acceptés. La valeur par défaut est le \_ CCW GL.

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

Dans une scène composée entièrement de surfaces fermées opaques, les polygones de l’arrière-plan ne sont jamais visibles. L’élimination de ces polygones invisibles présente l’avantage évident de accélérer le rendu de l’image. Vous activez et désactivez l’élimination des polygones de type « arrière » avec [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) à l’aide de l’argument GL \_ Culling \_ .

La projection d’un polygone sur les coordonnées de la fenêtre est dite d’enroulement dans le sens des aiguilles d’une montre si un objet imaginaire suivant le chemin de son premier vertex, son deuxième vertex, etc. jusqu’au dernier vertex, et enfin vers son premier vertex, se déplace dans le sens des aiguilles d’une montre à propos de l’intérieur du polygone. L’enroulement du polygone est dit être placé dans le sens inverse des aiguilles d’une montre si l’objet imaginaire qui suit le même chemin se déplace dans le sens inverse des aiguilles d’une montre à l’intérieur du polygone. La fonction **glFrontFace** spécifie si les polygones avec un enroulement dans le sens des aiguilles d’une montre dans les coordonnées de la fenêtre ou dans le sens inverse des aiguilles d’une montre. Le passage \_ du CCW du GL au *mode* sélectionne les polygones dans le sens inverse. Le \_ PV GL sélectionne les polygones dans le sens des aiguilles d’une montre. Par défaut, les polygones à gauche sont pris en face.

La fonction suivante récupère des informations sur **glFrontface**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ frontal \_

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

[**glCullFace**](glcullface.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





