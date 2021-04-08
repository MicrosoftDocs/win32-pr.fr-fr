---
title: fonction glFlush (GL. h)
description: La fonction glFlush force l’exécution des fonctions OpenGL en temps fini.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- glFlush fonction OpenGL
topic_type:
- apiref
api_name:
- glFlush
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8366fd5c42f68c495d544c20c3382b4e9fd37665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743876"
---
# <a name="glflush-function"></a>glFlush fonction)

La fonction **glFlush** force l’exécution des fonctions OpenGL en temps fini.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glFlush(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

Les différentes implémentations OpenGL entamponnt des commandes dans différents emplacements, y compris les tampons réseau et l’accélérateur graphique lui-même. La fonction **glFlush** vide toutes ces mémoires tampons, ce qui entraîne l’exécution de toutes les commandes émises aussi rapidement qu’elles sont acceptées par le moteur de rendu réel. Bien que cette exécution ne puisse pas être effectuée dans un laps de temps donné, elle se termine dans un laps de temps limité.

Étant donné que tous les programmes OpenGL peuvent être exécutés sur un réseau, ou sur un accélérateur qui met en mémoire tampon des commandes, veillez à appeler **glFlush** dans tous les programmes nécessitant que toutes les commandes précédemment émises soient terminées. Par exemple, appelez **glFlush** avant d’attendre une entrée utilisateur qui dépend de l’image générée.

La fonction **glFlush** peut retourner à tout moment. Il n’attend pas que l’exécution de toutes les fonctions OpenGL précédemment émises soit terminée.

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

[**glFinish**](glfinish.md)
</dt> </dl>

 

 





