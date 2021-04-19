---
title: fonction glPushName (GL. h)
description: Les fonctions glPushName et glPopName poussent et dépilent la pile de noms. | fonction glPushName (GL. h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- glPushName fonction OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff783a108f5cb1ac34141c6c57f47b16e23531a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106545239"
---
# <a name="glpushname-function"></a>glPushName fonction)

Les fonctions **glPushName** et [**glPopName**](glpopname.md) poussent et dépilent la pile de noms.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*name* 
</dt> <dd>

Nom qui fera l’objet d’un push dans la pile de noms.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**dépassement de capacité de la \_ pile GL \_**</dt> </dl>    | La fonction a été appelée alors que la pile de matrices actuelle était pleine.<br/>                                                           |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glPushName** provoque un push du nom dans la pile de noms, qui est initialement vide. La fonction [**glPopName**](glpopname.md) Dépile un nom en haut de la pile. La pile de noms est utilisée en mode de sélection pour permettre l’identification unique des jeux de commandes de rendu. Il se compose d’un ensemble ordonné d’entiers non signés.

La pile de noms est toujours vide lorsque le mode de rendu n’est pas la sélection de la comptabilité \_ . Les appels à **glPushName** ou [**glPopName**](glpopname.md) alors que le mode de rendu n’est pas GL \_ Select sont ignorés.

Les fonctions suivantes récupèrent les informations relatives à **glPushName** et [**glPopName**](glpopname.md):

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de la profondeur de la \_ pile nom GL \_ \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Max \_ nom \_ \_ profondeur de la pile

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

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





