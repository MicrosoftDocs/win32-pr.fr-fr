---
title: fonction glRenderMode (GL. h)
description: La fonction glRenderMode définit le mode de pixellisation.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- glRenderMode fonction OpenGL
topic_type:
- apiref
api_name:
- glRenderMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af07d2492d70f9c0a3a764d767b52b2f71204939
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106198"
---
# <a name="glrendermode-function"></a>glRenderMode fonction)

La fonction **glRenderMode** définit le mode de pixellisation.

## <a name="syntax"></a>Syntaxe


```C++
GLint WINAPI glRenderMode(
   GLenum mode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mode* 
</dt> <dd>

Mode de pixellisation. Les trois valeurs suivantes sont acceptées. La valeur par défaut est GL \_ Render.



| Valeur                                                                                                                                                   | Signification                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <dt>**\_rendu GL**</dt> </dl>       | Mode de rendu. Les primitives sont pixellisées, produisant des fragments de pixels, qui sont écrites dans le trame. Il s’agit du mode normal et du mode par défaut.<br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <dt>**sélection du GL \_**</dt> </dl>       | Mode de sélection. Aucun fragment de pixel n’est produit, et aucune modification du contenu du trame n’est effectuée. Au lieu de cela, un enregistrement des noms des primitives qui auraient été dessinées si le mode de rendu était le \_ rendu GL est retourné dans une mémoire tampon Select, qui doit être créée (voir [**glSelectBuffer**](glselectbuffer.md)) avant que le mode de sélection soit entré.<br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <dt>**Commentaires sur le GL \_**</dt> </dl> | Mode commentaires. Aucun fragment de pixel n’est produit, et aucune modification du contenu du trame n’est effectuée. Au lieu de cela, les coordonnées et les attributs des vertex qui auraient été dessinés avaient le mode de rendu « GL \_ Render » est retourné dans une mémoire tampon de commentaires, qui doit être créée (voir [**glFeedbackBuffer**](glfeedbackbuffer.md)) avant d’entrer en mode commentaires.<br/> |



 

</dd> </dl>

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *mode* ne faisait pas partie des trois valeurs acceptées.<br/>                                                                                     |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée avec l’argument GL \_ Select avant que [**glSelectBuffer**](glselectbuffer.md) ne soit appelé au moins une fois.<br/>       |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée avec l’argument \_ Feedback GL avant que [**glBeedbackBuffer**](glfeedbackbuffer.md) ne soit appelé au moins une fois.<br/> |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/>       |



## <a name="remarks"></a>Notes

La fonction **glRenderMode** prend un argument, *mode*, qui peut prendre l’une des trois valeurs prédéfinies ci-dessus.

La valeur de retour de la fonction **glRenderMode** est déterminée par le mode de rendu au moment où **glRenderMode** est appelé, plutôt que par *mode*. Les valeurs retournées pour les trois modes de rendu sont les suivantes.



| Valeur        | Signification                                                                 |
|--------------|-------------------------------------------------------------------------|
| \_rendu GL   | Zéro.                                                                   |
| sélection du GL \_   | Nombre d’enregistrements d’accès transférés à la mémoire tampon de sélection.             |
| Commentaires sur le GL \_ | Nombre de valeurs (pas de vertex) transférées vers la mémoire tampon de commentaires. |



 

Pour plus d’informations sur le fonctionnement de la sélection et des commentaires, consultez [**glSelectBuffer**](glselectbuffer.md) et [**glFeedbackBuffer**](glfeedbackbuffer.md) .

Si une erreur est générée, **glRenderMode** retourne zéro quel que soit le mode de rendu actuel.

La fonction suivante récupère des informations relatives à **glRenderMode**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Render \_ mode

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

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPassThrough**](glpassthrough.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





