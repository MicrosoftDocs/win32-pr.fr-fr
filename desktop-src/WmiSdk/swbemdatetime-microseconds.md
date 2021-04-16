---
description: Obtient ou définit une valeur qui représente le composant microsecondes de la valeur DateTime.
ms.assetid: b810b781-86a3-4730-8114-44d10454f7c3
ms.tgt_platform: multiple
title: Propriété SWbemDateTime. microsecondrs (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Microseconds
- ISWbemDateTime.Microseconds
- ISWbemDateTime.get_Microseconds
- ISWbemDateTime.put_Microseconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 94213eb70a98be1af8f8404ddece8bf2f07ca807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320825"
---
# <a name="swbemdatetimemicroseconds-property"></a>SWbemDateTime. microsecondes, propriété

La propriété **microsecondes** de l’objet [**SWbemDateTime**](swbemdatetime.md) obtient ou définit une valeur qui représente le composant microsecondes de la valeur DateTime.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
SWbemDateTime.Microseconds As Long
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="error-codes"></a>Codes d’erreur

Une fois que vous avez obtenu ou défini la propriété **microsecondes** , l’objet **Err** peut contenir le code d’erreur ci-dessous.

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B)
</dt> <dd>

La valeur n’était pas comprise dans la plage comprise entre 0 et 999999.

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

[**SWbemDateTime.MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Date/heure**](datetime.md)
</dt> </dl>

 

 




