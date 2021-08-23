---
title: fonction glInitNames (GL. h)
description: La fonction glInitNames initialise la pile de noms.
ms.assetid: 26c134f5-c17c-4637-93b6-5293f316dd6c
keywords:
- glInitNames fonction OpenGL
topic_type:
- apiref
api_name:
- glInitNames
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a567242431fc90be3b60d8ae08875b585ff6a81794899a6c9eb69e7a0a03daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012117"
---
# <a name="glinitnames-function"></a>glInitNames fonction)

La fonction **glInitNames** initialise la pile de noms.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glInitNames(void);
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



## <a name="remarks"></a>Remarques

La fonction **glInitNames** provoque l’initialisation de la pile de noms à son état vide par défaut. La pile de noms est utilisée en mode de sélection pour permettre l’identification unique des jeux de commandes de rendu. Il se compose d’un ensemble ordonné d’entiers non signés.

La pile de noms est toujours vide lorsque le mode de rendu n’est pas la sélection de la comptabilité \_ . Les appels à **glInitNames** alors que le mode de rendu n’est pas GL \_ Select sont ignorés.

Les fonctions suivantes récupèrent les informations relatives à **glInitNames**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de la profondeur de la \_ pile nom GL \_ \_

**glGet** avec argument GL \_ Max \_ nom \_ \_ profondeur de la pile

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

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





