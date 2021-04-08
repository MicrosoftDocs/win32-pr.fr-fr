---
title: Objet Enumerator (WSManDisp. h)
description: Représente un flux de résultats retourné par des opérations, telles qu’une opération d’extraction.
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- Objet énumérateur Windows Remote Management
- Objet énumérateur Windows Remote Management, décrit
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
ms.openlocfilehash: 6ad2395ae0ba17b1f221cd0a6dc0f7517a89db71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033178"
---
# <a name="enumerator-object"></a><span data-ttu-id="2f734-105">Enumerator (objet)</span><span class="sxs-lookup"><span data-stu-id="2f734-105">Enumerator object</span></span>

<span data-ttu-id="2f734-106">Représente un flux de résultats retourné par des opérations, telles qu’une opération d’extraction.</span><span class="sxs-lookup"><span data-stu-id="2f734-106">Represents a stream of results returned from operations, such as a Pull operation.</span></span> <span data-ttu-id="2f734-107">Par exemple, la méthode [**session. Enumerate**](session-enumerate.md) retourne plusieurs résultats.</span><span class="sxs-lookup"><span data-stu-id="2f734-107">For example, the [**Session.Enumerate**](session-enumerate.md) method returns multiple results.</span></span>

## <a name="members"></a><span data-ttu-id="2f734-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2f734-108">Members</span></span>

<span data-ttu-id="2f734-109">L’objet **énumérateur** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2f734-109">The **Enumerator** object has these types of members:</span></span>

-   [<span data-ttu-id="2f734-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2f734-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="2f734-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2f734-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2f734-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2f734-112">Methods</span></span>

<span data-ttu-id="2f734-113">L’objet **énumérateur** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2f734-113">The **Enumerator** object has these methods.</span></span>



| <span data-ttu-id="2f734-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="2f734-114">Method</span></span>                                  | <span data-ttu-id="2f734-115">Description</span><span class="sxs-lookup"><span data-stu-id="2f734-115">Description</span></span>                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f734-116">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="2f734-116">**ReadItem**</span></span>](enumerator-readitem.md) | <span data-ttu-id="2f734-117">Récupère un élément de la ressource et retourne une représentation XML de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2f734-117">Retrieves an item from the resource and returns an XML representation of the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2f734-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2f734-118">Properties</span></span>

<span data-ttu-id="2f734-119">L’objet **énumérateur** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2f734-119">The **Enumerator** object has these properties.</span></span>



| <span data-ttu-id="2f734-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="2f734-120">Property</span></span>                                                     | <span data-ttu-id="2f734-121">Description</span><span class="sxs-lookup"><span data-stu-id="2f734-121">Description</span></span>                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f734-122">**AtEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="2f734-122">**AtEndOfStream**</span></span>](enumerator-atendofstream.md)<br/> | <span data-ttu-id="2f734-123">Obtient une valeur booléenne qui indique s’il y a plus d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="2f734-123">Gets a Boolean value that indicates whether there are more items in the collection.</span></span><br/> |
| [<span data-ttu-id="2f734-124">**Error**</span><span class="sxs-lookup"><span data-stu-id="2f734-124">**Error**</span></span>](enumerator-error.md)<br/>                 | <span data-ttu-id="2f734-125">Obtient une représentation XML des informations d’erreur supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2f734-125">Gets an XML representation of additional error information.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="2f734-126">Notes</span><span class="sxs-lookup"><span data-stu-id="2f734-126">Remarks</span></span>

<span data-ttu-id="2f734-127">Pour démarrer une énumération, utilisez [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="2f734-127">To start an enumeration, use [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="2f734-128">Pour effectuer une opération [*WS-Enumeration :*](windows-remote-management-glossary.md)[*pull*](windows-remote-management-glossary.md) qui poursuit la lecture des éléments dans l’énumération, utilisez [**Enumerator. ReadItem**](enumerator-readitem.md).</span><span class="sxs-lookup"><span data-stu-id="2f734-128">To do a [*WS-Enumeration:*](windows-remote-management-glossary.md)[*Pull*](windows-remote-management-glossary.md) operation that continues reading items in the enumeration, use [**Enumerator.ReadItem**](enumerator-readitem.md).</span></span>

<span data-ttu-id="2f734-129">L’objet **énumérateur** correspond à l’interface [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) .</span><span class="sxs-lookup"><span data-stu-id="2f734-129">The **Enumerator** object corresponds to the [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="2f734-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="2f734-130">Examples</span></span>

<span data-ttu-id="2f734-131">L’exemple de code VBScript suivant énumère tous les disques sur un ordinateur distant spécifié par le nom de domaine complet (servername.domain.com).</span><span class="sxs-lookup"><span data-stu-id="2f734-131">The following VBScript code example enumerates all the disks on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="2f734-132">La sous-routine DisplayOutput met en forme la sortie des données de la même façon que l’outil WinRM. cmd.</span><span class="sxs-lookup"><span data-stu-id="2f734-132">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2f734-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f734-133">Requirements</span></span>



| <span data-ttu-id="2f734-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f734-134">Requirement</span></span> | <span data-ttu-id="2f734-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f734-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f734-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f734-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2f734-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f734-137">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2f734-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f734-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2f734-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f734-139">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2f734-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f734-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f734-141"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f734-141"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f734-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="2f734-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f734-143"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f734-143"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2f734-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2f734-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f734-145"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2f734-145"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2f734-146">DLL</span><span class="sxs-lookup"><span data-stu-id="2f734-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f734-147"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f734-147"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f734-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f734-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f734-149">API de script WinRM</span><span class="sxs-lookup"><span data-stu-id="2f734-149">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="2f734-150">Énumération ou liste de toutes les instances d’une ressource</span><span class="sxs-lookup"><span data-stu-id="2f734-150">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="2f734-151">Scripts dans Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="2f734-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





