---
title: fonction glIndexfv (GL. h)
description: La fonction glIndexfv définit l’index de couleur actuel.
ms.assetid: 355d1896-ea9d-4a80-9dee-285f3bf638e5
keywords:
- glIndexfv fonction OpenGL
topic_type:
- apiref
api_name:
- glIndexfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a649f15dd6fad637d9e742a97235fdcd99d82794
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032594"
---
# <a name="glindexfv-function"></a>glIndexfv fonction)

La fonction **glIndexfv** définit l’index de couleur actuel.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glIndexfv(
   const GLfloat *c
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*c* 
</dt> <dd>

Pointeur vers un tableau d’un élément qui contient la nouvelle valeur pour l’index de couleur actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **glIndexfv** met à jour l’index de couleurs actuel (à valeur unique). Il accepte un argument : la nouvelle valeur pour l’index de couleur actuel.

L’index actuel est stocké sous la forme d’une valeur à virgule flottante. Les valeurs entières sont converties directement en valeurs à virgule flottante, sans mappage spécial.

Les valeurs d’index situées en dehors de la plage représentable de la mémoire tampon d’index de couleurs ne sont pas ancrées. Toutefois, avant qu’un index ne soit déformé (s’il est activé) et écrit dans le trame, il est converti au format à virgule fixe. Tous les bits de la partie entière de la valeur à virgule fixe résultante qui ne correspondent pas aux bits dans le trame sont masqués.

L’index actuel peut être mis à jour à tout moment. En particulier, **glIndexfv** peut être appelé entre un appel à [**glBegin**](/windows/desktop/OpenGL/glbegin) et l’appel correspondant à [**glEnd**](glend.md).

La fonction suivante récupère des informations relatives à **glIndexfv**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ index

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

