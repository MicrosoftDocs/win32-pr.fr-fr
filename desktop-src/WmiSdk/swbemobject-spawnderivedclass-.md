---
description: Utilisez la \_ méthode SpawnDerivedClass de l’objet SWbemObject pour créer un objet de classe dérivée à partir de l’objet actuel. L’objet doit être une définition de classe qui devient la classe parente de l’objet généré.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: Méthode SWbemObject.SpawnDerivedClass_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0ed0a01926c76ecfc4d393a4de8225d7d0c98a9904f113aed18cd1cb5f8ccabb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313793"
---
# <a name="swbemobjectspawnderivedclass_-method"></a>SWbemObject. SpawnDerivedClass, \_ méthode

Utilisez la **méthode \_ SpawnDerivedClass** de l’objet [**SWbemObject**](swbemobject.md) pour créer un objet de classe dérivée à partir de l’objet actuel. L’objet doit être une définition de classe qui devient la classe parente de l’objet généré.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IFlags* \[ facultatif\]
</dt> <dd>

Réservé et doit avoir la valeur 0 (zéro) si elle est spécifiée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’appel réussit, l’objet [**SWbemObject**](swbemobject.md) contient le nouvel objet de définition de classe. Aucun objet n’est retourné en cas d’erreur.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la **méthode \_ SpawnDerivedClass** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrIllegalOperation** -2147749918 (0x8004101E)
</dt> <dd>

L’utilisateur a demandé une opération non conforme, telle que la génération d’une classe à partir d’une instance.

</dd> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

La classe source n’a pas été entièrement définie ou inscrite avec WMI, de sorte qu’une nouvelle classe dérivée n’est pas autorisée.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’objet qui est retourné automatiquement devient une sous-classe de l’objet actuel. Ce comportement ne peut pas être substitué. Il n’existe aucune autre méthode permettant de créer des classes dérivées.

Vous ne pouvez pas créer une classe dérivée à partir d’une classe qui est locale à votre propre processus client. Avant d’utiliser cette méthode pour créer une classe dérivée, vous devez créer la classe de base. Pour créer la classe de base, appelez [**SWbemObject. \_ put**](swbemobject-put-.md)et récupérez la classe de base à l’aide de [**SWbemServices. obtenir**](swbemservices-get.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




