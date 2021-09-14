---
description: Obtient ou définit une valeur qui représente le composant « année » de la valeur DATETIME.
ms.assetid: eab3738a-c92a-4602-b1ee-e2547da88308
ms.tgt_platform: multiple
title: Propriété SWbemDateTime. Year (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Year
- ISWbemDateTime.Year
- ISWbemDateTime.get_Year
- ISWbemDateTime.put_Year
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5fe8988b3772f0f5d976c38eb5e9cc44fb9c4ede
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292835"
---
# <a name="swbemdatetimeyear-property"></a>SWbemDateTime. Year, propriété

La propriété **year** de l’objet [**SWbemDateTime**](swbemdatetime.md) obtient ou définit une valeur qui représente le composant Year de la valeur [**DateTime**](datetime.md) . La valeur doit être comprise dans la plage 0000-9999 ou l’erreur wbemErrValueOutOfRange est retournée.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
SWbemDateTime.Year As Long
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="error-codes"></a>Codes d’erreur

Une fois que vous avez obtenu ou défini la propriété **year** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur ci-dessous.

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B)
</dt> <dd>

La valeur n’était pas comprise dans la plage de 0000 à 9999.

</dd> </dl>

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

[**SWbemDateTime.YearSpecified**](swbemdatetime-yearspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Date/heure**](datetime.md)
</dt> </dl>

 

