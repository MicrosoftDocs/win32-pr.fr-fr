---
title: fonction glFinish (GL. h)
description: La fonction glFinish se bloque jusqu’à ce que toute l’exécution de OpenGL soit terminée.
ms.assetid: 1dcb4767-02ea-41d8-bf1f-d61d20873d4f
keywords:
- glFinish fonction OpenGL
topic_type:
- apiref
api_name:
- glFinish
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99d4cb185beb09cb882667b80dbd06a25546fb9209da38a775cefa887443617
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580173"
---
# <a name="glfinish-function"></a>glFinish fonction)

La fonction **glFinish** se bloque jusqu’à ce que toute l’exécution de OpenGL soit terminée.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glFinish(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glFinish** ne retourne pas de résultat tant que les effets de toutes les fonctions OpenGL appelées précédemment ne sont pas terminés. Ces effets incluent toutes les modifications apportées à l’État OpenGL, toutes les modifications apportées à l’état de la connexion et toutes les modifications apportées au contenu de trame.

La fonction **glFinish** nécessite un aller-retour au serveur.

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

[**glFlush**](glflush.md)
</dt> </dl>

 

 





