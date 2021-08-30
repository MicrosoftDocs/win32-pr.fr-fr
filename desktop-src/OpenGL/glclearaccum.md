---
title: fonction glClearAccum (GL. h)
description: La fonction glClearAccum spécifie les valeurs claires pour la mémoire tampon d’accumulation.
ms.assetid: 77d8f340-be47-43f4-96fc-31025a4c8b4e
keywords:
- glClearAccum fonction OpenGL
topic_type:
- apiref
api_name:
- glClearAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e4e5b02b52ac72e5694b1c5f912dd8dd98fb8dda5b623b28addd20fccbb7dd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082069"
---
# <a name="glclearaccum-function"></a>glClearAccum fonction)

La fonction **glClearAccum** spécifie les valeurs claires pour la mémoire tampon d’accumulation.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glClearAccum(
   GLfloat red,
   GLfloat green,
   GLfloat blue,
   GLfloat alpha
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rouge* 
</dt> <dd>

Valeur rouge utilisée lorsque la mémoire tampon d’accumulation est effacée. La valeur par défaut est zéro.

</dd> <dt>

*écologie* 
</dt> <dd>

Valeur verte utilisée lorsque la mémoire tampon d’accumulation est effacée. La valeur par défaut est zéro.

</dd> <dt>

*bleu* 
</dt> <dd>

Valeur bleue utilisée lorsque la mémoire tampon d’accumulation est effacée. La valeur par défaut est zéro.

</dd> <dt>

*alpha* 
</dt> <dd>

Valeur alpha utilisée lorsque la mémoire tampon d’accumulation est effacée. La valeur par défaut est zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glClearAccum** spécifie les valeurs rouge, vert, bleu et alpha utilisées par [**glClear**](glclear.md) pour effacer la mémoire tampon d’accumulation.

Les valeurs spécifiées par **glClearAccum** sont ancrées à la plage \[ 1, 1 \] .

La fonction suivante récupère des informations relatives à **glClearAccum**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Amort \_ Clear \_ value

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

[**glClear**](glclear.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





