---
description: Valeur booléenne qui indique si le composant microsecondes dans la valeur DateTime CIM contient un intervalle ou une valeur générique.
ms.assetid: 65244ece-2326-4edc-b982-57e2046ec33e
ms.tgt_platform: multiple
title: SWbemDateTime. MicrosecondsSpecified, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.get_MicrosecondsSpecified
- ISWbemDateTime.put_MicrosecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d4fa9d99cf323e19ccd298786896f789bbb08be6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540842"
---
# <a name="swbemdatetimemicrosecondsspecified-property"></a>SWbemDateTime. MicrosecondsSpecified, propriété

La propriété **MicrosecondsSpecified** de l’objet [**SWbemDateTime**](swbemdatetime.md) est une valeur booléenne qui indique si le composant microsecondes dans la valeur DateTime CIM contient un intervalle ou une valeur générique. Si **MicrosecondsSpecified** a la valeur **true** et que [**IsInterval**](swbemdatetime-isinterval.md) a la valeur **false**, [**SWbemDateTime. microsecondes**](swbemdatetime-microseconds.md) contient une valeur DateTime. Une valeur DateTime qui contient un intervalle ne peut pas être convertie au format de **\_ Date VT** ou **fileTime** . Si [**HoursSpecified**](swbemdatetime-hoursspecified.md) a la **valeur false** et que **IsInterval** a la **valeur true**, **SWbemDateTime. microsecondes** contient un intervalle.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
SWbemDateTime.MicrosecondsSpecified As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="examples"></a>Exemples

Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md). Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).

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

[**SWbemDateTime. microsecondes**](swbemdatetime-microseconds.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Date/heure](datetime.md)
</dt> </dl>

 

 




