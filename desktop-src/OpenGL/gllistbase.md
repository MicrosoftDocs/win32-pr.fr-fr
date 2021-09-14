---
title: fonction glListBase (GL. h)
description: La fonction glListBase définit la base de la liste d’affichage pour glCallLists.
ms.assetid: df82f699-b2af-471a-83f3-5620857ba45d
keywords:
- glListBase fonction OpenGL
topic_type:
- apiref
api_name:
- glListBase
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46af03477afc1b656df3a321fd8aa652b034b35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222612"
---
# <a name="gllistbase-function"></a>glListBase fonction)

La fonction **glListBase** définit la base de la liste d’affichage pour **glCallLists**.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glListBase(
   GLuint base
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*base* 
</dt> <dd>

Offset d’entier qui sera ajouté aux décalages [**glCallLists**](glcalllists.md) pour générer des noms de liste d’affichage. La valeur initiale est égale à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glListBase** spécifie un tableau d’offsets. Les noms d’affichage de liste sont générés par l’ajout de *base* à chaque décalage. Les noms qui référencent des listes d’affichage valides sont exécutés ; d’autres sont ignorées.

La fonction suivante récupère des informations relatives à **glListBase**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ List \_ base

## <a name="requirements"></a>Spécifications



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

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





