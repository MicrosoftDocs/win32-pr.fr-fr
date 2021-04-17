---
description: Convertit une valeur de date et d’heure au format DATETIME CIM au format FILETIME.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: Méthode SWbemDateTime. GetFileTime (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f8a8c85cb4c78be578187b1f55afce078fe7bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485729"
---
# <a name="swbemdatetimegetfiletime-method"></a>Méthode SWbemDateTime. GetFileTime

La méthode **GetFileTime** de l’objet [**SWbemDateTime**](swbemdatetime.md) convertit une valeur de date et d’heure dans le format [DateTime](datetime.md) CIM au format FILETIME.

Si le paramètre est défini sur **true**, la valeur de retour représente une heure locale pour le client. Dans le cas contraire, la valeur de retour est une heure UTC (Coordinated Universal Time). Une structure [DateTime](datetime.md) **fileTime** est une valeur 64 bits qui représente le nombre d’unités de 100 nanosecondes depuis le début du 1er janvier 1601. Windows Management Instrumentation (WMI) traite les valeurs **fileTime** comme des représentations sous forme de chaîne de nombres 64 bits non signés.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bIsLocaL* \[ dans, facultatif\]
</dt> <dd>

Indique si la valeur retournée est interprétée comme heure locale. La propriété UTC contient ensuite l’heure locale convertie en décalage UTC (temps universel coordonné) correct. Si la valeur est **false**, la valeur est interprétée comme étant UTC avec un décalage de zéro (0).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Date et heure au format **fileTime** .

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **GetFileTime** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur figurant dans la liste suivante.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

L'appel a échoué.

</dd> </dl>

## <a name="remarks"></a>Notes

**VT \_** Les valeurs de date et **fileTime** ne peuvent pas contenir de champs génériques.

La méthode **GetFileTime** échoue (wbemErrFailed) si l’une des propriétés suivantes a la **valeur false**:

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

En cas de retour réussi de [**SetFileTime**](swbemdatetime-setfiletime.md), toutes ces propriétés ont la valeur **true**.

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

[**SWbemDateTime. getVarDate,**](swbemdatetime-getvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Date/heure**](datetime.md)
</dt> </dl>

 

