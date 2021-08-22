---
title: Session. obten, méthode (WSManDisp. h)
description: Récupère la ressource spécifiée par l’URI et retourne une représentation XML de l’instance actuelle de la ressource.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- méthode d’extraction Windows Remote Management
- méthode d’extraction Windows Remote Management, objet Session
- Windows Remote Management d’objet de Session, méthode d’extraction
topic_type:
- apiref
api_name:
- Session.Get
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c983c5f95ddfa3acc88b85b383ec85ddf85f885293031fe9bc4e4e07c90850a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642559"
---
# <a name="sessionget-method"></a>Session. obten, méthode

Récupère la ressource spécifiée par l' [*URI*](windows-remote-management-glossary.md) et retourne une représentation XML de l’instance actuelle de la ressource.

## <a name="syntax"></a>Syntaxe


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*resourceuri* \[ dans\]
</dt> <dd>

Identificateur de la ressource à récupérer.

Ce paramètre peut contenir l’un des éléments suivants :

-   URI avec ou sans [*sélecteurs*](windows-remote-management-glossary.md). Quand vous appelez la méthode **obtenir** avec un sélecteur pour obtenir une ressource WMI, utilisez la ou les propriétés de clé de l’objet. par exemple, dans l’exemple de code VBScript (Visual Basic scripting Edition) suivant, la clé est spécifiée par `Win32_Service?Name=winmgmt` . Pour les classes Singleton, telles que [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), vous ne pouvez pas utiliser de sélecteur.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   Objet [**ResourceLocator**](resourcelocator.md) qui peut contenir des sélecteurs, des [*fragments*](windows-remote-management-glossary.md)ou des [*options*](windows-remote-management-glossary.md).
-   Une référence de point de terminaison [*WS-Addressing*](windows-remote-management-glossary.md) , comme décrit dans la norme de protocole WS-Management. Pour plus d’informations sur la spécification publique pour [protocole WS-Management](ws-management-protocol.md), consultez la [page index des spécifications de gestion](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*indicateurs* \[ dans, facultatif\]
</dt> <dd>

Réservé. Doit avoir la valeur 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Représentation XML de la ressource.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant récupère la représentation XML de l’instance de [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) qui représente le service WinMgmt WMI sur l’ordinateur local.


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


strResourceUri = "http://schemas.microsoft.com/" _ 
    & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
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



L’exemple de code VBScript suivant récupère l’instance de service WinMgmt WMI à partir d’un ordinateur distant. L’ordinateur distant est identifié par le nom de domaine complet (servername.domain.com). La seule différence entre la version locale et la version distante est la spécification de l’ordinateur distant dans l’appel à [**WSMan. CreateSession**](wsman-createsession.md).


```VB
Const RemoteComputer = "servername.domain.com"

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Dim objSession
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/" _ 
    & "Win32_Service?Name=winmgmt"


On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
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

[**Session**](session.md)
</dt> </dl>

 

