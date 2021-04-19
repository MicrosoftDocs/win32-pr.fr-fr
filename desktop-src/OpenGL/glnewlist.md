---
title: fonction glNewList (GL. h)
description: Les fonctions glNewList et glEndList créent ou remplacent une liste d’affichage. | fonction glNewList (GL. h)
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- glNewList fonction OpenGL
topic_type:
- apiref
api_name:
- glNewList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6135f67c07f69d24df67d4f1899404359efaa7aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106520283"
---
# <a name="glnewlist-function"></a>glNewList fonction)

Les fonctions **glNewList** et [**glEndList**](glendlist.md) créent ou remplacent une liste d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glNewList(
   GLuint list,
   GLenum mode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*list* 
</dt> <dd>

Nom de la liste d’affichage.

</dd> <dt>

*mode* 
</dt> <dd>

Mode de compilation. Les valeurs suivantes sont acceptées.



| Valeur                                                                                                                                                                                      | Signification                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <dt>**compilation du GL \_**</dt> </dl>                                       | Les commandes sont simplement compilées.<br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <dt>**\_compilation \_ et \_ exécution du GL**</dt> </dl> | Les commandes sont exécutées lorsqu’elles sont compilées dans la liste d’affichage.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *liste* était égale à zéro.<br/>                                                                                                           |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *mode* n’était pas une valeur acceptée.<br/>                                                                                          |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

Les listes d’affichage sont des groupes de commandes OpenGL qui ont été stockées pour une exécution ultérieure. Les listes d’affichage sont créées avec **glNewList**. Toutes les commandes suivantes sont placées dans la liste d’affichage, dans l’ordre d’émission, jusqu’à ce que **glEndList** soit appelé.

La fonction **glNewList** a deux paramètres. Le premier paramètre, *List*, est un entier positif qui devient le nom unique de la liste d’affichage. Les noms peuvent être créés et réservés avec [**glGenLists**](glgenlists.md) et testés pour l’unicité avec [**glIsList**](glislist.md). Le deuxième paramètre, *mode*, est une constante symbolique qui peut prendre l’une des deux valeurs précédentes.

Certaines commandes ne sont pas compilées dans la liste d’affichage, mais sont exécutées immédiatement, quel que soit le mode de liste d’affichage. Ces commandes sont [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)et toutes les routines [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .

De même, [**glTexImage2D**](glteximage2d.md) et [**glTexImage1D**](glteximage1d.md) sont exécutés immédiatement et ne sont pas compilés dans la liste d’affichage lorsque leur premier argument est la texture du \_ proxy GL \_ \_ 2D ou la \_ texture du proxy GL \_ \_ 1D, respectivement.

Lorsque la fonction **glEndList** est rencontrée, la définition de la liste d’affichage est effectuée en associant la liste avec la *liste* de noms uniques (spécifiée dans la commande **glNewList** ). Si une liste d’affichage avec la *liste* de noms existe déjà, elle est remplacée uniquement lorsque **glEndList** est appelé.

Les fonctions [**glCallList**](glcalllist.md) et [**glCallLists**](glcalllists.md) peuvent être entrées dans des listes d’affichage. Les commandes de la liste d’affichage ou des listes exécutées par **glCallList** ou **glCallLists** ne sont pas incluses dans la liste d’affichage en cours de création, même si le mode de création de liste est la \_ compilation et l’exécution du GL \_ \_ .

La fonction suivante récupère des informations relatives à **glNewList**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEndList**](glendlist.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> </dl>

 

 





