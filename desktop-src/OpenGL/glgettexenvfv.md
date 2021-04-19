---
title: fonction glGetTexEnvfv (GL. h)
description: Les fonctions glGetTexEnvfv et glGetTexEnviv retournent les paramètres d’environnement de texture. | fonction glGetTexEnvfv (GL. h)
ms.assetid: aa037494-e227-48f1-8d5e-9f82073dc2ea
keywords:
- glGetTexEnvfv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnvfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36d542461b05a824c78bbad82d843735289f2fb4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522302"
---
# <a name="glgettexenvfv-function"></a>glGetTexEnvfv fonction)

Les fonctions **glGetTexEnvfv** et [**glGetTexEnviv**](glgettexenviv.md) retournent les paramètres d’environnement de texture.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetTexEnvfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Environnement de texture. Doit être une \_ texture GL \_ env.

</dd> <dt>

*pname* 
</dt> <dd>

Nom symbolique d’un paramètre d’environnement de texture. Les valeurs suivantes sont acceptées.



| Valeur                                                                                                                                                                                | Signification                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <dt>**\_ \_ mode env de la texture GL \_**</dt> </dl>    | Le paramètre *params* retourne le mode d’environnement de texture à valeur unique, une constante symbolique.<br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <dt>**couleur de la texture du GL \_ \_ env \_**</dt> </dl> | Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante qui sont la couleur de l’environnement de texture. Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à l’entier pouvant être représenté le plus positif, et-1,0 correspond à l’entier représentable le plus négatif.<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Retourne les données demandées.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *target* ou *pname* n’est pas une valeur acceptée.<br/>                                                                             |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glGetTexEnv** retourne dans *params* les valeurs sélectionnées d’un environnement de texture qui a été spécifié avec [**glTexEnv**](gltexenv-functions.md). Le paramètre *target* spécifie un environnement de texture. Actuellement, un seul environnement de texture est défini et pris en charge : la \_ texture GL \_ env.

Le paramètre *pname* désigne un paramètre d’environnement de texture spécifique.

Si une erreur est générée, aucune modification n’est apportée au contenu des *paramètres*.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





