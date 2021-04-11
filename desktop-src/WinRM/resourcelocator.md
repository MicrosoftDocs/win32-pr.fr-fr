---
title: Objet ResourceLocator (WSManDisp. h)
description: Fournit le chemin d’accès à une ressource. Vous pouvez utiliser un objet ResourceLocator à la place d’un URI de ressource dans les opérations d’objet de session, telles que session. obtenir, session. put ou session. Enumerate.
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- Objet ResourceLocator Windows Remote Management
- Windows Remote Management d’objets ResourceLocator, Description
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
ms.openlocfilehash: cd110b94d3174134e6410428843de76e809d5e22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103077"
---
# <a name="resourcelocator-object"></a><span data-ttu-id="d6c01-106">Objet ResourceLocator</span><span class="sxs-lookup"><span data-stu-id="d6c01-106">ResourceLocator object</span></span>

<span data-ttu-id="d6c01-107">Objet qui fournit le chemin d’accès à une ressource.</span><span class="sxs-lookup"><span data-stu-id="d6c01-107">An object that supplies the path to a resource.</span></span> <span data-ttu-id="d6c01-108">Vous pouvez utiliser un objet **ResourceLocator** à la place d’un [*URI de ressource*](windows-remote-management-glossary.md) dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="d6c01-108">You can use a **ResourceLocator** object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="d6c01-109">Cet objet vous permet d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6c01-109">This object enables you to:</span></span>

