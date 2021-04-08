---
description: La \_ propriété Path de l’objet SWbemLastError retourne un objet SWbemObjectPath qui représente le chemin d’accès de l’objet de la classe ou de l’instance en cours. Cette propriété peut être passée en tant que paramètre aux méthodes qui requièrent un chemin d’accès d’objet.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: SWbemLastError.Path_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c979fd76ffb4ee97f62362d53fac4151de17bae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034726"
---
# <a name="swbemlasterrorpath_-property"></a>SWbemLastError. Path, \_ propriété

La **propriété \_ path** de l’objet [**SWbemLastError**](swbemlasterror.md) retourne un objet [**SWbemObjectPath**](swbemobjectpath.md) qui représente le chemin d’accès de l’objet de la classe ou de l’instance en cours. Cette propriété peut être passée en tant que paramètre aux méthodes qui requièrent un chemin d’accès d’objet.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

Seule la propriété de [**classe**](swbemobjectpath-class.md) de l’instance [**SWbemObjectPath**](swbemobjectpath.md) retournée peut être modifiée. Si vous essayez de modifier une autre propriété ou si vous essayez d’appeler les méthodes [**SetAsClass**](swbemobjectpath-setasclass.md) ou [**SetAsSingleton**](swbemobjectpath-setassingleton.md) , vous recevez une erreur de **wbemErrReadOnly**.

Pour cette raison, vous ne pouvez pas modifier l’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui est la valeur de la propriété [**Keys**](swbemobjectpath-keys.md) de l’instance [**SWbemObjectPath**](swbemobjectpath.md) retournée. Si vous essayez d’appeler les méthodes [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)ou [**DeleteAll**](swbemnamedvalueset-deleteall.md) sur cette valeur, vous recevez une erreur **wbemErrReadOnly** . En outre, vous ne pouvez pas modifier les [**SWbemNamedValue**](swbemnamedvalue.md) obtenus à partir de cette collection. Les tentatives de modification de la propriété [**value**](swbemnamedvalue-value.md) retournent le même code d’erreur.

Toutefois, si vous appelez [**SWbemObject. Clone \_**](swbemobject-clone-.md) pour créer une copie, la propriété [**path \_**](swbemobject-path-.md) de la copie est entièrement modifiable.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




