---
title: Enumerator. AtEndOfStream, propriété (WSManDisp. h)
description: Obtient une valeur booléenne qui indique s’il y a plus d’éléments dans la collection.
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la propriété AtEndOfStream
- Propriété AtEndOfStream Windows Remote Management, objet Enumerator
- Objet Enumerator Windows Remote Management, propriété AtEndOfStream
topic_type:
- apiref
api_name:
- Enumerator.AtEndOfStream
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023798f6c868e434218dd1a4dbdf1928bf4526a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103265"
---
# <a name="enumeratoratendofstream-property"></a>Enumerator. AtEndOfStream, propriété

Obtient une valeur booléenne qui indique s’il y a plus d’éléments dans la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a>Valeur de la propriété

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**:**


</dt> <dd>

Il n’y a plus d’éléments dans la collection.

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**Fausses**


</dt> <dd>

D’autres éléments sont disponibles.

</dd> </dl>

## <a name="remarks"></a>Notes

Si vous libérez l’objet [**énumérateur**](enumerator.md) après avoir obtenu toutes les données requises, toutes les demandes d’énumération en attente sont supprimées. Pour plus d’informations, consultez [énumération ou liste de toutes les instances d’une ressource](enumerating-or-listing-all-instances-of-a-resource.md).

## <a name="examples"></a>Exemples

L’exemple VBScript suivant énumère les instances du système d’exploitation. Notez que la libération de l’objet d’énumération nettoie toutes les demandes d’énumération en attente. La sous-routine DisplayOutput met en forme la sortie des données de la même façon que l’outil WinRM. cmd.


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
    "wmi/root/cimv2/Win32_OperatingSystem"

Set objResultSet = objSession.Enumerate( strResource )

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

[**Énumérateur**](enumerator.md)
</dt> <dt>

[Énumération ou liste de toutes les instances d’une ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





