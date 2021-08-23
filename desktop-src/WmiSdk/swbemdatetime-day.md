---
description: Obtient ou définit une valeur qui représente le composant « jour » de la valeur DateTime.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: SWbemDateTime. Day, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Day
- ISWbemDateTime.Day
- ISWbemDateTime.get_Day
- ISWbemDateTime.put_Day
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d2483e52d9b40978a28f96bb5352df4f9abf4f89becf52550b82fd931580d7e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640499"
---
# <a name="swbemdatetimeday-property"></a>SWbemDateTime. Day, propriété

La propriété **Day** de l’objet [**SWbemDateTime**](swbemdatetime.md) obtient ou définit une valeur qui représente le composant Day de la valeur DateTime. La valeur doit être comprise entre 1 et 31 si [**IsInterval**](swbemdatetime-isinterval.md) a la valeur **false**. Toutefois, la vérification des erreurs n’est pas sensible à la valeur du mois. Par conséquent, la valeur dans la plage de 31 ne retourne pas d’erreur dans les cas où la valeur [**SWbemDateTime. month**](swbemdatetime-month.md) correspond à un mois de moins de 31 jours (février, avril, juin, septembre).

La valeur par défaut pour **Day** est 01.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="error-codes"></a>Codes d’erreur

Une fois que vous avez obtenu ou défini la propriété **Day** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur ci-dessous.

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B)
</dt> <dd>

Si [**IsInterval**](swbemdatetime-isinterval.md) a la **valeur true** et que la plage des valeurs correctes est supérieure à 0 à 99999999.

</dd> </dl>

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

[**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Date/heure](datetime.md)
</dt> </dl>

 

