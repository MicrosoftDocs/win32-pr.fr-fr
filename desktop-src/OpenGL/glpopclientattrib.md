---
title: fonction glPopClientAttrib (GL. h)
description: Les fonctions glPushClientAttrib et glPopClientAttrib permettent d’enregistrer et de restaurer des groupes de variables d’état client sur la pile client-Attribute. | fonction glPopClientAttrib (GL. h)
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- glPopClientAttrib fonction OpenGL
topic_type:
- apiref
api_name:
- glPopClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9f09e9c7292754a736594a9bf3d57a70063744
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121330"
---
# <a name="glpopclientattrib-function"></a>glPopClientAttrib fonction)

Les fonctions [**glPushClientAttrib**](glpushclientattrib.md) et **glPopClientAttrib** permettent d’enregistrer et de restaurer des groupes de variables d’état client sur la pile client-Attribute.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                               | Signification                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**dépassement de capacité de la \_ pile GL \_**</dt> </dl> | La fonction a été appelée alors que la pile client-attribut était pleine.<br/> |



## <a name="remarks"></a>Notes

La fonction **glPushClientAttrib** utilise son paramètre mask pour déterminer les groupes de variables d’état client qui sont enregistrés sur la pile client-Attribute. Vous pouvez utiliser l’opérateur de bits or pour joindre des constantes symboliques acceptées afin de définir des bits et de construire un masque.

La fonction **glPopClientAttrib** restaure les valeurs des variables d’état client enregistrées avec **glPushclientAttrib**. Les variables d’état client qui n’ont pas encore été enregistrées restent inchangées. L’envoi d’attributs vers une pile d’attribut client complète ou la déduplication d’attributs d’une pile vide définit un indicateur d’erreur et aucune autre modification n’est apportée à l’État OpenGL. Par défaut, la pile des attributs du client est vide.

Certaines valeurs d’état client OpenGL ne peuvent pas être enregistrées sur la pile client-Attribute. Par exemple, vous ne pouvez pas enregistrer les États Select ou feedback sur la pile client-Attribute. La profondeur de la pile client-attribute est d’au moins 16.

Les fonctions **glPushclientAttrib** et **glPopClientAttrib** ne sont pas compilées dans des listes d’affichage, mais sont exécutées immédiatement.

Les fonctions **glPushClientAttrib** et **glPopClientAttrib** peuvent uniquement envoyer et dépiler les modes de stockage de pixels et les États du client de tableau de vertex. Vous devez utiliser [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md) pour les États push et pop qui sont conservés sur le serveur.

> [!Note]  
> Les fonctions **glPushClientAttrib** et **glPopClientAttrib** sont uniquement disponibles dans OpenGL version 1,1 ou ultérieure.

 

Les fonctions suivantes récupèrent les informations relatives à **glPushClientAttrib** et **glPopClientAttrib**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de la profondeur de la pile de l' \_ attribut GL client \_ \_ \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Max. profondeur de la pile des \_ attributs du client \_ \_ \_

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDisableClientState**](gldisableclientstate.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





