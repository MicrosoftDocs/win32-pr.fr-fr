---
description: L’objet SWbemDateTime est un objet d’assistance pour analyser et définir des valeurs DateTime Common Information Model (CIM).
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: Objet SWbemDateTime (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 65f3f9836b52693e3f74bac5cfd94553e02d7bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519747"
---
# <a name="swbemdatetime-object"></a>Objet SWbemDateTime

L’objet **SWbemDateTime** est un objet d’assistance pour analyser et définir des valeurs [DateTime](datetime.md) Common Information Model (CIM). Il joue un rôle similaire à [**SWbemObjectPath**](swbemobjectpath.md), qui fournit une assistance pour mettre en forme et interpréter les chemins d’accès aux objets. Vous pouvez utiliser l’appel VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) pour créer l’objet **SWbemDateTime** .

Un objet **SWbemDateTime** peut être initialisé à partir de et mis en forme dans les valeurs **VT \_ Date** ou **fileTime** à l’aide de méthodes sur l’objet. À l’aide des propriétés de l’objet, la valeur peut être analysée en composant l’année, le mois, le jour, l’heure, les minutes, les secondes ou les microsecondes. L’objet **SWbemDateTime** peut être mis en forme en valeurs locales ou de temps universel coordonné (UTC, Universal Time Coordinated). Pour plus d’informations, consultez [format de date et d’heure](date-and-time-format.md).

**SWbemDateTime** est le seul objet de script Windows Management Instrumentation (WMI) qui est marqué comme sécurisé pour l’initialisation et les scripts s’exécutant sur les pages HTML dans Internet Explorer.

## <a name="members"></a>Membres

L’objet **SWbemDateTime** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemDateTime** a ces méthodes.



| Méthode                                           | Description                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**GetFileTime**](swbemdatetime-getfiletime.md) | Convertit une date et une heure de **fileTime** , exprimées sous forme de **BSTR**, au format [DateTime](datetime.md) WMI.<br/> |
| [**GetVarDate,**](swbemdatetime-getvardate.md)   | Convertit une valeur de date et d’heure au format [DateTime](datetime.md) WMI en une **\_ Date VT**.<br/>                  |
| [**SetFileTime**](swbemdatetime-setfiletime.md) | Convertit un format [DateTime](datetime.md) WMI en date et heure **fileTime** , exprimé sous forme de **BSTR**.<br/>  |
| [**SetVarDate**](swbemdatetime-setvardate.md)   | Convertit une date et une heure au format de **\_ Date VT** en [DateTime](datetime.md)WMI.<br/>                        |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemDateTime** a ces propriétés.



| Propriété                                                                        | Type d’accès           | Description                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Temps**](swbemdatetime-day.md)<br/>                                     | Lecture/écriture<br/> | Composant « jour » d’une valeur [DateTime](datetime.md) CIM.<br/>                                                           |
| [**DaySpecified**](swbemdatetime-dayspecified.md)<br/>                   | Lecture/écriture<br/> | Indique si le jour est spécifié ou laissé comme caractère générique.<br/>                                                        |
| [**Heures**](swbemdatetime-hours.md)<br/>                                 | Lecture/écriture<br/> | Heures du composant « jour » d’une valeur [DateTime](datetime.md) CIM.<br/>                                              |
| [**HoursSpecified**](swbemdatetime-hoursspecified.md)<br/>               | Lecture/écriture<br/> | Indique si l’heure est spécifiée ou laissée comme caractère générique.<br/>                                                       |
| [**IsInterval**](swbemdatetime-isinterval.md)<br/>                       | Lecture/écriture<br/> | Indique qu’au moins un composant de la valeur [DateTime](datetime.md) CIM représente un intervalle et non une date.<br/> |
| [**Microsecondes**](swbemdatetime-microseconds.md)<br/>                   | Lecture/écriture<br/> | Composant microsecondes d’une valeur [DateTime](datetime.md) CIM.<br/>                                                  |
| [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)<br/> | Lecture/écriture<br/> | Indique si le composant microsecondes est spécifié ou laissé comme caractère générique.<br/>                                     |
| [**Maximum**](swbemdatetime-minutes.md)<br/>                             | Lecture/écriture<br/> | Composant « minutes » d’une valeur [DateTime](datetime.md) CIM.<br/>                                                       |
| [**MinutesSpecified**](swbemdatetime-minutesspecified.md)<br/>           | Lecture/écriture<br/> | Indique si le composant « minutes » est spécifié ou laissé comme caractère générique.<br/>                                          |
| [**Chronique**](swbemdatetime-month.md)<br/>                                 | Lecture/écriture<br/> | Composant « mois » d’une valeur [DateTime](datetime.md) CIM.<br/>                                                         |
| [**MonthSpecified**](swbemdatetime-monthspecified.md)<br/>               | Lecture/écriture<br/> | Indique si le mois est spécifié ou laissé comme caractère générique.<br/>                                                      |
| [**Durée**](swbemdatetime-seconds.md)<br/>                             | Lecture/écriture<br/> | Composant « secondes » d’une valeur [DateTime](datetime.md) CIM.<br/>                                                       |
| [**SecondsSpecified**](swbemdatetime-secondsspecified.md)<br/>           | Lecture/écriture<br/> | Indique si le composant seconds est spécifié ou laissé comme caractère générique.<br/>                                          |
| [**UNIVERSEL**](swbemdatetime-utc.md)<br/>                                     | Lecture/écriture<br/> | Composant UTC d’une valeur [DateTime](datetime.md) CIM.<br/>                                                           |
| [**UTCSpecified**](swbemdatetime-utcspecified.md)<br/>                   | Lecture/écriture<br/> | Indique si le composant UTC est spécifié ou laissé comme caractère générique.<br/>                                              |
| [**Valeur**](swbemdatetime-value.md)<br/>                                 | Lecture/écriture<br/> | Valeur [DateTime](datetime.md) CIM complète.<br/>                                                                         |
| [**Year**](swbemdatetime-year.md)<br/>                                   | Lecture/écriture<br/> | Composant d’année d’une valeur [DateTime](datetime.md) CIM.<br/>                                                          |
| [**YearSpecified**](swbemdatetime-yearspecified.md)<br/>                 | Lecture/écriture<br/> | Indique si l’année est spécifiée ou conservée comme caractère générique.<br/>                                                |



 

