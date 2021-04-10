---
title: Session. obten, méthode (WSManDisp. h)
description: Récupère la ressource spécifiée par l’URI et retourne une représentation XML de l’instance actuelle de la ressource.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Méthode d’extraction Windows Remote Management
- Méthode d’extraction Windows Remote Management, objet session
- Windows Remote Management d’objet de session, méthode d’extraction
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
ms.openlocfilehash: 7e4ee84cc711db312389151d1dd95fb890474dcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317385"
---
# <a name="sessionget-method"></a><span data-ttu-id="130ef-106">Session. obten, méthode</span><span class="sxs-lookup"><span data-stu-id="130ef-106">Session.Get method</span></span>

<span data-ttu-id="130ef-107">Récupère la ressource spécifiée par l' [*URI*](windows-remote-management-glossary.md) et retourne une représentation XML de l’instance actuelle de la ressource.</span><span class="sxs-lookup"><span data-stu-id="130ef-107">Retrieves the resource specified by the [*URI*](windows-remote-management-glossary.md) and returns an XML representation of the current instance of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="130ef-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="130ef-108">Syntax</span></span>


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="130ef-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="130ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="130ef-110">*resourceuri* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="130ef-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="130ef-111">Identificateur de la ressource à récupérer.</span><span class="sxs-lookup"><span data-stu-id="130ef-111">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="130ef-112">Ce paramètre peut contenir l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="130ef-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="130ef-113">URI avec ou sans [*sélecteurs*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="130ef-113">A URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="130ef-114">Quand vous appelez la méthode **obtenir** avec un sélecteur pour obtenir une ressource WMI, utilisez la ou les propriétés de clé de l’objet.</span><span class="sxs-lookup"><span data-stu-id="130ef-114">When calling the **Get** method with a selector to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="130ef-115">Par exemple, dans l’exemple de code Visual Basic Scripting Edition (VBScript) suivant, la clé est spécifiée par `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="130ef-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span> <span data-ttu-id="130ef-116">Pour les classes Singleton, telles que [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), vous ne pouvez pas utiliser de sélecteur.</span><span class="sxs-lookup"><span data-stu-id="130ef-116">For singleton classes, such as [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), you cannot use a selector.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   <span data-ttu-id="130ef-117">Objet [**ResourceLocator**](resourcelocator.md) qui peut contenir des sélecteurs, des [*fragments*](windows-remote-management-glossary.md)ou des [*options*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="130ef-117">A [**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="130ef-118">Une référence de point de terminaison [*WS-Addressing*](windows-remote-management-glossary.md) , comme décrit dans la norme de protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="130ef-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="130ef-119">Pour plus d’informations sur la spécification publique pour [protocole WS-Management](ws-management-protocol.md), consultez la [page index des spécifications de gestion](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="130ef-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="130ef-120">*indicateurs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="130ef-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="130ef-121">Réservé.</span><span class="sxs-lookup"><span data-stu-id="130ef-121">Reserved.</span></span> <span data-ttu-id="130ef-122">Doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="130ef-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="130ef-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="130ef-123">Return value</span></span>

<span data-ttu-id="130ef-124">Représentation XML de la ressource.</span><span class="sxs-lookup"><span data-stu-id="130ef-124">An XML representation of the resource.</span></span>

## <a name="examples"></a><span data-ttu-id="130ef-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="130ef-125">Examples</span></span>

<span data-ttu-id="130ef-126">L’exemple de code VBScript suivant récupère la représentation XML de l’instance de [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) qui représente le service WinMgmt WMI sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="130ef-126">The following VBScript code example retrieves the XML representation of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) instance that represents the WMI Winmgmt service on the local computer.</span></span>


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



<span data-ttu-id="130ef-127">L’exemple de code VBScript suivant récupère l’instance de service WinMgmt WMI à partir d’un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="130ef-127">The following VBScript code example retrieves the WMI Winmgmt service instance from a remote computer.</span></span> <span data-ttu-id="130ef-128">L’ordinateur distant est identifié par le nom de domaine complet (servername.domain.com).</span><span class="sxs-lookup"><span data-stu-id="130ef-128">The remote computer is identified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="130ef-129">La seule différence entre la version locale et la version distante est la spécification de l’ordinateur distant dans l’appel à [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="130ef-129">The only difference between the local and remote version is the specification of the remote computer in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="130ef-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="130ef-130">Requirements</span></span>



| <span data-ttu-id="130ef-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="130ef-131">Requirement</span></span> | <span data-ttu-id="130ef-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="130ef-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="130ef-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="130ef-133">Minimum supported client</span></span><br/> | <span data-ttu-id="130ef-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="130ef-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="130ef-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="130ef-135">Minimum supported server</span></span><br/> | <span data-ttu-id="130ef-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="130ef-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="130ef-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="130ef-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="130ef-138"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="130ef-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="130ef-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="130ef-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="130ef-140"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="130ef-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="130ef-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="130ef-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="130ef-142"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="130ef-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="130ef-143">DLL</span><span class="sxs-lookup"><span data-stu-id="130ef-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="130ef-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="130ef-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="130ef-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="130ef-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="130ef-146">**session**</span><span class="sxs-lookup"><span data-stu-id="130ef-146">**Session**</span></span>](session.md)
</dt> </dl>

 

