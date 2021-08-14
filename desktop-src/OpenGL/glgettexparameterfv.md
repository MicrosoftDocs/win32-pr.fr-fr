---
title: fonction glGetTexParameterfv (GL. h)
description: Les fonctions glGetTexParameterfv et glGetTexParameteriv retournent des valeurs de paramètre de texture. | fonction glGetTexParameterfv (GL. h)
ms.assetid: 616292ea-222c-4efe-bb69-3058d9c99910
keywords:
- glGetTexParameterfv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7925ae070a3e35f6c9b3a9ba65ff506f775b77e625dc852b49cc305c76003428
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359709"
---
# <a name="glgettexparameterfv-function"></a>glGetTexParameterfv fonction)

Les fonctions **glGetTexParameterfv** et [**glGetTexParameteriv**](glgettexparameteriv.md) retournent des valeurs de paramètre de texture.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetTexParameterfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Nom symbolique de la texture cible. La \_ texture GL \_ 1D et la \_ texture GL \_ 2D sont acceptées.

</dd> <dt>

*pname* 
</dt> <dd>

Nom symbolique d’un paramètre de texture. Les valeurs suivantes sont acceptées.



| Valeur                                                                                                                                                                                         | Signification                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**filtre de la \_ texture GL \_ \_**</dt> </dl>       | Retourne le filtre d’agrandissement de texture à valeur unique, une constante symbolique.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**filtre de la \_ texture GL \_ min. \_**</dt> </dl>       | Retourne le filtre de réduction de la texture à valeur unique, une constante symbolique.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**\_ \_ encapsuler la texture GL \_ S**</dt> </dl>                   | Retourne la fonction d’encapsulation à valeur unique pour les coordonnées de texture *s*, une constante symbolique.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**\_enveloppe de \_ la texture GL \_ T**</dt> </dl>                   | Retourne la fonction d’encapsulation à valeur unique pour la coordonnée de texture *t*, une constante symbolique.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**couleur de bordure de la \_ texture GL \_ \_**</dt> </dl> | Retourne quatre nombres entiers ou à virgule flottante qui composent la couleur RVBA de la bordure de texture. Les valeurs à virgule flottante sont retournées dans la plage \[ 0, 1 \] . Les valeurs entières sont retournées sous la forme d’un mappage linéaire de la représentation à virgule flottante interne, de sorte que 1,0 correspond à l’entier représentable le plus positif et-1,0 correspond à l’entier pouvant être représenté le plus négatif.<br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**\_priorité de texture GL \_**</dt> </dl>              | Retourne la priorité de résidence de la texture cible (ou de la texture nommée qui lui est liée). La valeur initiale est 1. Consultez [**glPrioritizeTextures**](glprioritizetextures.md).<br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <dt>**la \_ texture du GL \_ résident**</dt> </dl>              | Retourne l’état de résidence de la texture cible. Si la valeur retournée dans params est définie sur GL \_ true, la texture réside dans la mémoire de texture. Consultez [**glAreTexturesResident**](glaretexturesresident.md).<br/>                                                                                                                                                                           |



 

</dd> <dt>

*params* 
</dt> <dd>

Retourne les paramètres de texture.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | la *cible* ou le *nom* n’était pas une valeur acceptée.<br/>                                                                              |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glGetTexParameter** *retourne in paramètre* la valeur ou les valeurs du paramètre de texture spécifié comme *pname*. Le paramètre *target* définit la texture cible, à savoir la texture GL \_ \_ 1D ou la \_ texture GL \_ 2D, pour spécifier une texturation unidimensionnelle ou à deux dimensions. Le paramètre *pname* accepte les mêmes symboles que [**glTexParameter**](gltexparameter-functions.md), avec les mêmes interprétations.

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

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





