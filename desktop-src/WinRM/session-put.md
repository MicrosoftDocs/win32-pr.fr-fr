---
title: Session. put, méthode (WSManDisp. h)
description: Met à jour une ressource.
ms.assetid: f121d9ce-6aa3-45e3-b0ba-67b19c2f5665
ms.tgt_platform: multiple
keywords:
- Put, méthode Windows Remote Management
- Put, méthode Windows Remote Management, objet session
- Windows Remote Management d’objet de session, méthode put
topic_type:
- apiref
api_name:
- Session.Put
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0f09b0a0f8de4e7f7d06cb84753e6b708841f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384948"
---
# <a name="sessionput-method"></a><span data-ttu-id="7909e-106">Session. put, méthode</span><span class="sxs-lookup"><span data-stu-id="7909e-106">Session.Put method</span></span>

<span data-ttu-id="7909e-107">Met à jour une ressource.</span><span class="sxs-lookup"><span data-stu-id="7909e-107">Updates a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="7909e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7909e-108">Syntax</span></span>


```VB
Session.Put( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7909e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7909e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7909e-110">*resourceuri* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7909e-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7909e-111">Identificateur de la ressource à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="7909e-111">The identifier of the resource to be updated.</span></span>

<span data-ttu-id="7909e-112">Ce paramètre peut contenir l’un des éléments contenus dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="7909e-112">This parameter can contain one of elements contained in the following list:</span></span>

-   <span data-ttu-id="7909e-113">URI avec ou sans [*sélecteurs*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="7909e-113">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="7909e-114">Quand vous appelez la méthode **put** pour obtenir une ressource WMI, utilisez la ou les propriétés de clé de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7909e-114">When calling the **Put** method to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="7909e-115">Par exemple, dans l’exemple de code Visual Basic Scripting Edition (VBScript) suivant, la clé est spécifiée par `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="7909e-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="7909e-116">Objet [**ResourceLocator**](resourcelocator.md) qui peut contenir des sélecteurs, des [*fragments*](windows-remote-management-glossary.md)ou des [*options*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="7909e-116">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="7909e-117">Référence du point de terminaison [*WS-Addressing*](windows-remote-management-glossary.md) , comme décrit dans la norme [protocole WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="7909e-117">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="7909e-118">Pour plus d’informations sur la spécification publique du protocole WS-Management, consultez la [page index des spécifications de gestion](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="7909e-118">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="7909e-119">*ressource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7909e-119">*resource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7909e-120">Contenu de la ressource mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7909e-120">The updated resource content.</span></span>

</dd> <dt>

<span data-ttu-id="7909e-121">*indicateurs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7909e-121">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7909e-122">Réservé.</span><span class="sxs-lookup"><span data-stu-id="7909e-122">Reserved.</span></span> <span data-ttu-id="7909e-123">Doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="7909e-123">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7909e-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7909e-124">Return value</span></span>

<span data-ttu-id="7909e-125">XML qui contient le contenu de la ressource mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7909e-125">The XML that contains the updated resource content.</span></span>

## <a name="examples"></a><span data-ttu-id="7909e-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="7909e-126">Examples</span></span>

<span data-ttu-id="7909e-127">L’exemple de code VBScript suivant écrit des données dans l’objet [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) .</span><span class="sxs-lookup"><span data-stu-id="7909e-127">The following VBScript code example writes data to the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) object.</span></span> <span data-ttu-id="7909e-128">Vous devez inclure toutes les propriétés non-tableau de l’objet dans le XML du paramètre de *ressource* .</span><span class="sxs-lookup"><span data-stu-id="7909e-128">You must include all non-array properties of the object in the XML of the *Resource* parameter.</span></span> <span data-ttu-id="7909e-129">L’ordre des propriétés n’est pas significatif.</span><span class="sxs-lookup"><span data-stu-id="7909e-129">The order of the properties is not significant.</span></span>


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

'Change the property value by putting
'the new XML content into the resource.
Dim strResourceUri, strReturnedResourceUri, newXmlContent
strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
  & "wmi/root/cimv2/Win32_WMISetting"
newXmlContent = _
  "<p:Win32_WMISetting xmlns:p=""http://schemas.microsoft.com/" & _
  "wbem/wsman/1/wmi/root/cimv2/Win32_WMISetting"">" & _
  "<p:LoggingLevel>2</p:LoggingLevel></p:Win32_WMISetting>" 

On Error Resume Next
strReturnedResourceUri = objSession.Put(reourceUri, newXmlContent)
WScript.Echo "Returned resource Uri:" & Chr(10) & _
  strReturnedResourceUri
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



## <a name="requirements"></a><span data-ttu-id="7909e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7909e-130">Requirements</span></span>



| <span data-ttu-id="7909e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7909e-131">Requirement</span></span> | <span data-ttu-id="7909e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7909e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7909e-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7909e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7909e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7909e-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="7909e-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7909e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7909e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7909e-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7909e-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="7909e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7909e-138"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7909e-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7909e-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="7909e-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7909e-140"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7909e-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7909e-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7909e-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="7909e-142"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7909e-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7909e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="7909e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7909e-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7909e-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7909e-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7909e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7909e-146">**session**</span><span class="sxs-lookup"><span data-stu-id="7909e-146">**Session**</span></span>](session.md)
</dt> </dl>

 

