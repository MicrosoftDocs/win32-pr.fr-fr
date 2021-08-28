---
description: Utilisez la \_ méthode SpawnInstance de l’objet SWbemObject pour créer une nouvelle instance d’une classe.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: Méthode SWbemObject.SpawnInstance_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1b465bb53fd031dff397ef0ddf39db39d5d9987f03e037becebcd8dd41a65b87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640039"
---
# <a name="swbemobjectspawninstance_-method"></a>SWbemObject. SpawnInstance, \_ méthode

Utilisez la **méthode \_ SpawnInstance** de l’objet [**SWbemObject**](swbemobject.md) pour créer une nouvelle instance d’une classe. L’objet actuel doit être une définition de classe obtenue à partir de WMI via une méthode telle que [**SWbemServices. obtenir**](swbemservices-get.md) ou [**SWbemServices.ExecQuery**](swbemservices-execquery.md). Utilisez ensuite cette définition de classe pour créer des instances. Créez chaque nouvelle instance localement au sein du processus, puis appelez [**SWbemObject. put \_**](swbemobject-put-.md) pour réellement créer l’instance dans WMI.

> [!Note]  
> La génération d’une instance à partir d’une instance est prise en charge, mais l’instance retournée est vide.

 

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Réservé et doit être égal à zéro s’il est spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cet appel retourne un objet [**SWbemObject**](swbemobject.md) qui contient une nouvelle instance de la classe.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la **méthode \_ SpawnInstance** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

L’objet actuel n’est pas une définition de classe valide et ne peut pas générer de nouvelles instances. Soit il est incomplet, soit il n’a pas été inscrit auprès de WMI à l’aide de [**SWbemObject. put \_**](swbemobject-put-.md).

</dd> <dt>

**wbemErrIllegalOperation** -2147749918 (0x8004101E)
</dt> <dd>

Retourné si cette méthode est utilisée sur une instance au lieu d’une classe.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre non valide a été spécifié.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

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



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**M**](swbemobject.md)
</dt> <dt>

[**SWbemObject. put\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServices.**](swbemservices-get.md)
</dt> </dl>

 

 




