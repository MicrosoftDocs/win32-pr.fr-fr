---
description: La propriété Origin de l’objet SWbemProperty récupère le nom de la classe WMI dans laquelle cette propriété a été introduite. Pour les classes avec des hiérarchies d’héritage profond, il est souvent souhaitable de savoir quelles propriétés ont été déclarées dans quelles classes.
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: Propriété SWbemProperty. Origin (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Origin
- ISWbemProperty.Origin
- ISWbemProperty.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f0aef6c1041e14d65ee3cbacaa40255421a1b064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203155"
---
# <a name="swbempropertyorigin-property"></a>SWbemProperty. Origin, propriété

La propriété **origin** de l’objet [**SWbemProperty**](swbemproperty.md) récupère le nom de la classe WMI dans laquelle cette propriété a été introduite. Pour les classes avec des hiérarchies d’héritage profond, il est souvent souhaitable de savoir quelles propriétés ont été déclarées dans quelles classes.

Si la propriété est locale (consultez [**SWbemQualifier. IsLocal**](swbemqualifier-islocal.md)), cette valeur est la même que la classe propriétaire. Cette propriété est en lecture seule.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemProperty.Origin As String
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemProperty<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



 

 




