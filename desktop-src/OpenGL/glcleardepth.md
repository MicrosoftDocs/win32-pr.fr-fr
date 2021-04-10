---
title: fonction glClearDepth (GL. h)
description: La fonction glClearDepth spécifie la valeur Clear pour la mémoire tampon de profondeur.
ms.assetid: 8e26ae78-edc1-4201-a0db-d5bc8ae6dc82
keywords:
- glClearDepth fonction OpenGL
topic_type:
- apiref
api_name:
- glClearDepth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf968c7ae172bf4ce354c84b2071d62304327ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317289"
---
# <a name="glcleardepth-function"></a>glClearDepth fonction)

La fonction **glClearDepth** spécifie la valeur Clear pour la mémoire tampon de profondeur.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glClearDepth(
   GLclampd depth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*profondeur* 
</dt> <dd>

Valeur de profondeur utilisée lorsque la mémoire tampon de profondeur est effacée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glClearDepth** spécifie la valeur de profondeur utilisée par [**glClear**](glclear.md) pour effacer la mémoire tampon de profondeur. Les valeurs spécifiées par **glClearDepth** sont ancrées à la plage \[ 0, 1 \] .

La fonction suivante récupère les informations relatives à la fonction **glClearDepth** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ profondeur \_ effacer la \_ valeur

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

 

 