-   <span data-ttu-id="d6c01-110">Ajoutez un ou plusieurs [*sélecteurs*](windows-remote-management-glossary.md) identifiant une instance particulière d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="d6c01-110">Add one or more [*selectors*](windows-remote-management-glossary.md) that identify a particular instance of a resource.</span></span> <span data-ttu-id="d6c01-111">Cela revient à fournir une valeur de clé dans l’URI de ressource pour une ressource qui utilise des clés.</span><span class="sxs-lookup"><span data-stu-id="d6c01-111">This is the same as supplying a key value in the resource URI for a resource that uses keys.</span></span> <span data-ttu-id="d6c01-112">Pour plus d’informations, consultez [**ResourceLocator. AddSelector**](resourcelocator-addselector.md).</span><span class="sxs-lookup"><span data-stu-id="d6c01-112">For more information, see [**ResourceLocator.AddSelector**](resourcelocator-addselector.md).</span></span> <span data-ttu-id="d6c01-113">Vous pouvez effectuer une opération similaire à l’aide du paramètre *Filter* dans un appel à [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="d6c01-113">You can do a similar operation using the *filter* parameter in a call to [**Session.Enumerate**](session-enumerate.md).</span></span>
-   <span data-ttu-id="d6c01-114">Spécifiez un chemin d’accès de [*fragment*](windows-remote-management-glossary.md) et un dialecte pour obtenir une seule propriété d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="d6c01-114">Specify a [*fragment*](windows-remote-management-glossary.md) path and dialect to get only one property of a resource.</span></span> <span data-ttu-id="d6c01-115">Vous pouvez également spécifier l’un ou l’ensemble des éléments d’une propriété de tableau en fournissant l’index de tableau.</span><span class="sxs-lookup"><span data-stu-id="d6c01-115">You can also specify one or all of the elements of an array property by supplying the array index.</span></span> <span data-ttu-id="d6c01-116">Pour plus d’informations, consultez [**ResourceLocator. FragmentPath**](resourcelocator-fragmentpath.md).</span><span class="sxs-lookup"><span data-stu-id="d6c01-116">For more information, see [**ResourceLocator.FragmentPath**](resourcelocator-fragmentpath.md).</span></span>
-   <span data-ttu-id="d6c01-117">Ajoutez une ou plusieurs [*options*](windows-remote-management-glossary.md) qu’une source de données peut nécessiter pour traiter une demande.</span><span class="sxs-lookup"><span data-stu-id="d6c01-117">Add one or more [*options*](windows-remote-management-glossary.md) that a data source may require to process a request.</span></span> <span data-ttu-id="d6c01-118">Pour plus d’informations, consultez [**ResourceLocator. AddOption**](resourcelocator-addoption.md).</span><span class="sxs-lookup"><span data-stu-id="d6c01-118">For more information, see [**ResourceLocator.AddOption**](resourcelocator-addoption.md).</span></span>

<span data-ttu-id="d6c01-119">Pour plus d’informations, consultez [interrogation d’instances spécifiques d’une ressource](querying-for-specific-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="d6c01-119">For more information, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

## <a name="members"></a><span data-ttu-id="d6c01-120">Membres</span><span class="sxs-lookup"><span data-stu-id="d6c01-120">Members</span></span>

<span data-ttu-id="d6c01-121">L’objet **ResourceLocator** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d6c01-121">The **ResourceLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="d6c01-122">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d6c01-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="d6c01-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d6c01-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d6c01-124">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d6c01-124">Methods</span></span>

<span data-ttu-id="d6c01-125">L’objet **ResourceLocator** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d6c01-125">The **ResourceLocator** object has these methods.</span></span>



| <span data-ttu-id="d6c01-126">Méthode</span><span class="sxs-lookup"><span data-stu-id="d6c01-126">Method</span></span>                                                   | <span data-ttu-id="d6c01-127">Description</span><span class="sxs-lookup"><span data-stu-id="d6c01-127">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6c01-128">**AddOption**</span><span class="sxs-lookup"><span data-stu-id="d6c01-128">**AddOption**</span></span>](resourcelocator-addoption.md)           | <span data-ttu-id="d6c01-129">Ajoute les données supplémentaires requises pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="d6c01-129">Adds additional data required to process the request.</span></span><br/>                                                                   |
| [<span data-ttu-id="d6c01-130">**AddSelector**</span><span class="sxs-lookup"><span data-stu-id="d6c01-130">**AddSelector**</span></span>](resourcelocator-addselector.md)       | <span data-ttu-id="d6c01-131">Ajoute un [*Sélecteur*](windows-remote-management-glossary.md) à l’objet **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="d6c01-131">Adds a [*selector*](windows-remote-management-glossary.md) to the **ResourceLocator** object.</span></span><br/>     |
| [<span data-ttu-id="d6c01-132">**ClearOptions**</span><span class="sxs-lookup"><span data-stu-id="d6c01-132">**ClearOptions**</span></span>](resourcelocator-clearoptions.md)     | <span data-ttu-id="d6c01-133">Supprime toutes les [*options*](windows-remote-management-glossary.md) de l’objet **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="d6c01-133">Removes any [*options*](windows-remote-management-glossary.md) from the **ResourceLocator** object.</span></span><br/> |
| [<span data-ttu-id="d6c01-134">**ClearSelectors**</span><span class="sxs-lookup"><span data-stu-id="d6c01-134">**ClearSelectors**</span></span>](resourcelocator-clearselectors.md) | <span data-ttu-id="d6c01-135">Supprime tous les sélecteurs d’un objet **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="d6c01-135">Removes all the selectors from a **ResourceLocator** object.</span></span><br/>                                                            |



 

### <a name="properties"></a><span data-ttu-id="d6c01-136">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d6c01-136">Properties</span></span>

<span data-ttu-id="d6c01-137">L’objet **ResourceLocator** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d6c01-137">The **ResourceLocator** object has these properties.</span></span>



| <span data-ttu-id="d6c01-138">Propriété</span><span class="sxs-lookup"><span data-stu-id="d6c01-138">Property</span></span>                                                                          | <span data-ttu-id="d6c01-139">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="d6c01-139">Access type</span></span>           | <span data-ttu-id="d6c01-140">Description</span><span class="sxs-lookup"><span data-stu-id="d6c01-140">Description</span></span>                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6c01-141">**FragmentDialect**</span><span class="sxs-lookup"><span data-stu-id="d6c01-141">**FragmentDialect**</span></span>](resourcelocator-fragmentdialect.md)<br/>             | <span data-ttu-id="d6c01-142">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d6c01-142">Read/write</span></span><br/> | <span data-ttu-id="d6c01-143">Obtient ou définit le dialecte du langage pour un [*fragment*](windows-remote-management-glossary.md)de [*ressource*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="d6c01-143">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md).</span></span><br/> |
| [<span data-ttu-id="d6c01-144">**FragmentPath**</span><span class="sxs-lookup"><span data-stu-id="d6c01-144">**FragmentPath**</span></span>](resourcelocator-fragmentpath.md)<br/>                   | <span data-ttu-id="d6c01-145">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d6c01-145">Read/write</span></span><br/> | <span data-ttu-id="d6c01-146">Obtient ou définit le chemin d’accès d’un [*fragment*](windows-remote-management-glossary.md) ou d’une propriété de [*ressource*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="d6c01-146">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property.</span></span><br/> |
| [<span data-ttu-id="d6c01-147">**MustUnderstandOptions**</span><span class="sxs-lookup"><span data-stu-id="d6c01-147">**MustUnderstandOptions**</span></span>](resourcelocator-mustunderstandoptions.md)<br/> | <span data-ttu-id="d6c01-148">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d6c01-148">Read/write</span></span><br/> | <span data-ttu-id="d6c01-149">Obtient ou définit la valeur **MustUnderstandOptions** de l’objet **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="d6c01-149">Gets or sets the **MustUnderstandOptions** value for the **ResourceLocator** object.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="d6c01-150">**URI**</span><span class="sxs-lookup"><span data-stu-id="d6c01-150">**ResourceURI**</span></span>](resourcelocator-resourceuri.md)<br/>                     | <span data-ttu-id="d6c01-151">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d6c01-151">Read/write</span></span><br/> | <span data-ttu-id="d6c01-152">Obtient ou définit l' [*URI de ressource*](windows-remote-management-glossary.md) dans un objet **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="d6c01-152">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a **ResourceLocator** object.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="d6c01-153">Notes</span><span class="sxs-lookup"><span data-stu-id="d6c01-153">Remarks</span></span>

<span data-ttu-id="d6c01-154">L’objet **ResourceLocator** correspond à l’interface **IWSManResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="d6c01-154">The **ResourceLocator** object corresponds to the **IWSManResourceLocator** interface.</span></span>

## <a name="examples"></a><span data-ttu-id="d6c01-155">Exemples</span><span class="sxs-lookup"><span data-stu-id="d6c01-155">Examples</span></span>

<span data-ttu-id="d6c01-156">L’exemple de code VBScript suivant obtient les propriétés **NumberOfLogicalProcessors** et **NumberOfCores** à partir d’une instance spécifique du [**\_ processeur Win32**](/windows/desktop/CIMWin32Prov/win32-processor).</span><span class="sxs-lookup"><span data-stu-id="d6c01-156">The following VBScript code example obtains the **NumberOfLogicalProcessors** and **NumberOfCores** properties from a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d6c01-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6c01-157">Requirements</span></span>



| <span data-ttu-id="d6c01-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6c01-158">Requirement</span></span> | <span data-ttu-id="d6c01-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6c01-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c01-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6c01-160">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c01-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6c01-161">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d6c01-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6c01-162">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c01-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6c01-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d6c01-164">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6c01-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6c01-165"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6c01-165"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6c01-166">MIDL</span><span class="sxs-lookup"><span data-stu-id="d6c01-166">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6c01-167"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6c01-167"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="d6c01-168">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d6c01-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6c01-169"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d6c01-169"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d6c01-170">DLL</span><span class="sxs-lookup"><span data-stu-id="d6c01-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6c01-171"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6c01-171"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d6c01-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6c01-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c01-173">API de script WinRM</span><span class="sxs-lookup"><span data-stu-id="d6c01-173">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> </dl>

 

