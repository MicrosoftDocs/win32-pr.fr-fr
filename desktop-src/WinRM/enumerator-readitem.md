---
title: Enumerator. ReadItem, méthode (WSManDisp. h)
description: Récupère un élément de la ressource et retourne une représentation XML de l’élément.
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode ReadItem
- Méthode ReadItem Windows Remote Management, objet Enumerator
- Objet Enumerator Windows Remote Management, méthode ReadItem
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fda1b31cbc14d4a7474d4de55b572df82a8aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032632"
---
# <a name="enumeratorreaditem-method"></a>Enumerator. ReadItem, méthode

Récupère un élément de la ressource et retourne une représentation XML de l’élément.

## <a name="syntax"></a>Syntaxe


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*resource* 
</dt> <dd>

URI de l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Représentation XML de l’élément.

## <a name="remarks"></a>Notes

Pour limiter le nombre d’éléments lus, définissez la propriété [**Session.BatchItems**](session-batchitems.md) .

Notez que la libération de l’objet d’énumération nettoie toutes les demandes d’énumération en attente.

La méthode [**session. Enumerate**](session-enumerate.md) n’obtient pas de collection de la même façon qu’une [requête WMI](/windows/desktop/WmiSdk/querying-wmi), telle que `SELECT * from Win32_LogicalDisk` , retourne une collection dans une [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset). Pour lire un fichier en tant que flux de texte, vous créez l’objet [TextStream](/previous-versions//312a5kbt(v=vs.85)) de script et appelez la méthode [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) pour lire chaque ligne du fichier. De la même façon, vous appelez la méthode **session. Enumerate** pour obtenir un objet [**énumérateur**](enumerator.md) , puis vous appelez la méthode **Enumerator. ReadItem** . Comme pour la lecture à partir du fichier texte, vous pouvez vérifier la propriété [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) pour vérifier si vous avez atteint la fin des éléments de données.

## <a name="examples"></a>Exemples

L’exemple VBScript suivant appelle la méthode [**session. Enumerate**](session-enumerate.md) pour obtenir une liste de tâches planifiées. La sous-routine DisplayOutput utilise le fichier de transformation XML (WsmTxt. Xsl) de l’outil en ligne de commande WinRM pour générer les données sous forme de tableau.


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

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

[**Énumérateur**](enumerator.md)
</dt> <dt>

[Énumération ou liste de toutes les instances d’une ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

