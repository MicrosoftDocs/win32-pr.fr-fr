---
title: fonction glStencilOp (GL. h)
description: La fonction glStencilOp définit les actions de test de stencil.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- glStencilOp fonction OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da899207456cece58216874c7540a032326e4180e9484590e2effd619eea72f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614333"
---
# <a name="glstencilop-function"></a>glStencilOp fonction)

La fonction **glStencilOp** définit les actions de test de stencil.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*incident* 
</dt> <dd>

Action à effectuer en cas d’échec du test du stencil. Les six constantes symboliques suivantes sont acceptées.



| Valeur                                                                                                                                                | Signification                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <dt>**conserver le GL \_**</dt> </dl>          | Conserve la valeur actuelle.<br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <dt>**\_zéro GL**</dt> </dl>          | Définit la valeur de la mémoire tampon du stencil sur zéro.<br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <dt>**remplacement du GL \_**</dt> </dl> | Définit la valeur de la mémoire tampon du stencil sur *ref*, comme spécifié par **glStencilFunc**.<br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <dt>**incrémental du GL \_**</dt> </dl>          | Incrémente la valeur de la mémoire tampon du stencil actuelle. S’attache à la valeur non signée maximale représentable.<br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <dt>**\_DECR (GL**</dt> </dl>          | Décrémente la valeur de la mémoire tampon du stencil actuelle. La valeur de est ancrée à zéro.<br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ inversée**</dt> </dl>    | L’opération de bits inverse la valeur de la mémoire tampon du stencil actuelle.<br/>                                                |



 

</dd> <dt>

*zfail* 
</dt> <dd>

Action du stencil lorsque le test du stencil réussit, mais le test de profondeur échoue. Accepte les mêmes constantes symboliques que *Fail.*

</dd> <dt>

*zpass* 
</dt> <dd>

Action de stencil lorsque le test de stencil et le test de profondeur réussissent, ou lorsque le test de stencil réussit et qu’il n’y a pas de mémoire tampon de profondeur ou de test de profondeur n’est pas activé. Accepte les mêmes constantes symboliques que *Fail*.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *Fail*, *zfail* ou *ZPass* a une valeur autre que les six valeurs constantes définies.<br/>                                      |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

Le stencil, tel que la mise en mémoire tampon *z*, permet d’activer et de désactiver le dessin par pixel. Vous dessinez dans les plans de stencil à l’aide de primitives de dessin OpenGL, puis vous affichez la géométrie et les images à l’aide des plans de gabarit pour masquer des parties de l’écran. Le stencil est généralement utilisé dans les algorithmes de rendu multipasses pour obtenir des effets spéciaux, tels que les décalques, le mode plan et le rendu de géométrie solide constructive.

Le test de stencil élimine conditionnellement un pixel en fonction du résultat d’une comparaison entre la valeur dans la mémoire tampon de stencil et une valeur de référence. Le test est activé avec des appels [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument de test de stencil de la comptabilité \_ \_ , et contrôlé avec [**glStencilFunc**](glstencilfunc.md).

La fonction **glStencilOp** accepte trois arguments qui indiquent ce qui se passe à la valeur du stencil stocké lorsque le stencil est activé. Si le test du stencil échoue, aucune modification n’est apportée aux mémoires tampons de couleur ou de profondeur du pixel et l' *échec* spécifie ce qui se passe au contenu de la mémoire tampon du stencil.

Les valeurs de mémoire tampon de stencil sont traitées comme des entiers non signés. En cas de incrémentation et de décrémentation, les valeurs sont ancrées à 0 et 2 *n* 1, où *n* est la valeur retournée par l’interrogation des bits du stencil du GL \_ \_ .

Les deux autres arguments de **glStencilOp** spécifient des actions de tampon de stencil qui réussissent (*ZPass*) ou échouent (*zfail*). (Voir [**glDepthFunc**](gldepthfunc.md).) Elles sont spécifiées à l’aide des six mêmes constantes symboliques que *Fail*. Notez que *zfail* est ignoré lorsqu’il n’y a pas de mémoire tampon de profondeur, ou lorsque la mémoire tampon de profondeur n’est pas activée. Dans ces cas, *Fail* et *ZPass* spécifient l’action du stencil lorsque le test du stencil échoue et passe, respectivement.

Initialement, le test stencil est désactivé. S’il n’existe pas de mémoire tampon de stencil, aucune modification de stencil ne peut se produire et c’est comme si les tests de stencil réussissent toujours, quel que soit l’appel à **glStencilOp**.

Les fonctions suivantes récupèrent les informations relatives à **glStencilOp**:

échec de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument du stencil du GL \_ \_

**glGet** avec argument de la passe de \_ \_ profondeur passe-passe de stencil \_ \_

 échec de la \_ profondeur de \_ réussite du stencil \_ de glGet avec argument GL \_

**glGet** avec arguments de stencil de la comptabilité GL \_ \_

[**glIsEnabled**](glisenabled.md) avec l’argument \_ test de stencil du GL \_

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