## <a name="remarks"></a>Notes

WMI enregistre les horodateurs au format UTC (Universal Time Coordinate). L’heure UTC n’est pas le format utilisé par la plupart des développeurs et administrateurs informatiques. Par conséquent, un problème courant consiste à déterminer comment traduire le temps universel coordonné (UTC) en un nom plus lisible. Pour plus d’informations sur l’utilisation du temps universel coordonné (UTC), consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md) et [utilisation de dates et d’heures à l’aide de WMI](/previous-versions/tn-archive/ee198928(v=technet.10)). Vous pouvez également lire les informations [sur le temps (OH et sur les dates)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) et [comment soustraire un nombre spécifié de jours d’une valeur UTC ?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) billets de blog pour plus d’informations.

Tout champ numérique peut avoir une valeur générique si la propriété [**IsInterval**](swbemdatetime-isinterval.md) est définie sur **false**. Les champs avec des valeurs de caractère générique contiennent des astérisques dans le champ entier.

Chaque propriété, par exemple [**Day**](swbemdatetime-day.md), a une valeur booléenne spécifiée correspondante, telle que [**DaySpecified**](swbemdatetime-dayspecified.md). Quand **DaySpecified** a la valeur **false**, la valeur est interprétée comme un intervalle plutôt que comme un nombre compris entre 01 et 31. Si un intervalle est utilisé n’importe où dans la valeur [DateTime](datetime.md) CIM, [**IsInterval**](swbemdatetime-isinterval.md) est également défini sur **true**. La valeur par défaut est pour une valeur DateTime CIM qui contient une date plutôt qu’un ou plusieurs intervalles.

Par exemple, si [**SWbemDateTime. DaySpecified**](swbemdatetime-dayspecified.md) a la valeur **true**, [**SWbemDateTime. Value**](swbemdatetime-value.md) comprend la valeur actuelle de [**SWbemDateTime. Day**](swbemdatetime-day.md), sinon il s’agit d’une valeur générique. Dans les deux cas, la propriété [**IsInterval**](swbemdatetime-isinterval.md) a la **valeur false** .

## <a name="examples"></a>Exemples

L’exemple de code de script suivant montre comment utiliser un objet **SWbemDateTime** pour analyser une valeur de propriété DateTime lue à partir de l’espace de stockage WMI, la propriété **InstallDate** dans [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



L’exemple suivant montre comment créer un objet **SWbemDateTime** , stocker une valeur de date dans l’objet, afficher la date comme locale et le temps universel coordonné (UTC), et stocker la valeur dans une classe et une propriété nouvellement créées. Pour plus d’informations sur la constante **wbemCimtypeDatetime**, consultez [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



L’exemple de code de script suivant montre comment utiliser un objet **SWbemDateTime** pour modifier une valeur d’intervalle sur une propriété lue à partir de l’espace de stockage WMI.


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



L’exemple de code de script suivant montre comment utiliser un objet **SWbemDate** pour lire une valeur **fileTime** .


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



Le code PowerShell suivant crée une instance d’un objet SWbemDateTime, récupère la date d’installation du système d’exploitation et convertit la date dans un format différent.


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



Le code PowerShell suivant convertit le code dans un format prêt à être utilisé par un fournisseur CIM.


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



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

[WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[Date/heure](datetime.md)
</dt> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

