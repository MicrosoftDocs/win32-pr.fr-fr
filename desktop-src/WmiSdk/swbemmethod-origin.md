---
description: La propriété Origin de l’objet SWbemMethod retourne le nom de la classe dans laquelle cette méthode a été introduite.
ms.assetid: da98393b-af95-47ad-b589-663063f65afb
ms.tgt_platform: multiple
title: Propriété SWbemMethod. Origin (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.Origin
- ISWbemMethod.Origin
- ISWbemMethod.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c1b903a2c55bbd571a9cd1f36a51812a70c123cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292794"
---
# <a name="swbemmethodorigin-property"></a>SWbemMethod. Origin, propriété

La propriété **origin** de l’objet [**SWbemMethod**](swbemmethod.md) retourne le nom de la classe dans laquelle cette méthode a été introduite. Pour les classes avec des hiérarchies d’héritage profond, il est souvent souhaitable de savoir quelles méthodes ont été déclarées dans quelles classes. Cette propriété est en lecture seule.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemMethod.Origin As String
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethod<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemMethod<br/>                                                            |



 

 




