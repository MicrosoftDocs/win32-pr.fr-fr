---
title: fonction glPassThrough (GL. h)
description: La fonction glPassThrough place un marqueur dans la mémoire tampon de commentaires.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- glPassThrough fonction OpenGL
topic_type:
- apiref
api_name:
- glPassThrough
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1174dd933d46813a89c35b781d0408c3ac5476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741133"
---
# <a name="glpassthrough-function"></a>glPassThrough fonction)

La fonction **glPassThrough** place un marqueur dans la mémoire tampon de commentaires.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPassThrough(
   GLfloat token
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*token* 
</dt> <dd>

Valeur de marqueur à placer dans la mémoire tampon de commentaires. Elle est indiquée avec la valeur d’identification unique suivante.



| Valeur                                                                                                                                                                                   | Signification                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <dt>**\_jeton de transfert GL \_ \_**</dt> </dl> | L’ordre des commandes **glPassThrough** en ce qui concerne la spécification des primitives graphiques est conservé.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

Les commentaires sont un mode de rendu OpenGL sélectionné en appelant [**glRenderMode**](glrendermode.md) avec des commentaires sur le GL \_ . Lorsque OpenGL est en mode commentaires, aucun Pixel n’est généré par pixellisation. Au lieu de cela, les informations sur les primitives qui auraient été pixellisées sont renvoyées à l’application par OpenGL. Consultez [**glFeedbackBuffer**](glfeedbackbuffer.md) pour obtenir une description de la mémoire tampon de commentaires et les valeurs qu’elle contient.

La fonction **glPassThrough** insère un marqueur défini par l’utilisateur dans la mémoire tampon de commentaires lorsqu’il est exécuté en mode commentaires. Le paramètre de *jeton* est retourné comme s’il s’agissait d’une primitive.

La fonction **glPassThrough** est ignorée si OpenGL n’est pas en mode commentaires.

La fonction suivante récupère des informations relatives à **glPassThrough**:

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

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





