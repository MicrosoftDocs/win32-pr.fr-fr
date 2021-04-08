---
title: fonction glClearColor (GL. h)
description: La fonction glClearColor spécifie des valeurs claires pour les mémoires tampons de couleur.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- glClearColor fonction OpenGL
topic_type:
- apiref
api_name:
- glClearColor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34005ce34900f5fee8a4c9b2f1b963b7fe4bb6d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741940"
---
# <a name="glclearcolor-function"></a>glClearColor fonction)

La fonction **glClearColor** spécifie des valeurs claires pour les mémoires tampons de couleur.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glClearColor(
   GLclampf red,
   GLclampf green,
   GLclampf blue,
   GLclampf alpha
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rouge* 
</dt> <dd>

Valeur rouge utilisée par [**glClear**](glclear.md) pour effacer les mémoires tampons de couleurs. La valeur par défaut est zéro.

</dd> <dt>

*écologie* 
</dt> <dd>

Valeur verte utilisée par [**glClear**](glclear.md) pour effacer les mémoires tampons de couleurs. La valeur par défaut est zéro.

</dd> <dt>

*bleu* 
</dt> <dd>

Valeur bleue utilisée par [**glClear**](glclear.md) pour effacer les mémoires tampons de couleurs. La valeur par défaut est zéro.

</dd> <dt>

*alpha* 
</dt> <dd>

Valeur alpha utilisée par [**glClear**](glclear.md) pour effacer les mémoires tampons de couleurs. La valeur par défaut est zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glClearColor** spécifie les valeurs rouge, vert, bleu et alpha utilisées par [**glClear**](glclear.md) pour effacer les mémoires tampons de couleur. Les valeurs spécifiées par **glClearColor** sont ancrées à la plage \[ 0, 1 \] .

Les fonctions suivantes récupèrent les informations relatives à la fonction **glClearColor** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Amort \_ Clear \_ value

**glGet** avec argument \_ \_ valeur Clear de couleur GL \_

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

 

 





