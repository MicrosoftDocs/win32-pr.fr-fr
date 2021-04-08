---
description: La propriété Keys de l’objet SWbemObjectPath est un objet SWbemNamedValueSet qui contient les liaisons de valeur de clé. Cette propriété est en lecture seule.
ms.assetid: 1919403d-6dea-4d41-9bc7-a622a9c9c2c8
ms.tgt_platform: multiple
title: SWbemObjectPath. Keys, propriété (Adoctint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Keys
- ISWbemObjectPath.Keys
- ISWbemObjectPath.get_Keys
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898ae7dac4a9c63273a8ff45a85b5bbb65aaa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034253"
---
# <a name="swbemobjectpathkeys-property"></a>SWbemObjectPath. Keys, propriété

La propriété **Keys** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) est un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui contient les liaisons de valeur de clé. Cette propriété est en lecture seule.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemObjectPath.Keys As Object
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="error-codes"></a>Codes d’erreur

Une fois que vous avez récupéré la propriété **Keys** , l’objet **Err** peut contenir le code d’erreur ci-dessous.

<dl> <dt>

**wbemErrNotSupported** -2147749900 (0x8004100C)
</dt> <dd>

La fonctionnalité ou l'opération n'est pas prise en charge. Cette erreur est retournée si un script tente d’écrire dans cette propriété.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                             |
| En-tête<br/>                   | <dl> <dt>Adoctint. h (inclure wbemdisp. h)</dt> </dl> |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl>                    |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                                          |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                                           |



 

 




