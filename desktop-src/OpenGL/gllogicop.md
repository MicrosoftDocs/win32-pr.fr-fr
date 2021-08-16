---
title: fonction glLogicOp (GL. h)
description: La fonction glLogicOp spécifie une opération de pixel logique pour le rendu de l’index des couleurs.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- glLogicOp fonction OpenGL
topic_type:
- apiref
api_name:
- glLogicOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427bd338e416843418fa7551d4e1632dccaf268426ca2a910e164aeae50663dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492669"
---
# <a name="gllogicop-function"></a>glLogicOp fonction)

La fonction **glLogicOp** spécifie une opération de pixel logique pour le rendu de l’index des couleurs.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*opcode* 
</dt> <dd>

Constante symbolique qui sélectionne une opération logique. Les symboles suivants sont acceptés où s est égal à la valeur du bit source et d correspond à la valeur du bit de destination.



| Valeur                                                                                                                                                                   | Signification              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <dt>**\_effacement GL**</dt> </dl>                          | 0<br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <dt>**\_ensemble GL**</dt> </dl>                                | 1<br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <dt>**\_copie GL**</dt> </dl>                             | s<br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <dt>**\_copie GL \_ inversée**</dt> </dl> | ! s<br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <dt>**GL \_ NOOP**</dt> </dl>                             | d<br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ inversée**</dt> </dl>                       | ! d<br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <dt>**GL \_ et**</dt> </dl>                                | s & d<br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <dt>**GL \_ NAND**</dt> </dl>                             | ! (s & d)<br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <dt>**GL \_ ou**</dt> </dl>                                   | s \| d<br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <dt>**GL \_ ou**</dt> </dl>                                | ! (s \| d)<br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <dt>**GL \_ Xor**</dt> </dl>                                | s ^ d<br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <dt>**GL \_ EQUIV**</dt> </dl>                          | ! (s ^ d)<br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <dt>**GL \_ et \_ inverse**</dt> </dl>       | s & ! d<br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <dt>**GL \_ et \_ inversé**</dt> </dl>    | ! s & d<br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <dt>**GL \_ ou \_ inverse**</dt> </dl>          | s \| ! d<br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <dt>**GL \_ ou \_ inversé**</dt> </dl>       | ! s \| d<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | l' *opcode* n’était pas une valeur acceptée.<br/>                                                                                        |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glLogicOp** spécifie une opération logique qui, lorsqu’elle est activée, est appliquée entre l’index de couleur entrant et l’index de couleur à l’emplacement correspondant dans le trame. L’opération logique est activée ou désactivée avec [**glEnable**](glenable.md) et **glDisable** à l’aide de la constante symbolique GL \_ Logic \_ op.

Le paramètre *opcode* est une constante symbolique choisie dans la liste ci-dessous. Dans l’explication des opérations logiques, *s* représente l’index de couleur entrant et *d* représente l’index dans le trame. Les opérateurs langage C standard sont utilisés. Comme ces opérateurs de bits suggèrent, l’opération logique est appliquée indépendamment à chaque paire de bits des index source et de destination.

Les opérations de pixels logiques ne sont pas appliquées aux tampons de couleurs RVBA.

Lorsque plusieurs mémoires tampons d’index de couleurs sont activées pour le dessin, les opérations logiques sont effectuées séparément pour chaque mémoire tampon activée, en utilisant le contenu de cette mémoire tampon pour l’index de destination (voir [**glDrawBuffer**](gldrawbuffer.md)).

Le paramètre *opcode* doit être l’une des 16 valeurs acceptées. Les autres valeurs génèrent une erreur.

Les fonctions suivantes récupèrent les informations relatives à **glLogicOp**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ logique \_ op \_ mode

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Logic \_ op

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

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





