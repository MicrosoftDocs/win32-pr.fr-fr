---
title: fonction glDeleteLists (GL. h)
description: La fonction glDeleteLists supprime un groupe contigu de listes d’affichage.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- glDeleteLists fonction OpenGL
topic_type:
- apiref
api_name:
- glDeleteLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311797"
---
# <a name="gldeletelists-function"></a>glDeleteLists fonction)

La fonction **glDeleteLists** supprime un groupe contigu de listes d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glDeleteLists(
   GLuint  list,
   GLsizei range
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*list* 
</dt> <dd>

Nom entier de la première liste d’affichage à supprimer.

</dd> <dt>

*range* 
</dt> <dd>

Nombre de listes d’affichage à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *plage* était négative.<br/>                                                                                                      |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glDeleteLists** provoque la suppression d’un groupe contigu de listes d’affichage. Le paramètre *List* est le nom de la première liste d’affichage à supprimer, et *Range* est le nombre de listes d’affichage à supprimer. Toutes *les listes d'* affichage *de la* plage de liste d liste  =  *d*  =    +   -1 sont supprimées.

Tous les emplacements de stockage alloués aux listes d’affichage spécifiées sont libérés, et les noms sont disponibles pour être réutilisés ultérieurement. Les noms dans la plage qui n’ont pas de liste d’affichage associée sont ignorés. Si la *plage* est égale à zéro, rien ne se produit.

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





