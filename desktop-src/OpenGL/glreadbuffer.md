---
title: fonction glReadBuffer (GL. h)
description: La fonction glReadBuffer sélectionne une source de mémoire tampon de couleur pour les pixels.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- glReadBuffer fonction OpenGL
topic_type:
- apiref
api_name:
- glReadBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e88cdcb2b1b3257b23606f8160e0986584db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512597"
---
# <a name="glreadbuffer-function"></a>glReadBuffer fonction)

La fonction **glReadBuffer** sélectionne une source de mémoire tampon de couleur pour les pixels.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glReadBuffer(
   GLenum mode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mode* 
</dt> <dd>

Mémoire tampon de couleur. Les valeurs acceptées sont le préversion GL, le préversion GL, l’arrière-plan du GL, l’arrière-plan du GL, le \_ \_ \_ \_ \_ \_ \_ \_ \_ rectus GL, le \_ verso, le GL à \_ gauche, \_ le GL droit et le GL des, \_ où *i* est compris entre 0 et le GL des tampons au niveau  \_ \_ 1.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *mode* ne faisait pas partie des douze (ou plus) valeurs acceptées.<br/>                                                             |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | le *mode* a spécifié une mémoire tampon qui n’existe pas.<br/>                                                                             |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glReadBuffer** spécifie une mémoire tampon de couleur comme source pour les commandes [**glReadPixels**](glreadpixels.md) et [**glCopyPixels**](glcopypixels.md) suivantes. Le paramètre *mode* accepte une ou plusieurs valeurs prédéfinies. (GL \_ AUX0 via GL \_ AUX3 sont toujours définis.) Dans un système entièrement configuré, les préversions GL \_ , GL gauche et GL vers l’avant-plan de la zone de préversion de la mémoire tampon de l’avant-plan, le préversion \_ \_ \_ GL \_ \_ et \_ \_ \_ \_ le nom de la mémoire tampon d’arrière-plan.

Les configurations à double mise en mémoire tampon non stéréo n’ont qu’une seule partie de l’avant-gauche et une mémoire tampon en arrière-plan. Les configurations à une seule mise en mémoire tampon ont un avant-plan et une mémoire tampon de l’avant-plan si elle est stéréo, et seulement une mémoire tampon en avant-gauche si elle est non stéréo. La spécification d’une mémoire tampon inexistante dans **glReadBuffer** est une erreur.

Par défaut, le *mode* est \_ recto GL dans les configurations à une seule mise en mémoire tampon, et le GL \_ revient dans les configurations à double mémoire tampon.

La fonction suivante récupère des informations relatives à **glReadBuffer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL de lecture de la \_ \_ mémoire tampon

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> </dl>

 

 





