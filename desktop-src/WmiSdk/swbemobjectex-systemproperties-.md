---
description: Retourne un objet SWbemPropertySet qui contient la collection de propriétés système WMI qui s’appliquent à l’objet.
ms.assetid: e95c325a-8851-4f55-a99d-4346d064e308
ms.tgt_platform: multiple
title: SWbemObjectEx.SystemProperties_ propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.SystemProperties_
- ISWbemObjectEx.SystemProperties_
- ISWbemObjectEx.get_SystemProperties_
- ISWbemObjectEx.put_SystemProperties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cf8b7e15536c0d4e3116f0583662b3cd0b7d0887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210416"
---
# <a name="swbemobjectexsystemproperties_-property"></a>SWbemObjectEx.Sys\_ propriété temProperties

La **propriété \_ SystemProperties** de l’objet [**SWbemObjectEx**](swbemobjectex.md) retourne un objet [**SWbemPropertySet**](swbempropertyset.md) qui contient la collection de [Propriétés système WMI](wmi-system-properties.md) qui s’appliquent à l’objet.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
SWbemObjectEx.SystemProperties_ As Object
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="examples"></a>Exemples

L’exemple de code suivant récupère les valeurs de propriété pour la \_ classe de processus Win32.


```VB
Set objWmi = GetObject ("winmgmts:root\cimv2")
Set objClass = objWmi.Get("Win32_Process")

' SWbemObjectEx.SystemProperties_ returns 
' an SWbemPropertySet object that contains the collection
' of sytem properties for Win32_Process class

For Each objProperty In objClass.SystemProperties_

    WScript.Echo vbCrLf & objProperty.Name & ":"

    ' Have to take into account that
    ' __Derivation is an array

    If Not objProperty.IsArray Then
        WScript.Echo vbTab & objProperty.Value
    Else
        For Each strValue In objProperty.Value
            WScript.Echo vbTab & strValue
        Next
    End If

Next
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> </dl>

 

 




