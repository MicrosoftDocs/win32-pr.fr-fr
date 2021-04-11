---
title: Session. put, méthode (WSManDisp. h)
description: Met à jour une ressource.
ms.assetid: f121d9ce-6aa3-45e3-b0ba-67b19c2f5665
ms.tgt_platform: multiple
keywords:
- Put, méthode Windows Remote Management
- Put, méthode Windows Remote Management, objet session
- Windows Remote Management d’objet de session, méthode put
topic_type:
- apiref
api_name:
- Session.Put
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0f09b0a0f8de4e7f7d06cb84753e6b708841f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384948"
---
# <a name="sessionput-method"></a>Session. put, méthode

Met à jour une ressource.

## <a name="syntax"></a>Syntaxe


```VB
Session.Put( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*resourceuri* \[ dans\]
</dt> <dd>

Identificateur de la ressource à mettre à jour.

Ce paramètre peut contenir l’un des éléments contenus dans la liste suivante :

-   URI avec ou sans [*sélecteurs*](windows-remote-management-glossary.md). Quand vous appelez la méthode **put** pour obtenir une ressource WMI, utilisez la ou les propriétés de clé de l’objet. Par exemple, dans l’exemple de code Visual Basic Scripting Edition (VBScript) suivant, la clé est spécifiée par `Win32_Service?Name=winmgmt` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   Objet [**ResourceLocator**](resourcelocator.md) qui peut contenir des sélecteurs, des [*fragments*](windows-remote-management-glossary.md)ou des [*options*](windows-remote-management-glossary.md).
-   Référence du point de terminaison [*WS-Addressing*](windows-remote-management-glossary.md) , comme décrit dans la norme [protocole WS-Management](ws-management-protocol.md) . Pour plus d’informations sur la spécification publique du protocole WS-Management, consultez la [page index des spécifications de gestion](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*ressource* \[ dans\]
</dt> <dd>

Contenu de la ressource mise à jour.

</dd> <dt>

*indicateurs* \[ dans, facultatif\]
</dt> <dd>

Réservé. Doit avoir la valeur 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

XML qui contient le contenu de la ressource mis à jour.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant écrit des données dans l’objet [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) . Vous devez inclure toutes les propriétés non-tableau de l’objet dans le XML du paramètre de *ressource* . L’ordre des propriétés n’est pas significatif.


```VB

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

'Change the property value by putting
'the new XML content into the resource.
Dim strResourceUri, strReturnedResourceUri, newXmlContent
strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
  & "wmi/root/cimv2/Win32_WMISetting"
newXmlContent = _
  "<p:Win32_WMISetting xmlns:p=""http://schemas.microsoft.com/" & _
  "wbem/wsman/1/wmi/root/cimv2/Win32_WMISetting"">" & _
  "<p:LoggingLevel>2</p:LoggingLevel></p:Win32_WMISetting>" 

On Error Resume Next
strReturnedResourceUri = objSession.Put(reourceUri, newXmlContent)
WScript.Echo "Returned resource Uri:" & Chr(10) & _
  strReturnedResourceUri
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
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

 

