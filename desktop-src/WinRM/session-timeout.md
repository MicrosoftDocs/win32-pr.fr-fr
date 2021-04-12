---
title: Session. Timeout, propriété (WSManDisp. h)
description: Définit et obtient la durée maximale, en millisecondes, pendant laquelle l’application cliente attend Windows Remote Management exécuter ses opérations.
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- Propriété Timeout Windows Remote Management
- Propriété Timeout Windows Remote Management, objet session
- Windows Remote Management de l’objet session, propriété Timeout
topic_type:
- apiref
api_name:
- Session.Timeout
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6c28b5284d9061e1c80fb3c66193d394c347a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317521"
---
# <a name="sessiontimeout-property"></a>Session. Timeout (propriété)

Définit et obtient la durée maximale, en millisecondes, pendant laquelle l’application cliente attend Windows Remote Management exécuter ses opérations.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Session.Timeout As long
```



## <a name="property-value"></a>Valeur de la propriété

Valeur du délai d’attente, en millisecondes. Lorsque la valeur du délai d’attente est dépassée, une erreur d’exécution se produit.

## <a name="remarks"></a>Notes

La valeur du délai d’attente peut être définie avant chaque opération effectuée par l’agent. Si une valeur de délai d’attente n’est pas spécifiée, l’agent définit la valeur du délai d’attente.

Pendant une opération d’énumération, la valeur du délai d’attente ne peut pas être réinitialisée pendant l’énumération de la ressource.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant démarre un processus de Calc.exe à l’aide de la méthode [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) de la classe de [**\_ processus WMI Win32**](/windows/desktop/CIMWin32Prov/win32-process) . Le paramètre *strInputParameters* contient les paramètres d’entrée au format XML. Le script spécifie un délai d’expiration pour la session.


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
    "wmi/root/cimv2/Win32_Process"

'Reset timeout to 10,000 milliseconds
objSession.Timeout = 10000     

strInputParameters = "<p:Create_INPUT " & _
    "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Process"">" & _
    "<p:CommandLine>" & "calc.exe" & _
    "</p:CommandLine>" & _
    "</p:Create_INPUT>"

strOutputParameters = objSession.Invoke( "Create", _
    strResource, strInputParameters )

DisplayOutput( strOutputParameters )

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**session**](session.md)
</dt> </dl>

 

