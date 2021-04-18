---
title: fonction glIndexMask (GL. h)
description: La fonction glIndexMask contrôle l’écriture de bits individuels dans les mémoires tampons d’index de couleurs.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- glIndexMask fonction OpenGL
topic_type:
- apiref
api_name:
- glIndexMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d426cb1f4bb2e794bef53853d0336db1d64b263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509302"
---
# <a name="glindexmask-function"></a>glIndexMask fonction)

La fonction **glIndexMask** contrôle l’écriture de bits individuels dans les mémoires tampons d’index de couleurs.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mask* 
</dt> <dd>

Masque de bits permettant d’activer et de désactiver l’écriture de bits individuels dans les mémoires tampons d’index de couleurs. Initialement, le masque est tous les éléments.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glIndexMask** contrôle l’écriture de bits individuels dans les mémoires tampons d’index de couleurs. Les *n* bits les moins significatifs du *masque*, où *1* est le nombre de bits dans une mémoire tampon d’index de couleurs, spécifiez un masque. Chaque fois qu’un point apparaît dans le masque, le bit correspondant dans la mémoire tampon d’index de couleurs (ou mémoires tampons) est rendu accessible en écriture. Lorsqu’un zéro s’affiche, le bit est protégé en écriture.

Ce masque est utilisé uniquement en mode d’index de couleurs, et il affecte uniquement les mémoires tampons actuellement sélectionnées pour l’écriture (voir [**glDrawBuffer**](gldrawbuffer.md)). Initialement, tous les bits sont activés pour l’écriture.

La fonction suivante récupère des informations relatives à **glIndexMask**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ index \_ WRITEMASK

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

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





