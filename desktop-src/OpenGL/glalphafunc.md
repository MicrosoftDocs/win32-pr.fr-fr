---
title: fonction glAlphaFunc (GL. h)
description: La fonction glAlphaFunc permet à votre application de définir la fonction de test alpha.
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- glAlphaFunc fonction OpenGL
topic_type:
- apiref
api_name:
- glAlphaFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf96cfe2be0224c9c2e2409fc68805b530ae1f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513609"
---
# <a name="glalphafunc-function"></a>glAlphaFunc fonction)

La fonction **glAlphaFunc** permet à votre application de définir la fonction de test alpha.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glAlphaFunc(
   GLenum   func,
   GLclampf ref
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*func* 
</dt> <dd>

Fonction de comparaison alpha. Voici les constantes symboliques acceptées et leurs significations.



| Valeur                                                                                                                                                   | Signification                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ jamais**</dt> </dl>          | Ne passe jamais.<br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ moins**</dt> </dl>             | Passe si la valeur alpha entrante est inférieure à la valeur de référence.<br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ égal**</dt> </dl>          | Passe si la valeur alpha entrante est égale à la valeur de référence.<br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**\_LEQUAL GL**</dt> </dl>       | Passe si la valeur alpha entrante est inférieure ou égale à la valeur de référence.<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ supérieur**</dt> </dl>    | Passe si la valeur alpha entrante est supérieure à la valeur de référence.<br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**\_NOTEQUAL GL**</dt> </dl> | Passe si la valeur alpha entrante n’est pas égale à la valeur de référence.<br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**\_GEQUAL GL**</dt> </dl>       | Passe si la valeur alpha entrante est supérieure ou égale à la valeur de référence.<br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**\_toujours GL**</dt> </dl>       | Passe toujours. Il s’agit de la valeur par défaut.<br/>                                                 |



 

</dd> <dt>

*ref* 
</dt> <dd>

Valeur de référence à laquelle les valeurs alpha entrantes sont comparées. Cette valeur est ancrée à la plage de 0 à 1, où 0 représente la valeur alpha la plus basse possible et 1 la valeur la plus élevée possible. La référence par défaut est 0.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *Func* n’est pas une valeur acceptée.<br/>                                                                                          |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

Le test alpha ignore les fragments en fonction du résultat d’une comparaison entre les valeurs alpha des fragments entrants et une valeur de référence constante. La fonction **glAlphaFunc** spécifie la référence et la fonction de comparaison. La comparaison est effectuée uniquement si le test alpha est activé. (Pour plus d’informations sur GL \_ \_Test alpha, consultez [**glEnable**](glenable.md).)

Les paramètres *Func* et *ref* spécifient les conditions dans lesquelles le pixel est dessiné. La valeur alpha entrante est comparée à *ref* à l’aide de la fonction spécifiée par *Func*. Si la comparaison réussit, le fragment entrant est dessiné, conditionnel sur les tests du stencil et de la mémoire tampon de profondeur suivants. Si la comparaison échoue, aucune modification n’est apportée au trame à cet emplacement de pixel.

La fonction **glAlphaFunc** fonctionne sur toutes les écritures de pixels, y compris celles résultant de la conversion d’analyse des points, des lignes, des polygones et des bitmaps, et des opérations de dessin et de copie de pixels. La fonction **glAlphaFunc** n’affecte pas les opérations d’effacement de l’écran.

Le test alpha est effectué uniquement en mode RVBA.

Les fonctions suivantes récupèrent les informations relatives à la fonction **glAlphaFunc** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument GL \_ alpha de \_ test \_ Func

**glGet** avec l’argument GL \_ alpha \_ test \_ Ref

[**glIsEnabled**](glisenabled.md) avec l’argument GL \_ alpha \_ test

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

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





