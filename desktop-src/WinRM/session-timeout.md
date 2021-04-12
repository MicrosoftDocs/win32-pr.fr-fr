---
title: Session. Timeout, propriété (WSManDisp. h)
description: Définit et obtient la durée maximale, en millisecondes, pendant laquelle l’application cliente attend Windows Remote Management exécuter ses opérations.
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- Propriété Timeout Windows Remote Management
- Propriété Timeout Windows Remote Management, objet session
- Windows Remote Management de l’objet session, propriété Timeout
topic_type:
- apiref
api_name:
- Session.Timeout
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6c28b5284d9061e1c80fb3c66193d394c347a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317521"
---
# <a name="sessiontimeout-property"></a><span data-ttu-id="cafcf-106">Session. Timeout (propriété)</span><span class="sxs-lookup"><span data-stu-id="cafcf-106">Session.Timeout property</span></span>

<span data-ttu-id="cafcf-107">Définit et obtient la durée maximale, en millisecondes, pendant laquelle l’application cliente attend Windows Remote Management exécuter ses opérations.</span><span class="sxs-lookup"><span data-stu-id="cafcf-107">Sets and gets the maximum amount of time, in milliseconds, that the client application waits for Windows Remote Management to complete its operations.</span></span>

<span data-ttu-id="cafcf-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="cafcf-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cafcf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cafcf-109">Syntax</span></span>


```VB
Session.Timeout As long
```



## <a name="property-value"></a><span data-ttu-id="cafcf-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cafcf-110">Property value</span></span>

<span data-ttu-id="cafcf-111">Valeur du délai d’attente, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="cafcf-111">Time-out value, in milliseconds.</span></span> <span data-ttu-id="cafcf-112">Lorsque la valeur du délai d’attente est dépassée, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="cafcf-112">When the time-out value is exceeded, a run-time error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="cafcf-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cafcf-113">Remarks</span></span>

<span data-ttu-id="cafcf-114">La valeur du délai d’attente peut être définie avant chaque opération effectuée par l’agent.</span><span class="sxs-lookup"><span data-stu-id="cafcf-114">The time-out value can be set before each operation performed by the agent.</span></span> <span data-ttu-id="cafcf-115">Si une valeur de délai d’attente n’est pas spécifiée, l’agent définit la valeur du délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="cafcf-115">If a time-out value is not specified, the agent sets the time-out value.</span></span>

<span data-ttu-id="cafcf-116">Pendant une opération d’énumération, la valeur du délai d’attente ne peut pas être réinitialisée pendant l’énumération de la ressource.</span><span class="sxs-lookup"><span data-stu-id="cafcf-116">During an enumerate operation, the time-out value cannot be reset while the resource is being enumerated.</span></span>

## <a name="examples"></a><span data-ttu-id="cafcf-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="cafcf-117">Examples</span></span>

<span data-ttu-id="cafcf-118">L’exemple de code VBScript suivant démarre un processus de Calc.exe à l’aide de la méthode [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) de la classe de [**\_ processus WMI Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="cafcf-118">The following VBScript code example starts a Calc.exe process using the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span> <span data-ttu-id="cafcf-119">Le paramètre *strInputParameters* contient les paramètres d’entrée au format XML.</span><span class="sxs-lookup"><span data-stu-id="cafcf-119">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="cafcf-120">Le script spécifie un délai d’expiration pour la session.</span><span class="sxs-lookup"><span data-stu-id="cafcf-120">The script specifies a time-out for the session.</span></span>


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

'Reset timeout to 10,000 milliseconds
objSession.Timeout = 10000     

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



## <a name="requirements"></a><span data-ttu-id="cafcf-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cafcf-121">Requirements</span></span>



| <span data-ttu-id="cafcf-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cafcf-122">Requirement</span></span> | <span data-ttu-id="cafcf-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="cafcf-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cafcf-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cafcf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cafcf-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cafcf-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="cafcf-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cafcf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cafcf-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cafcf-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="cafcf-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="cafcf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cafcf-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cafcf-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cafcf-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="cafcf-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cafcf-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cafcf-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="cafcf-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cafcf-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="cafcf-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cafcf-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cafcf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="cafcf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cafcf-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cafcf-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cafcf-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cafcf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cafcf-137">**session**</span><span class="sxs-lookup"><span data-stu-id="cafcf-137">**Session**</span></span>](session.md)
</dt> </dl>

 

