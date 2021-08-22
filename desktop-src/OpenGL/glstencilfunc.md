---
title: fonction glStencilFunc (GL. h)
description: La fonction glStencilFunc définit la fonction et la valeur de référence pour le test des stencils.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- glStencilFunc fonction OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e529bd83cff8ffb25c8853b7d896926e63982370387f7e2fb5d2ca30a394c1cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491509"
---
# <a name="glstencilfunc-function"></a>glStencilFunc fonction)

La fonction **glStencilFunc** définit la fonction et la valeur de référence pour le test des stencils.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*func* 
</dt> <dd>

Fonction de test. Les huit jetons suivants sont valides.



| Valeur                                                                                                                                                   | Signification                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ jamais**</dt> </dl>          | Échoue toujours.<br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ moins**</dt> </dl>             | Passe si (  &  *masque* de référence) < (masque de *stencil*  &  ).<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**\_LEQUAL GL**</dt> </dl>       | Passe si (  &  *masque* de référence) = (masque de *stencil*  &  ).<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ supérieur**</dt> </dl>    | Passe si (  &  *masque* de référence) > (masque de *stencil*  &  ).<br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**\_GEQUAL GL**</dt> </dl>       | Passe si (  &  *masque* de référence) = (masque de *stencil*  &  ).<br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ égal**</dt> </dl>          | Passe si (  &  *masque* de référence) = (masque de *stencil*  &  ).<br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**\_NOTEQUAL GL**</dt> </dl> | Passe si (  &  *masque* de référence) ? (*gabarit*  &  *masque*).<br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**\_toujours GL**</dt> </dl>       | Passe toujours.<br/>                                        |



 

</dd> <dt>

*ref* 
</dt> <dd>

Valeur de référence pour le test de stencil. Le paramètre *ref* est ancré à la plage \[ 0, 2 *n* 1 \] , où *n* est le nombre de bitplanes dans la mémoire tampon du stencil.

</dd> <dt>

*mask* 
</dt> <dd>

Masque qui est **et** Ed avec la valeur de référence et la valeur de stencil stockée lorsque le test est terminé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *Func* ne faisait pas partie des huit valeurs acceptées.<br/>                                                                           |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

Le stencil, tel que la mise en mémoire tampon *z*, permet d’activer et de désactiver le dessin par pixel. Vous dessinez dans les plans de stencil à l’aide de primitives de dessin OpenGL, puis vous affichez la géométrie et les images à l’aide des plans de gabarit pour masquer des parties de l’écran. Le stencil est généralement utilisé dans les algorithmes de rendu multipasses pour obtenir des effets spéciaux, tels que les décalques, le mode plan et le rendu de géométrie solide constructive.

Le test de stencil élimine conditionnellement un pixel en fonction du résultat d’une comparaison entre la valeur de référence et la valeur dans la mémoire tampon de stencil. Le test est activé par [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument de test de stencil du GL \_ \_ . Les actions effectuées en fonction du résultat du test de stencil sont spécifiées avec [**glStencilOp**](glstencilop.md).

Le paramètre *Func* est une constante symbolique qui détermine la fonction de comparaison de stencil. Il accepte l’une des huit valeurs indiquées ci-dessus. Le paramètre *ref* est une valeur de référence entière qui est utilisée dans la comparaison de stencil. Elle est ancrée dans la plage \[ 0, 2 *n* 1 \] , où *n* est le nombre de bitplanes dans la mémoire tampon du stencil. Le paramètre *Mask* est au niveau du bit **and** Ed avec la valeur de référence et la valeur de stencil stockée, avec les valeurs **et** Ed qui participent à la comparaison.

Si le *stencil* représente la valeur stockée dans l’emplacement de la mémoire tampon de stencil correspondante, la liste précédente montre l’effet de chaque fonction de comparaison qui peut être spécifiée par *Func*. Uniquement si la comparaison réussit est le pixel passé à l’étape suivante du processus de pixellisation (voir [**glStencilOp**](glstencilop.md)). Tous les tests considèrent les valeurs de *stencil* comme des entiers non signés dans la plage \[ 0, 2 *n* 1 \] , où *n* est le nombre de bitplanes dans la mémoire tampon de stencil.

Au départ, le test stencil est désactivé. S’il n’existe pas de mémoire tampon de stencil, aucune modification de stencil ne peut se produire et c’est comme si le test de stencil passe toujours.

Les fonctions suivantes récupèrent les informations relatives à **glStencilFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL de \_ stencil \_ Func

**glGet** avec argument valeur de stencil du gabarit de GL \_ \_ \_

**glGet** avec argument de \_ référence de stencil de GL \_

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

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





