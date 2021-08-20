---
title: fonction glPopName (GL. h)
description: Les fonctions glPushName et glPopName poussent et dépilent la pile de noms. | fonction glPopName (GL. h)
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
keywords:
- glPopName fonction OpenGL
topic_type:
- apiref
api_name:
- glPopName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe30aa09d401fc8ef35a3671e02a898776af26111ae0f8e31cd1f6ad3bff70b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290169"
---
# <a name="glpopname-function"></a>glPopName fonction)

Les fonctions [**glPushName**](glpushname.md) et **glPopName** poussent et dépilent la pile de noms.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPopName(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DÉPASSEMENT de capacité de la \_ pile GL \_**</dt> </dl>   | La fonction a été appelée alors que la pile de matrice actuelle ne contenait qu’une seule matrice.<br/>                                     |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction [**glPushName**](glpushname.md) provoque un push du nom dans la pile de noms, qui est initialement vide. La fonction **glPopName** Dépile un nom en haut de la pile. La pile de noms est utilisée en mode de sélection pour permettre l’identification unique des jeux de commandes de rendu. Il se compose d’un ensemble ordonné d’entiers non signés.

La pile de noms est toujours vide lorsque le mode de rendu n’est pas la sélection de la comptabilité \_ . Les appels à [**glPushName**](glpushname.md) ou **glPopName** alors que le mode de rendu n’est pas GL \_ Select sont ignorés.

Les fonctions suivantes récupèrent les informations relatives à [**glPushName**](glpushname.md) et **glPopName**:

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

 

 





