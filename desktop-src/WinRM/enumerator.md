---
title: Objet Enumerator (WSManDisp. h)
description: Représente un flux de résultats retourné par des opérations, telles qu’une opération d’extraction.
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- objet énumérateur Windows Remote Management
- objet énumérateur Windows Remote Management, décrit
topic_type:
- apiref
api_name:
- Enumerator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83799c4c67ad0b0f7c1ad89c77c3abab5989f1231508757c47dfe4c1705d7e20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051827"
---
# <a name="enumerator-object"></a>Enumerator (objet)

Représente un flux de résultats retourné par des opérations, telles qu’une opération d’extraction. Par exemple, la méthode [**session. Enumerate**](session-enumerate.md) retourne plusieurs résultats.

## <a name="members"></a>Membres

L’objet **énumérateur** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **énumérateur** possède ces méthodes.



| Méthode                                  | Description                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ReadItem**](enumerator-readitem.md) | Récupère un élément de la ressource et retourne une représentation XML de l’élément.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **énumérateur** a ces propriétés.



| Propriété                                                     | Description                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**AtEndOfStream**](enumerator-atendofstream.md)<br/> | Obtient une valeur booléenne qui indique s’il y a plus d’éléments dans la collection.<br/> |
| [**Erreur**](enumerator-error.md)<br/>                 | Obtient une représentation XML des informations d’erreur supplémentaires.<br/>                         |



 

## <a name="remarks"></a>Remarques

Pour démarrer une énumération, utilisez [**session. Enumerate**](session-enumerate.md). Pour effectuer une opération [*WS-Enumeration :*](windows-remote-management-glossary.md)[*pull*](windows-remote-management-glossary.md) qui poursuit la lecture des éléments dans l’énumération, utilisez [**Enumerator. ReadItem**](enumerator-readitem.md).

L’objet **énumérateur** correspond à l’interface [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) .

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant énumère tous les disques sur un ordinateur distant spécifié par le nom de domaine complet (servername.domain.com). La sous-routine DisplayOutput met en forme la sortie des données de la même façon que l’outil WinRM. cmd.


```VB
Option Explicit

Const RemoteComputer = "MIG50-64D.mig.net"

Dim objWsman, objSession, strResource
Dim objResultSet

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" _
    & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" _
     & "wmi/root/cimv2/Win32_OperatingSystem"
Dim iFlag
iFlag = objWsman.EnumerationFlagReturnObjectAndEPR or _
    objWsman.EnumerationFlagHierarchyDeep
Set objResultSet = _
    objSession.Enumerate( strResource, "", "",  iFlag)
While Not objResultSet.AtEndOfStream
    DisplayOutput( objResultSet.ReadItem ) 
Wend


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

[API de script WinRM](winrm-scripting-api.md)
</dt> <dt>

[Énumération ou liste de toutes les instances d’une ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[scripts dans Windows Remote Management](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





