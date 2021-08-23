---
title: Objet ResourceLocator (WSManDisp. h)
description: Fournit le chemin d’accès à une ressource. Vous pouvez utiliser un objet ResourceLocator à la place d’un URI de ressource dans les opérations d’objet de session, telles que session. obtenir, session. put ou session. Enumerate.
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- objet ResourceLocator Windows Remote Management
- Windows Remote Management d’objets ResourceLocator, description
topic_type:
- apiref
api_name:
- ResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26d3287c02949326b672f550271ba3472e6cb16abb6748efb4a80de425c40e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642869"
---
# <a name="resourcelocator-object"></a>Objet ResourceLocator

Objet qui fournit le chemin d’accès à une ressource. Vous pouvez utiliser un objet **ResourceLocator** à la place d’un [*URI de ressource*](windows-remote-management-glossary.md) dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).

Cet objet vous permet d’effectuer les opérations suivantes :

-   Ajoutez un ou plusieurs [*sélecteurs*](windows-remote-management-glossary.md) identifiant une instance particulière d’une ressource. Cela revient à fournir une valeur de clé dans l’URI de ressource pour une ressource qui utilise des clés. Pour plus d’informations, consultez [**ResourceLocator. AddSelector**](resourcelocator-addselector.md). Vous pouvez effectuer une opération similaire à l’aide du paramètre *Filter* dans un appel à [**session. Enumerate**](session-enumerate.md).
-   Spécifiez un chemin d’accès de [*fragment*](windows-remote-management-glossary.md) et un dialecte pour obtenir une seule propriété d’une ressource. Vous pouvez également spécifier l’un ou l’ensemble des éléments d’une propriété de tableau en fournissant l’index de tableau. Pour plus d’informations, consultez [**ResourceLocator. FragmentPath**](resourcelocator-fragmentpath.md).
-   Ajoutez une ou plusieurs [*options*](windows-remote-management-glossary.md) qu’une source de données peut nécessiter pour traiter une demande. Pour plus d’informations, consultez [**ResourceLocator. AddOption**](resourcelocator-addoption.md).

Pour plus d’informations, consultez [interrogation d’instances spécifiques d’une ressource](querying-for-specific-instances-of-a-resource.md).

## <a name="members"></a>Membres

L’objet **ResourceLocator** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **ResourceLocator** a ces méthodes.



| Méthode                                                   | Description                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddOption**](resourcelocator-addoption.md)           | Ajoute les données supplémentaires requises pour traiter la demande.<br/>                                                                   |
| [**AddSelector**](resourcelocator-addselector.md)       | Ajoute un [*Sélecteur*](windows-remote-management-glossary.md) à l’objet **ResourceLocator** .<br/>     |
| [**ClearOptions**](resourcelocator-clearoptions.md)     | Supprime toutes les [*options*](windows-remote-management-glossary.md) de l’objet **ResourceLocator** .<br/> |
| [**ClearSelectors**](resourcelocator-clearselectors.md) | Supprime tous les sélecteurs d’un objet **ResourceLocator** .<br/>                                                            |



 

### <a name="properties"></a>Propriétés

L’objet **ResourceLocator** a ces propriétés.



| Propriété                                                                          | Type d’accès           | Description                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FragmentDialect**](resourcelocator-fragmentdialect.md)<br/>             | Lecture/écriture<br/> | Obtient ou définit le dialecte du langage pour un [*fragment*](windows-remote-management-glossary.md)de [*ressource*](windows-remote-management-glossary.md) .<br/> |
| [**FragmentPath**](resourcelocator-fragmentpath.md)<br/>                   | Lecture/écriture<br/> | Obtient ou définit le chemin d’accès d’un [*fragment*](windows-remote-management-glossary.md) ou d’une propriété de [*ressource*](windows-remote-management-glossary.md) .<br/> |
| [**MustUnderstandOptions**](resourcelocator-mustunderstandoptions.md)<br/> | Lecture/écriture<br/> | Obtient ou définit la valeur **MustUnderstandOptions** de l’objet **ResourceLocator** .<br/>                                                                                                         |
| [**URI**](resourcelocator-resourceuri.md)<br/>                     | Lecture/écriture<br/> | Obtient ou définit l' [*URI de ressource*](windows-remote-management-glossary.md) dans un objet **ResourceLocator** .<br/>                                                          |



 

## <a name="remarks"></a>Remarques

L’objet **ResourceLocator** correspond à l’interface **IWSManResourceLocator** .

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant obtient les propriétés **NumberOfLogicalProcessors** et **NumberOfCores** à partir d’une instance spécifique du [**\_ processeur Win32**](/windows/desktop/CIMWin32Prov/win32-processor).


```VB
Option Explicit
Dim strUri
strUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
    & "wmi/root/cimv2/Win32_Processor"
Const FragmentDialect = _
    "https://www.w3.org/TR/1999/REC-xpath-19991116"

Dim WSMan
Set WSMan = CreateObject("WSMan.Automation")

Dim Session
Set Session = WSMan.CreateSession

Dim Locator
Set Locator = WSMan.CreateResourceLocator(strUri)

Locator.AddSelector "DeviceID", "CPU0"

Dim NumberOfCores_XML
Locator.FragmentPath = "NumberOfCores"
Locator.FragmentDialect = FragmentDialect
NumberOfCores_XML = Session.Get(Locator)
DisplayOutput NumberOfCores_XML

Dim NumberOfLogicalProcessors_XML
Locator.FragmentPath = "NumberOfLogicalProcessors"
Locator.FragmentDialect = FragmentDialect
NumberOfLogicalProcessors_XML = Session.Get(Locator)

DisplayOutput NumberOfLogicalProcessors_XML

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
</dt> </dl>

 

