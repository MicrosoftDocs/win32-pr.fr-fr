---
title: Session. Invoke, méthode (WSManDisp. h)
description: Invoque une méthode et retourne les résultats de l'appel de la méthode.
ms.assetid: c83d0631-2efb-47d9-abcf-ab0c8de06c36
ms.tgt_platform: multiple
keywords:
- appeler la méthode Windows Remote Management
- méthode Invoke Windows Remote Management, objet Session
- Windows Remote Management d’objet de Session, méthode Invoke
topic_type:
- apiref
api_name:
- Session.Invoke
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2afa20390890c53a7362d776c1df7c84d0a638e7fcb10269c901d194a50dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743250"
---
# <a name="sessioninvoke-method"></a>Session. Invoke, méthode

Invoque une méthode et retourne les résultats de l'appel de la méthode.

## <a name="syntax"></a>Syntaxe


```VB
Session.Invoke( _
  ByVal actionUri, _
  ByVal resourceUri, _
  ByVal parameters, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*actionUri* \[ dans\]
</dt> <dd>

URI de la méthode à appeler.

</dd> <dt>

*resourceuri* \[ dans\]
</dt> <dd>

Identificateur de la ressource à récupérer.

Ce paramètre peut contenir l’un des éléments suivants :

-   URI avec ou sans [*sélecteurs*](windows-remote-management-glossary.md). dans l’exemple VBScript (Visual Basic scripting Edition) suivant, la clé est spécifiée par `Win32_Service?Name=winmgmt` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _ 
       & "Win32_Service?Name=winmgmt"
    ```

    

-   Objet [**ResourceLocator**](resourcelocator.md) qui peut contenir des sélecteurs, des [*fragments*](windows-remote-management-glossary.md)ou des [*options*](windows-remote-management-glossary.md).
-   Référence du point de terminaison [*WS-Addressing*](windows-remote-management-glossary.md) , comme décrit dans la norme [protocole WS-Management](ws-management-protocol.md) . Pour plus d’informations sur la spécification publique du protocole WS-Management, consultez la [page index des spécifications de gestion](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*paramètres* \[ dans\]
</dt> <dd>

Représentation XML de l’entrée de la méthode. Cette chaîne doit être fournie, sinon cette méthode échouera.

</dd> <dt>

*indicateurs* \[ dans, facultatif\]
</dt> <dd>

Réservé. Doit avoir la valeur 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Représentation XML de la sortie de la méthode.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant démarre un processus de Calc.exe. Le paramètre *strInputParameters* contient les paramètres d’entrée au format XML. Le seul paramètre d’entrée requis pour la méthode [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) de la classe [**\_ Process WMI Win32**](/windows/desktop/CIMWin32Prov/win32-process) est la ligne de commande à exécuter.


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



L’exemple de code VBScript suivant appelle la méthode **session. Invoke** pour exécuter la méthode [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) du [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service). La méthode **StopService** n’a pas de paramètres d’entrée. Toutefois, la méthode **Invoke** requiert une chaîne XML dans le paramètre *Parameters* .


```VB
Option Explicit

Dim objWsman
Dim objSession
Dim strResponse
Dim strActionURI
Dim strInputXml
Dim strResourceURI
Dim strMethodName

set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession
strResourceURI = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=w32time"
strMethodName = "StopService"
strActionURI = strMethodName                                      

strInputXml = "<p:StopService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"

strResponse = objSession.Invoke(strMethodName, strResourceURI, strInputXml)

call DisplayOutput(strResponse)
 
strMethodName = "StartService" 
strActionURI = strResourceURI & "/" & strMethodName  
strInputXml = "<p:StartService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"
strResponse = objSession.Invoke(strMethodName, _
    strResourceURI, strInputXml)

call DisplayOutput(strResponse)

 
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

 

