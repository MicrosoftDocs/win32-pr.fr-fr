---
title: Session. Create, méthode (WSManDisp. h)
description: Crée une nouvelle instance d’une ressource et retourne la référence de point de terminaison (EPR) du nouvel objet.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- Créer une méthode Windows Remote Management
- Create Method Windows Remote Management, objet session
- Windows Remote Management d’objet de session, méthode Create
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eacdbdffb9e2dac219e3922cabfc5615de34e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465954"
---
# <a name="sessioncreate-method"></a><span data-ttu-id="c50ce-106">Session. Create, méthode</span><span class="sxs-lookup"><span data-stu-id="c50ce-106">Session.Create method</span></span>

<span data-ttu-id="c50ce-107">Crée une nouvelle instance d’une ressource et retourne la [*référence de point de terminaison (EPR)*](windows-remote-management-glossary.md) du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="c50ce-107">Creates a new instance of a resource and returns the [*endpoint reference (EPR)*](windows-remote-management-glossary.md) of the new object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50ce-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c50ce-108">Syntax</span></span>


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c50ce-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c50ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c50ce-110">*resourceuri* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c50ce-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c50ce-111">Identificateur de la ressource à créer.</span><span class="sxs-lookup"><span data-stu-id="c50ce-111">Identifier of the resource to create.</span></span>

<span data-ttu-id="c50ce-112">Ce paramètre peut contenir l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c50ce-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="c50ce-113">URI avec un ou plusieurs [*sélecteurs*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c50ce-113">URI with one or more [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="c50ce-114">N’oubliez pas que le [*plug-in WMI*](windows-remote-management-glossary.md) ne prend pas en charge la création d’une ressource autre qu’un écouteur de [protocole WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="c50ce-114">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a [WS-Management Protocol](ws-management-protocol.md) listener.</span></span>
-   <span data-ttu-id="c50ce-115">Objet [**ResourceLocator**](resourcelocator.md) qui peut contenir des sélecteurs, des [*fragments*](windows-remote-management-glossary.md)ou des [*options*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c50ce-115">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="c50ce-116">Référence du point de terminaison [*WS-Addressing*](windows-remote-management-glossary.md) , comme décrit dans la norme du protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="c50ce-116">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="c50ce-117">Pour plus d’informations sur la spécification publique du protocole WS-Management, consultez la [page index des spécifications de gestion](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="c50ce-117">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="c50ce-118">*resource*</span><span class="sxs-lookup"><span data-stu-id="c50ce-118">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="c50ce-119">XML qui contient le contenu des ressources.</span><span class="sxs-lookup"><span data-stu-id="c50ce-119">The XML that contains resource content.</span></span>

</dd> <dt>

<span data-ttu-id="c50ce-120">*indicateurs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c50ce-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c50ce-121">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c50ce-121">Reserved.</span></span> <span data-ttu-id="c50ce-122">Doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="c50ce-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c50ce-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c50ce-123">Return value</span></span>

<span data-ttu-id="c50ce-124">EPR de la nouvelle ressource.</span><span class="sxs-lookup"><span data-stu-id="c50ce-124">The EPR of the new resource.</span></span>

## <a name="remarks"></a><span data-ttu-id="c50ce-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c50ce-125">Remarks</span></span>

<span data-ttu-id="c50ce-126">**Session. Create** est utilisé uniquement pour créer des instances d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="c50ce-126">**Session.Create** is only used for creating new instances of a resource.</span></span> <span data-ttu-id="c50ce-127">Utilisez la méthode [**session. put**](session-put.md) pour mettre à jour les instances existantes d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="c50ce-127">Use the [**Session.Put**](session-put.md) method to update existing instances of a resource.</span></span> <span data-ttu-id="c50ce-128">Une fois que vous avez obtenu le nouvel URI de ressource, vous pouvez appeler [**session. obtenir**](session-get.md) pour récupérer le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="c50ce-128">After you obtain the new resource URI, you can call [**Session.Get**](session-get.md) to retrieve the new object.</span></span> <span data-ttu-id="c50ce-129">Le nouvel objet contient toutes les propriétés assignées par le fournisseur de ressources lors de la création du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="c50ce-129">The new object contains any properties that the resource provider assigns when creating the new object.</span></span> <span data-ttu-id="c50ce-130">Par exemple, si vous créez un [*écouteur*](windows-remote-management-glossary.md) de protocole WS-Management et que vous récupérez l’objet écouteur à l’aide de **session. obtenir**, vous obtenez également les propriétés **port**, **Enabled** et **ListeningOn** .</span><span class="sxs-lookup"><span data-stu-id="c50ce-130">For example, if you create a new WS-Management protocol [*listener*](windows-remote-management-glossary.md) and retrieve the listener object using **Session.Get**, then you also obtain the **Port**, **Enabled**, and **ListeningOn** properties.</span></span>

<span data-ttu-id="c50ce-131">N’oubliez pas que le [*plug-in WMI*](windows-remote-management-glossary.md) ne prend pas en charge la création d’une ressource autre qu’un écouteur de protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="c50ce-131">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a WS-Management protocol listener.</span></span>

<span data-ttu-id="c50ce-132">La syntaxe suivante est utilisée pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c50ce-132">The following syntax is used to call this method.</span></span>


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a><span data-ttu-id="c50ce-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="c50ce-133">Examples</span></span>

<span data-ttu-id="c50ce-134">L’exemple de code VBScript suivant appelle **session. Create** pour créer un écouteur sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c50ce-134">The following VBScript code example calls **Session.Create** to create a listener on the local computer.</span></span>


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
```



## <a name="requirements"></a><span data-ttu-id="c50ce-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c50ce-135">Requirements</span></span>



| <span data-ttu-id="c50ce-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c50ce-136">Requirement</span></span> | <span data-ttu-id="c50ce-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="c50ce-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c50ce-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c50ce-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c50ce-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c50ce-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c50ce-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c50ce-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c50ce-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c50ce-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c50ce-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="c50ce-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="c50ce-143"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c50ce-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c50ce-144">MIDL</span><span class="sxs-lookup"><span data-stu-id="c50ce-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c50ce-145"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c50ce-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c50ce-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c50ce-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="c50ce-147"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c50ce-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c50ce-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c50ce-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c50ce-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c50ce-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c50ce-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c50ce-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c50ce-151">**session**</span><span class="sxs-lookup"><span data-stu-id="c50ce-151">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="c50ce-152">Protocole Gestion des services web</span><span class="sxs-lookup"><span data-stu-id="c50ce-152">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

