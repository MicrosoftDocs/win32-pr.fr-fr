---
title: fonction glDrawBuffer (GL. h)
description: La fonction glDrawBuffer spécifie les mémoires tampons de couleur à dessiner.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- glDrawBuffer fonction OpenGL
topic_type:
- apiref
api_name:
- glDrawBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a99bd2b184766f1621d89b2c8d642902d300e14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510947"
---
# <a name="gldrawbuffer-function"></a>glDrawBuffer fonction)

La fonction **glDrawBuffer** spécifie les mémoires tampons de couleur à dessiner.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glDrawBuffer(
   GLenum mode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mode* 
</dt> <dd>

Spécifie jusqu’à quatre mémoires tampons de couleur à dessiner avec les constantes symboliques acceptées suivantes.



| Valeur                                                                                                                                                                       | Signification                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <dt>**GL \_ aucun**</dt> </dl>                                 | Aucune mémoire tampon de couleur n’est écrite.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <dt>**GL \_ avant \_ gauche**</dt> </dl>              | Seule la mémoire tampon de couleur frontale est écrite.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <dt>**GL \_ avant \_ droit**</dt> </dl>           | Seule la mémoire tampon de couleur frontale est écrite.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <dt>**en \_ arrière-plan du GL \_**</dt> </dl>                 | Seule la mémoire tampon de couleur de l’arrière-plan est écrite.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <dt>**\_arrière-plan du GL \_**</dt> </dl>              | Seule la mémoire tampon de couleur de l’arrière-plan est écrite.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <dt>**GL \_ frontal**</dt> </dl>                              | Seules les mémoires tampons de couleur frontale et gauche sont écrites. S’il n’existe pas de mémoire tampon de couleur frontale, seule la mémoire tampon de couleur d’avant-plan est écrite.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <dt>**Back. du GL \_**</dt> </dl>                                 | Seules les mémoires tampons de couleur de l’arrière-plan et de l’arrière-plan sont écrites. S’il n’existe aucune mémoire tampon de couleur d’arrière-plan, seule la mémoire tampon de couleur d’arrière-plan est écrite.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <dt>**GL \_ gauche**</dt> </dl>                                 | Seules les mémoires tampons de couleur d’arrière-plan et de gauche sont écrites. S’il n’y a pas de mémoire tampon de couleur de l’arrière-plan, seule la mémoire tampon de couleur de l’avant-gauche est écrite.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <dt>**\_droit GL**</dt> </dl>                              | Seules les mémoires tampons de couleur d’avant et de droite sont écrites. S’il n’y a pas de mémoire tampon de couleur de l’arrière-plan, seule la mémoire tampon de couleur de l’avant-droite est écrite.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <dt>**\_recto \_ et \_ Back GL**</dt> </dl> | Toutes les mémoires tampons de couleur de premier plan et d’arrière-plan (avant gauche, avant droit, arrière-plan de gauche, arrière-plan) sont écrites. S’il n’existe aucune mémoire tampon de couleur d’arrière-plan, seuls les tampons de couleur avant gauche et avant droit sont écrits. S’il n’y a pas de mémoire tampon de couleur droite, seules les mémoires tampons de couleur d’arrière-plan et de gauche sont écrites. S’il n’existe pas de mémoire tampon de couleur de droite ou d’arrière-plan, seule la mémoire tampon de couleur frontale est écrite.<br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <dt>**\_Auxi GL**</dt> </dl>       | Seule la mémoire tampon de couleur auxiliaire *i* est écrite ; *i* est compris entre 0 et \_ \_ le GL des tampons au-1. (GL \_ \_Les mémoires tampons aux ne sont pas la limite supérieure ; utilisez [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) pour interroger le nombre de tampons auxiliaires disponibles.)<br/>                                                                                                                            |



 

La valeur par défaut est \_ recto GL pour les contextes à une seule mise en mémoire tampon, et le GL est \_ de retour pour les contextes de double mise en mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *mode* n’était pas une valeur acceptée.<br/>                                                                                          |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | Aucune des mémoires tampons indiquées par le *mode* n’existait.<br/>                                                                           |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |


## <a name="remarks"></a>Notes

Lorsque les couleurs sont écrites dans le trame, elles sont écrites dans les tampons de couleurs spécifiés par **glDrawBuffer**.

Si plus d’une mémoire tampon de couleur est sélectionnée pour le dessin, les opérations de fusion ou logique sont calculées et appliquées indépendamment pour chaque mémoire tampon de couleur et peuvent produire des résultats différents dans chaque mémoire tampon.

Les contextes Monoscopic incluent uniquement les mémoires tampons de gauche, tandis que les contextes stéréoscopiques incluent les mémoires tampons de gauche et de droite. De même, les contextes à une seule mémoire tampon incluent uniquement les mémoires tampons d’arrière-plan, et les contextes de double mise en mémoire tampon incluent les mémoires tampons d’arrière-plan et d’arrière-plan. Le contexte est sélectionné lors de l’initialisation OpenGL.

C’est toujours le cas pour GL \_ des *i* = GL \_ AUX0 + *i*.

Les fonctions suivantes récupèrent les informations relatives à la fonction **glDrawBuffer** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument \_ mémoire tampon de dessin de la comptabilité \_

**glGet** avec argument GL \_ aux \_ tampons

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

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> </dl>

 

 





