---
title: fonction glClearIndex (GL. h)
description: La fonction glClearIndex spécifie la valeur Clear pour les mémoires tampons d’index de couleurs.
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- glClearIndex fonction OpenGL
topic_type:
- apiref
api_name:
- glClearIndex
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6ed297ba30749d20d846055122f3ab12f77f8625450626a58fd15928172a207
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082049"
---
# <a name="glclearindex-function"></a>glClearIndex fonction)

La fonction **glClearIndex** spécifie la valeur Clear pour les mémoires tampons d’index de couleurs.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glClearIndex(
   GLfloat c
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*c* 
</dt> <dd>

Index utilisé lorsque les mémoires tampons d’index de couleurs sont effacées. La valeur par défaut est zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glClearIndex** spécifie l’index utilisé par [**glClear**](glclear.md) pour effacer les mémoires tampons d’index de couleurs. Le paramètre *c* n’est pas ancré. Au lieu de cela, *c* est converti en une valeur à virgule fixe avec une précision non spécifiée à droite du point binaire. La partie entière de cette valeur est ensuite masquée par 2 <sup>m</sup>  -1, où *m* est le nombre de bits dans un index de couleur stocké dans le trame.

Les fonctions suivantes récupèrent les informations relatives à **glClearIndex**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument \_ \_ valeur Clear de l’index GL \_

**glGet** avec arguments GL \_ index \_ bits

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

 

 





