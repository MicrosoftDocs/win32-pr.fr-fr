---
title: Session. Invoke, méthode (WSManDisp. h)
description: Invoque une méthode et retourne les résultats de l'appel de la méthode.
ms.assetid: c83d0631-2efb-47d9-abcf-ab0c8de06c36
ms.tgt_platform: multiple
keywords:
- Appeler la méthode Windows Remote Management
- Méthode Invoke Windows Remote Management, objet session
- Windows Remote Management d’objet de session, méthode Invoke
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
ms.openlocfilehash: 117c688b616f377730524a09234b1dc38a4996c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743221"
---
# <a name="sessioninvoke-method"></a><span data-ttu-id="c4bc2-106">Session. Invoke, méthode</span><span class="sxs-lookup"><span data-stu-id="c4bc2-106">Session.Invoke method</span></span>

<span data-ttu-id="c4bc2-107">Invoque une méthode et retourne les résultats de l'appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="c4bc2-107">Invokes a method and returns the results of the method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4bc2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4bc2-108">Syntax</span></span>


```VB
Session.Invoke( _
  ByVal actionUri, _
  ByVal resourceUri, _
  ByVal parameters, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c4bc2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4bc2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4bc2-110">*actionUri* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4bc2-110">*actionUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bc2-111">URI de la méthode à appeler.</span><span class="sxs-lookup"><span data-stu-id="c4bc2-111">The URI of the method to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="c4bc2-112">*resourceuri* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4bc2-112">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bc2-113">Identificateur de la ressource à récupérer.</span><span class="sxs-lookup"><span data-stu-id="c4bc2-113">The identifier of the resource to retrieve.</span></span>

<span data-ttu-id="c4bc2-114">Ce paramètre peut contenir l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c4bc2-114">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="c4bc2-115">URI avec ou sans [*sélecteurs*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c4bc2-115">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="c4bc2-116">Dans l’exemple de Visual Basic Scripting Edition (VBScript) suivant, la clé est spécifiée par `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="c4bc2-116">In the following Visual Basic Scripting Edition (VBScript) example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _ 
       & "Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="c4bc2-117">Objet [**ResourceLocator**](resourcelocator.md) qui peut contenir des sélecteurs, des [*fragments*](windows-remote-management-glossary.md)ou des [*options*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c4bc2-117">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="c4bc2-118">Référence du point de terminaison [*WS-Addressing*](windows-remote-management-glossary.md) , comme décrit dans la norme [protocole WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="c4bc2-118">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="c4bc2-119">Pour plus d’informations sur la spécification publique du protocole WS-Management, consultez la [page index des spécifications de gestion](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="c4bc2-119">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="c4bc2-120">*paramètres* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4bc2-120">*parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bc2-121">Représentation XML de l’entrée de la méthode.</span><span class="sxs-lookup"><span data-stu-id="c4bc2-121">The XML representation of the input for the method.</span></span> <span data-ttu-id="c4bc2-122">Cette chaîne doit être fournie, sinon cette méthode échouera.</span><span class="sxs-lookup"><span data-stu-id="c4bc2-122">This string must be supplied or this method will fail.</span></span>

</dd> <dt>

<span data-ttu-id="c4bc2-123">*indicateurs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c4bc2-123">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bc2-124">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c4bc2-124">Reserved.</span></span> <span data-ttu-id="c4bc2-125">Doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="c4bc2-125">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4bc2-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4bc2-126">Return value</span></span>

<span data-ttu-id="c4bc2-127">Représentation XML de la sortie de la méthode.</span><span class="sxs-lookup"><span data-stu-id="c4bc2-127">The XML representation of the method output.</span></span>

## <a name="examples"></a><span data-ttu-id="c4bc2-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="c4bc2-128">Examples</span></span>

<span data-ttu-id="c4bc2-129">L’exemple de code VBScript suivant démarre un processus de Calc.exe.</span><span class="sxs-lookup"><span data-stu-id="c4bc2-129">The following VBScript code example starts a Calc.exe process.</span></span> <span data-ttu-id="c4bc2-130">Le paramètre *strInputParameters* contient les paramètres d’entrée au format XML.</span><span class="sxs-lookup"><span data-stu-id="c4bc2-130">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="c4bc2-131">Le seul paramètre d’entrée requis pour la méthode [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) de la classe [**\_ Process WMI Win32**](/windows/desktop/CIMWin32Prov/win32-process) est la ligne de commande à exécuter.</span><span class="sxs-lookup"><span data-stu-id="c4bc2-131">The only required input parameter for the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is the command line to execute.</span></span>


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



<span data-ttu-id="c4bc2-132">L’exemple de code VBScript suivant appelle la méthode **session. Invoke** pour exécuter la méthode [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) du [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="c4bc2-132">The following VBScript code example calls the **Session.Invoke** method to execute the [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) method of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="c4bc2-133">La méthode **StopService** n’a pas de paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="c4bc2-133">The **StopService** method does not have input parameters.</span></span> <span data-ttu-id="c4bc2-134">Toutefois, la méthode **Invoke** requiert une chaîne XML dans le paramètre *Parameters* .</span><span class="sxs-lookup"><span data-stu-id="c4bc2-134">However, the **Invoke** method requires an XML string in the *parameters* parameter.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c4bc2-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4bc2-135">Requirements</span></span>



| <span data-ttu-id="c4bc2-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4bc2-136">Requirement</span></span> | <span data-ttu-id="c4bc2-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4bc2-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4bc2-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4bc2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c4bc2-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4bc2-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c4bc2-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4bc2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c4bc2-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4bc2-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c4bc2-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4bc2-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4bc2-143"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4bc2-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4bc2-144">MIDL</span><span class="sxs-lookup"><span data-stu-id="c4bc2-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4bc2-145"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4bc2-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c4bc2-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c4bc2-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4bc2-147"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c4bc2-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c4bc2-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c4bc2-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4bc2-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4bc2-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4bc2-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4bc2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4bc2-151">**session**</span><span class="sxs-lookup"><span data-stu-id="c4bc2-151">**Session**</span></span>](session.md)
</dt> </dl>

 

