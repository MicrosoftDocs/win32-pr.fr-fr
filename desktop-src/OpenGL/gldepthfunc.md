---
title: fonction glDepthFunc (GL. h)
description: La fonction glDepthFunc spécifie la valeur utilisée pour les comparaisons de mémoire tampon de profondeur.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- glDepthFunc fonction OpenGL
topic_type:
- apiref
api_name:
- glDepthFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dec5130edb0b8ef30af1397be501fa9cd5d5744
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311793"
---
# <a name="gldepthfunc-function"></a>glDepthFunc fonction)

La fonction **glDepthFunc** spécifie la valeur utilisée pour les comparaisons de mémoire tampon de profondeur.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glDepthFunc(
   GLenum func
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*func* 
</dt> <dd>

Spécifie la fonction de comparaison de profondeur. Les constantes symboliques suivantes sont acceptées.



| Valeur                                                                                                                                                   | Signification                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ jamais**</dt> </dl>          | Ne passe jamais.<br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ moins**</dt> </dl>             | Passe si la valeur *z* entrante est inférieure à la valeur *z* stockée. Il s’agit de la valeur par défaut.<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**\_LEQUAL GL**</dt> </dl>       | Passe si la valeur z entrante est inférieure ou égale à la valeur z stockée.<br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ égal**</dt> </dl>          | Passe si la valeur z entrante est égale à la valeur z stockée.<br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ supérieur**</dt> </dl>    | Passe si la valeur z entrante est supérieure à la valeur z stockée.<br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**\_NOTEQUAL GL**</dt> </dl> | Passe si la valeur z entrante n’est pas égale à la valeur z stockée.<br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**\_GEQUAL GL**</dt> </dl>       | Passe si la valeur z entrante est supérieure ou égale à la valeur z stockée.<br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**\_toujours GL**</dt> </dl>       | Passe toujours.<br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glDepthFunc** spécifie la fonction utilisée pour comparer chaque valeur *z* de pixel entrante avec la valeur *z* présente dans la mémoire tampon de profondeur. La comparaison est effectuée uniquement si le test de profondeur est activé. (Voir [**glEnable**](glenable.md) avec l’argument GL \_ TEST de profondeur \_ .)

Au départ, le test de profondeur est désactivé.

Les fonctions suivantes récupèrent les informations relatives à **glDepthFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ profondeur \_ Func

[**glIsEnabled**](glisenabled.md) avec argument de profondeur du GL d’arguments \_ \_

## <a name="requirements"></a>Spécifications



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

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





