---
description: Valeur booléenne qui indique si le composant « mois » dans la valeur DateTime CIM contient un intervalle ou une valeur générique.
ms.assetid: 12dd94de-24be-4b13-bde5-2fc28be94efa
ms.tgt_platform: multiple
title: SWbemDateTime. MonthSpecified, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MonthSpecified
- ISWbemDateTime.MonthSpecified
- ISWbemDateTime.get_MonthSpecified
- ISWbemDateTime.put_MonthSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 52b44444a5810577289353778c2c00b1ebfb80fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916915"
---
# <a name="swbemdatetimemonthspecified-property"></a>SWbemDateTime. MonthSpecified, propriété

La propriété **MonthSpecified** de l’objet [**SWbemDateTime**](swbemdatetime.md) est une valeur booléenne qui indique si le composant month dans la valeur DateTime CIM contient un intervalle ou une valeur générique. Si **MonthSpecified** a la valeur **true** et que [**IsInterval**](swbemdatetime-isinterval.md) a la valeur **false**, [**SWbemDateTime. month**](swbemdatetime-month.md) contient une valeur de date. Une valeur DateTime qui contient un intervalle ne peut pas être convertie au format de **\_ Date VT** ou **fileTime** . Si **MonthSpecified** a la **valeur false** et que **IsInterval** a la **valeur true**, **SWbemDateTime. month** contient un intervalle.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
SWbemDateTime.MonthSpecified As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="examples"></a>Exemples

Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md). Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).

## <a name="requirements"></a>Spécifications



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

[**SWbemDateTime. mois**](swbemdatetime-month.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Date/heure](datetime.md)
</dt> </dl>

 

 




