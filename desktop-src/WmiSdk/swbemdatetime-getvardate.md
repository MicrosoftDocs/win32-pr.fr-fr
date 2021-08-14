---
description: Convertit une valeur de date et d’heure au format DATETIME CIM au \_ format de date VT.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: Méthode SWbemDateTime. getVarDate, (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 506c897da130b9558b37637918674a7c6024adb787ac3d91e53e430a6edfcd1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314754"
---
# <a name="swbemdatetimegetvardate-method"></a>Méthode SWbemDateTime. getVarDate,

La méthode **getVarDate,** de l’objet [**SWbemDateTime**](swbemdatetime.md) convertit une valeur de date et d’heure au format [**DateTime**](datetime.md) CIM au format de **\_ Date VT** .

le format de **\_ DATE VT** est une valeur [**DATETIME**](datetime.md) automation variant qui Visual Basic et ActiveX utiliser.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bIsLocal* \[ dans, facultatif\]
</dt> <dd>

Indique si la valeur retournée est interprétée comme heure locale. La propriété temps universel coordonné (UTC, Universal Time Coordinated) contient l’heure locale convertie en décalage UTC correct. Si la valeur est **false**, la valeur est interprétée comme étant UTC avec un décalage de zéro (0).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur de date et d’heure au format de **\_ Date VT** .

## <a name="remarks"></a>Remarques

**VT \_** Les valeurs de date et **fileTime** ne peuvent pas contenir de champs génériques.

La méthode **getVarDate,** échoue (**wbemErrFailed**) si l’une des propriétés suivantes a la **valeur false**:

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

En cas de retour réussi de [**SetVarDate**](swbemdatetime-setvardate.md), toutes ces propriétés ont la valeur **true**.

Après un appel réussi à [**SetVarDate**](swbemdatetime-setvardate.md), la valeur [**DateTime**](datetime.md) est toujours interprétée comme une valeur **DateTime** absolue au lieu d’un intervalle, et [**IsInterval**](swbemdatetime-isinterval.md) est défini sur **false**.

Si [**IsInterval**](swbemdatetime-isinterval.md) a la valeur **true**, un appel à **getVarDate,** provoque l’erreur **wbemErrFailed** .

Une perte de précision se produit lorsque vous appelez **getVarDate,**, car les valeurs [DateTime](datetime.md) ont une résolution d’une microseconde (s), et les valeurs de **\_ DATE VT** ont une résolution de 500 millisecondes.

## <a name="examples"></a>Exemples

Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format de **\_ Date** **fileTime** ou VT, consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md). Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).

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

[**SWbemDateTime. GetFileTime**](swbemdatetime-getfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Date/heure](datetime.md)
</dt> </dl>

 

 




