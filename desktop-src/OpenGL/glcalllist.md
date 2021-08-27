---
title: fonction glCallList (GL. h)
description: La fonction glCallList exécute une liste d’affichage.
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- glCallList fonction OpenGL
topic_type:
- apiref
api_name:
- glCallList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67805ff50eb4566e8a2a186c10229f944f4003baaef1274e9d4f52dd3b9c2a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082119"
---
# <a name="glcalllist-function"></a>glCallList fonction)

La fonction **glCallList** exécute une liste d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glCallList(
   GLuint list
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*list* 
</dt> <dd>

Nom entier de la liste d’affichage à exécuter.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

L’appel de la fonction **glCallList** commence l’exécution de la liste d’affichage nommée. Les fonctions enregistrées dans la liste d’affichage sont exécutées dans l’ordre, de la même façon que si vous les avez appelées sans utiliser de liste d’affichage. Si la *liste* n’a pas été définie en tant que liste d’affichage, **glCallList** est ignoré.

La fonction **glCallList** peut apparaître à l’intérieur d’une liste d’affichage. Pour éviter la possibilité d’une récurrence infinie résultant de l’appel d’une liste d’affichage, une limite est placée sur le niveau d’imbrication des listes d’affichage au cours de l’exécution de la liste d’affichage. Toutefois, cette limite est d’au moins 64. elle dépend de l’implémentation.

L’État OpenGL n’est pas enregistré et restauré à travers un appel à **glCallList**. Ainsi, les modifications apportées à l’État OpenGL pendant l’exécution d’une liste d’affichage sont conservées après la fin de l’exécution de la liste d’affichage. Pour conserver l’État OpenGL sur les appels **glCallList** , utilisez [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)et [**glPopMatrix**](glpopmatrix.md).

Vous pouvez exécuter des listes d’affichage entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md), à condition que la liste d’affichage comprenne uniquement les fonctions autorisées dans cet intervalle.

Les fonctions suivantes récupèrent les informations relatives à **glCallList**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL \_ Max \_ List \_ imbrication

[**glIsList**](glislist.md)

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

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





