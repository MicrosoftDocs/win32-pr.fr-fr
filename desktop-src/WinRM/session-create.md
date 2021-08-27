---
title: Session. Create, méthode (WSManDisp. h)
description: Crée une nouvelle instance d’une ressource et retourne la référence de point de terminaison (EPR) du nouvel objet.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- créer une méthode Windows Remote Management
- create method Windows Remote Management, objet Session
- Windows Remote Management d’objet de Session, méthode create
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97adac133adc4c636de395f564927a5f0194b3c52d50685ac034142e6c15aadf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823261"
---
# <a name="sessioncreate-method"></a>Session. Create, méthode

Crée une nouvelle instance d’une ressource et retourne la [*référence de point de terminaison (EPR)*](windows-remote-management-glossary.md) du nouvel objet.

## <a name="syntax"></a>Syntaxe


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*resourceuri* \[ dans\]
</dt> <dd>

Identificateur de la ressource à créer.

Ce paramètre peut contenir l’un des éléments suivants :

-   URI avec un ou plusieurs [*sélecteurs*](windows-remote-management-glossary.md). N’oubliez pas que le [*plug-in WMI*](windows-remote-management-glossary.md) ne prend pas en charge la création d’une ressource autre qu’un écouteur de [protocole WS-Management](ws-management-protocol.md) .
-   Objet [**ResourceLocator**](resourcelocator.md) qui peut contenir des sélecteurs, des [*fragments*](windows-remote-management-glossary.md)ou des [*options*](windows-remote-management-glossary.md).
-   Référence du point de terminaison [*WS-Addressing*](windows-remote-management-glossary.md) , comme décrit dans la norme du protocole WS-Management. Pour plus d’informations sur la spécification publique du protocole WS-Management, consultez la [page index des spécifications de gestion](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*resource* 
</dt> <dd>

XML qui contient le contenu des ressources.

</dd> <dt>

*indicateurs* \[ dans, facultatif\]
</dt> <dd>

Réservé. Doit avoir la valeur 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

EPR de la nouvelle ressource.

## <a name="remarks"></a>Remarques

**Session. Create** est utilisé uniquement pour créer des instances d’une ressource. Utilisez la méthode [**session. put**](session-put.md) pour mettre à jour les instances existantes d’une ressource. Une fois que vous avez obtenu le nouvel URI de ressource, vous pouvez appeler [**session. obtenir**](session-get.md) pour récupérer le nouvel objet. Le nouvel objet contient toutes les propriétés assignées par le fournisseur de ressources lors de la création du nouvel objet. Par exemple, si vous créez un [*écouteur*](windows-remote-management-glossary.md) de protocole WS-Management et que vous récupérez l’objet écouteur à l’aide de **session. obtenir**, vous obtenez également les propriétés **port**, **Enabled** et **ListeningOn** .

N’oubliez pas que le [*plug-in WMI*](windows-remote-management-glossary.md) ne prend pas en charge la création d’une ressource autre qu’un écouteur de protocole WS-Management.

La syntaxe suivante est utilisée pour appeler cette méthode.


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant appelle **session. Create** pour créer un écouteur sur l’ordinateur local.


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
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
</dt> <dt>

[Protocole Gestion des services web](ws-management-protocol.md)
</dt> </dl>

 

