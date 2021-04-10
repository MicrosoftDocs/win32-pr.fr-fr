---
title: fonction glLoadName (GL. h)
description: La fonction glLoadName charge un nom dans la pile de noms.
ms.assetid: 8d7d582b-3743-401e-af71-28034e49f3c2
keywords:
- glLoadName fonction OpenGL
topic_type:
- apiref
api_name:
- glLoadName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb47a0389cda13523104ee429bca46838970e15a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106411"
---
# <a name="glloadname-function"></a>glLoadName fonction)

La fonction **glLoadName** charge un nom dans la pile de noms.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glLoadName(
   GLuint name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*name* 
</dt> <dd>

Nom qui remplacera la valeur supérieure de la pile de noms.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée alors que la pile de noms était vide.<br/>                                                                    |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glLoadName** fait en sorte que *Name* remplace la valeur en haut de la pile de noms, qui est initialement vide. La pile de noms est utilisée en mode de sélection pour permettre l’identification unique des jeux de commandes de rendu. Il se compose d’un ensemble ordonné d’entiers non signés.

La pile de noms est toujours vide lorsque le mode de rendu n’est pas la sélection de la comptabilité \_ . Les appels à **glLoadName** alors que le mode de rendu n’est pas GL \_ Select sont ignorés.

Les fonctions suivantes récupèrent les informations relatives à **glLoadName**:

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

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





