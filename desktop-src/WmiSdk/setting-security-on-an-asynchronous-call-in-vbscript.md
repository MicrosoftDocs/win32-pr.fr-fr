---
description: Les performances des appels semi-synchrones sont généralement adaptées à la plupart des situations.
ms.assetid: f665fc60-68bd-495d-a441-e3a9473f9d89
ms.tgt_platform: multiple
title: Définition de la sécurité sur un appel asynchrone dans VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 972947e0cb4f5d385e4d2d27b7c14298771ac4e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536649"
---
# <a name="setting-security-on-an-asynchronous-call-in-vbscript"></a>Définition de la sécurité sur un appel asynchrone dans VBScript

Les performances des appels [*semi-synchrones*](gloss-s.md) sont généralement adaptées à la plupart des situations. Les appels asynchrones ne sont généralement pas une pratique recommandée pour les scripts. Toutefois, si des appels asynchrones doivent être effectués, une valeur de Registre peut être définie pour forcer WMI à effectuer des vérifications d’accès sur les appels asynchrones.


La valeur de Registre **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** détermine si WMI vérifie la présence d’un niveau d’authentification acceptable lors du retour de données pour un appel asynchrone. Le rappel peut être retourné à un niveau d’authentification inférieur à celui de l’appel asynchrone d’origine. Par défaut, cette valeur est définie sur zéro afin que les rappels ne soient pas vérifiés. Pour sécuriser les appels asynchrones dans les scripts, vous devez définir la clé de Registre sur 1 (un).

Les scripts peuvent utiliser les méthodes [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) et [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) de l’objet Registry [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) pour modifier le paramètre de la valeur de Registre **UnsecAppAccessControlDefault** . Pour plus d’informations sur les niveaux d’authentification et d’emprunt d’identité requis pour l’accès à distance, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).

## <a name="to-set-asynchronous-call-security-in-vbscript"></a>Pour définir la sécurité des appels asynchrones dans VBScript

L’exemple de code VBScript suivant montre comment modifier la valeur de Registre pour contrôler l’authentification WMI des rappels.

Le script modifie la valeur de **UnsecAppAccessControlDefault** de zéro à un, ou si la valeur est déjà définie, de 1 à zéro. Zéro est la valeur par défaut sur un système nouvellement installé. Une fois l’indicateur défini, le paramètre persiste lors du redémarrage ou du redémarrage de WMI.

Le script utilise un objet [**SWbemMethod. ins**](swbemmethod-inparameters.md) et [**SWbemObject.ExeCMethod**](swbemobject-execmethod-.md) pour appeler [**StdRegProv. GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) et [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov). Pour plus d’informations sur la définition des valeurs dans un objet **Parameters** , consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Pour obtenir un exemple d’appel de Registre à l’aide de [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), consultez [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).


```VB
' Registry key value in hex
Const hklm = &h800000002  
' Subkey string 
Const Subkey = "software\\microsoft\\wbem\\cimom" 
' Asynchronous access control
Const sValueName = "UnsecAppAccessControlDefault" 

' Obtain registry object
Set objReg = GetObject("winmgmts:root\default:StdRegProv") 

' Get the initial value of the asynchronous 
'   access control registry key
' Use an InParameters object to set up the 
'   parameters for the ExecMethod call
' For more information see Constructing InParameters Objects 
'   topic and SWbemObject.ExecMethod_ topic

Set InParams = objReg.methods_("GetStringValue").InParameters.SpawnInstance_
InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName

' Get return value from OutParameters object returned by ExecMethod. 
' For more information see Parsing OutParameters Objects topic

Set OutParams = objReg.Execmethod_("GetStringValue",InParams)

If (OutParams.ReturnValue <> 0) then
   Wscript.Echo "GetStringValue returned " & OutParams.ReturnValue
   Wscript.Quit 1
End If

Svalue = OutParams.sValue
If (sValue = 0) Then
   AccessControl = "WMI not performing asynch access control"
Else 
   AccessControl = "WMI performing asynch access control"  
End If
Wscript.Echo sValueName & " = " _
    & sValue & VBNewLine & AccessControl

' Change asynchronous access control registry key value
Set InParams = objReg.methods_("SetStringValue").InParameters.SpawnInstance_

InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName
InParams.sValue = sValue XOR 1

Set OutParams = objReg.ExecMethod_("SetStringValue",InParams)

If (OutParams.Returnvalue <> 0) Then
    Wscript.Echo "SetStringValue returned " & OutParams.Returnvalue
    Wscript.Quit 1
End If

Wscript.Echo SValueName & " changed to " & (sValue XOR 1)
```



 

 
