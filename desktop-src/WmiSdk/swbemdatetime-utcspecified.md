---
description: Valeur booléenne qui indique si le composant de temps UTC (Universal Coordinated Time) dans la valeur DateTime CIM contient un intervalle ou une valeur générique.
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: SWbemDateTime. UTCSpecified, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 80c8ab92d07c2ef75ea57a66f6bae26c428780e15beeae31c9e5bd883407f03f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640369"
---
# <a name="swbemdatetimeutcspecified-property"></a>SWbemDateTime. UTCSpecified, propriété

La propriété **UTCSpecified** de l’objet [**SWbemDateTime**](swbemdatetime.md) est une valeur booléenne qui indique si le composant de l’heure UTC (Universal Coordinated Time) de la valeur DateTime CIM contient un intervalle ou une valeur générique. Si **UTCSpecified** a la valeur **true** et que [**IsInterval**](swbemdatetime-isinterval.md) a la valeur **false**, [**SWbemDateTime. UTC**](swbemdatetime-utc.md) contient une valeur [**DateTime**](datetime.md) . Une valeur **DateTime** qui contient un intervalle ne peut pas être convertie au format de **\_ Date VT** ou **fileTime** . Si **UTCSpecified** a la **valeur false** et que **IsInterval** a la **valeur true**, **SWbemDateTime. UTC** contient un intervalle.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="examples"></a>Exemples

Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md). Pour obtenir une description du format DateTime CIM, consultez [format de date et d’heure](date-and-time-format.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemDateTime. UTC**](swbemdatetime-utc.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Date/heure](datetime.md)
</dt> </dl>

 

 




