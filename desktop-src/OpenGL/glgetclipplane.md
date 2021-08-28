---
title: fonction glGetClipPlane (GL. h)
description: La fonction glGetClipPlane retourne les coefficients du plan de découpage spécifié.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- glGetClipPlane fonction OpenGL
topic_type:
- apiref
api_name:
- glGetClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf551356088db2b99b79a28a396be785ab60f2196cc3e27353cb867d4b151dd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742038"
---
# <a name="glgetclipplane-function"></a>glGetClipPlane fonction)

La fonction **glGetClipPlane** retourne les coefficients du plan de découpage spécifié.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*plane (avion)* 
</dt> <dd>

Plan de découpage. Le nombre de plans de découpage dépend de l’implémentation, mais au moins six plans de découpage sont pris en charge. Ils sont identifiés par des noms symboliques de la forme \_ plan de clip GL \_ *i* où 0 = *i* < des plans de \_ clip GL Max \_ \_ .

</dd> <dt>

*Sommaire* 
</dt> <dd>

Retourne quatre valeurs à double précision qui sont les coefficients de l' *équation plane du plan en coordonnées* oculaires.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *plan* n’est pas une valeur acceptée.<br/>                                                                                         |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glGetClipPlane** retourne dans l' *équation* les quatre coefficients de l’équation plane pour le *plan*.

C’est toujours le cas dans le cadre du \_ plan de clip GL \_ *i* = GL \_ clip \_ PLANE0 + *i*.

Si une erreur est générée, aucune modification n’est apportée au contenu de l' *équation*.

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

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





