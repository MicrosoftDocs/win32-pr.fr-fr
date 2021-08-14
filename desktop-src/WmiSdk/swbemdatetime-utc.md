---
description: Obtient ou définit la représentation en temps universel coordonné (UTC) de la valeur DateTime.
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.tgt_platform: multiple
title: Propriété SWbemDateTime. UTC (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTC
- ISWbemDateTime.UTC
- ISWbemDateTime.get_UTC
- ISWbemDateTime.put_UTC
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c1bb3307116042a61aae06489bec7d8eabbf7859f3e8770811b50680dcfe5cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314692"
---
# <a name="swbemdatetimeutc-property"></a>SWbemDateTime. UTC, propriété

La propriété **UTC** de l’objet [**SWbemDateTime**](swbemdatetime.md) obtient ou définit la représentation en temps universel coordonné (UTC) de la valeur **DateTime** . UTC est l’heure définie par la norme de l’heure du monde. L’heure UTC a remplacé l’heure GMT (Greenwich Mean Time). Une valeur UTC avec un décalage égal à zéro est identique à l’heure GMT avec un décalage de zéro. Le nombre signé doit être compris entre-720 et 720, ou l’erreur **wbemErrValueOutOfRange** est retournée.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
SWbemDateTime.UTC As Long
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="error-codes"></a>Codes d’erreur

Une fois que vous avez obtenu ou défini la propriété **UTC** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur ci-dessous.

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B)
</dt> <dd>

La valeur n’était pas comprise dans la plage comprise entre-720 et 720.

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

[**SWbemDateTime.UTCSpecified**](swbemdatetime-utcspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Date/heure**](datetime.md)
</dt> </dl>

 

