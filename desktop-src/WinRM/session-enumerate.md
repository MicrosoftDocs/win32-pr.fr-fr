---
title: Session. Enumerate, méthode (WSManDisp. h)
description: Énumère une table, une collection de données ou une ressource de journal.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- Énumération de la méthode Windows Remote Management
- Énumérer la méthode Windows Remote Management, objet session
- Windows Remote Management d’objet de session, énumération, méthode
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca6b66b910251c641832cde3ddd93d6479f66be7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032631"
---
# <a name="sessionenumerate-method"></a><span data-ttu-id="97de7-106">Session. Enumerate, méthode</span><span class="sxs-lookup"><span data-stu-id="97de7-106">Session.Enumerate method</span></span>

<span data-ttu-id="97de7-107">Énumère une table, une collection de données ou une ressource de journal.</span><span class="sxs-lookup"><span data-stu-id="97de7-107">Enumerates a table, data collection, or log resource.</span></span> <span data-ttu-id="97de7-108">Pour créer une requête, incluez un paramètre de *filtre* et un paramètre de *dialecte* dans une énumération.</span><span class="sxs-lookup"><span data-stu-id="97de7-108">To create a query, include a *filter* parameter and a *dialect* parameter in an enumeration.</span></span> <span data-ttu-id="97de7-109">Vous pouvez également utiliser un objet [**ResourceLocator**](resourcelocator.md) pour créer des requêtes.</span><span class="sxs-lookup"><span data-stu-id="97de7-109">You can also use a [**ResourceLocator**](resourcelocator.md) object to create queries.</span></span> <span data-ttu-id="97de7-110">Pour plus d’informations, consultez [énumération ou liste de toutes les instances d’une ressource](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="97de7-110">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="97de7-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97de7-111">Syntax</span></span>


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="97de7-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97de7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97de7-113">*resourceuri* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97de7-113">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97de7-114">Identificateur de la ressource à récupérer.</span><span class="sxs-lookup"><span data-stu-id="97de7-114">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="97de7-115">Ce paramètre peut contenir l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="97de7-115">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="97de7-116">URI de la ressource.</span><span class="sxs-lookup"><span data-stu-id="97de7-116">The URI of the resource.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   <span data-ttu-id="97de7-117">Objet [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="97de7-117">A [**ResourceLocator**](resourcelocator.md) object.</span></span>
-   <span data-ttu-id="97de7-118">Une référence de point de terminaison [*WS-Addressing*](windows-remote-management-glossary.md) , comme décrit dans la norme de protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="97de7-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="97de7-119">Pour plus d’informations sur la spécification publique pour [protocole WS-Management](ws-management-protocol.md), consultez la [page index des spécifications de gestion](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="97de7-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="97de7-120">*filtre* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="97de7-120">*filter* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97de7-121">Filtre qui définit les éléments de la ressource qui sont retournés par l’énumération.</span><span class="sxs-lookup"><span data-stu-id="97de7-121">A filter that defines what items in the resource are returned by the enumeration.</span></span> <span data-ttu-id="97de7-122">Lorsque la ressource est énumérée, seuls les éléments qui correspondent aux critères de filtre sont retournés.</span><span class="sxs-lookup"><span data-stu-id="97de7-122">When the resource is enumerated, only those items that match the filter criteria are returned.</span></span> <span data-ttu-id="97de7-123">L’inclusion d’un paramètre de *filtre* et d’un paramètre de *dialecte* dans une énumération convertit l’énumération en requête.</span><span class="sxs-lookup"><span data-stu-id="97de7-123">Including a *filter* parameter and a *dialect* parameter in an enumeration converts the enumeration into a query.</span></span> <span data-ttu-id="97de7-124">Pour obtenir un exemple, consultez [interrogation d’instances spécifiques d’une ressource](querying-for-specific-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="97de7-124">For an example, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

<span data-ttu-id="97de7-125">Si vous avez un objet [**ResourceLocator**](resourcelocator.md) pour le paramètre *resourceURI* , ce paramètre ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="97de7-125">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="97de7-126">*dialecte* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="97de7-126">*dialect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97de7-127">Langue utilisée par le filtre.</span><span class="sxs-lookup"><span data-stu-id="97de7-127">The language used by the filter.</span></span> <span data-ttu-id="97de7-128">[WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), un sous-ensemble de SQL utilisé par WMI, est le seul langage pris en charge.</span><span class="sxs-lookup"><span data-stu-id="97de7-128">[WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), a subset of SQL used by WMI, is the only language supported.</span></span>

<span data-ttu-id="97de7-129">Si vous avez un objet [**ResourceLocator**](resourcelocator.md) pour le paramètre *resourceURI* , ce paramètre ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="97de7-129">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="97de7-130">*indicateurs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="97de7-130">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97de7-131">Paramètre qui doit contenir un indicateur dans l’énumération **\_ \_ WSManEnumFlags** .</span><span class="sxs-lookup"><span data-stu-id="97de7-131">A parameter that must contain a flag in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="97de7-132">Pour plus d’informations, consultez [énumération, constantes](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="97de7-132">For more information, see [Enumeration Constants](enumeration-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97de7-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97de7-133">Return value</span></span>

<span data-ttu-id="97de7-134">Objet [**énumérateur**](enumerator.md) qui contient les résultats de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="97de7-134">An [**Enumerator**](enumerator.md) object that contains the results of the enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="97de7-135">Notes</span><span class="sxs-lookup"><span data-stu-id="97de7-135">Remarks</span></span>

<span data-ttu-id="97de7-136">Pour plus d’informations sur la limitation des appels réseau pendant une énumération, consultez la propriété [**BatchItems**](session-batchitems.md) .</span><span class="sxs-lookup"><span data-stu-id="97de7-136">For more information about limiting network calls during an enumeration, see the [**BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="97de7-137">Sachez que si les indicateurs incluent les [**constantes d’énumération**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** ou **WSManFlagHierarchyShallow** , Windows Remote Management Service retourne le code d’erreur le **mode de \_ polymorphisme WSMan n’est pas \_ \_ \_ pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="97de7-137">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then Windows Remote Management service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

<span data-ttu-id="97de7-138">Si un filtre est spécifié, il doit s’agir d’un document valide en ce qui concerne le schéma de la ressource.</span><span class="sxs-lookup"><span data-stu-id="97de7-138">If a filter is specified, it must be a valid document with respect to the schema of the resource.</span></span> <span data-ttu-id="97de7-139">Le paramètre de dialecte est facultatif.</span><span class="sxs-lookup"><span data-stu-id="97de7-139">The dialect parameter is optional.</span></span> <span data-ttu-id="97de7-140">Toutefois, si la chaîne de filtre commence par <, mais n’est pas un fragment XML, vous devez inclure le paramètre de *dialecte* ou définir l’indicateur **WSManFlagNonXmlText** dans le paramètre *Flags* .</span><span class="sxs-lookup"><span data-stu-id="97de7-140">However, if the filter string begins with <, but is not an XML fragment, then either include the *dialect* parameter or set the **WSManFlagNonXmlText** flag in the *flags* parameter.</span></span> <span data-ttu-id="97de7-141">Pour plus d’informations, consultez [**énumération, constantes**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="97de7-141">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

<span data-ttu-id="97de7-142">La méthode C++ correspondante est [**IWSManSession :: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="97de7-142">The corresponding C++ method is [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

## <a name="examples"></a><span data-ttu-id="97de7-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="97de7-143">Examples</span></span>

<span data-ttu-id="97de7-144">L’exemple de code VBScript suivant énumère les instances de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) sur un ordinateur distant spécifié par le nom de domaine complet (ServerName.domain.com).</span><span class="sxs-lookup"><span data-stu-id="97de7-144">The following VBScript code example enumerates the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instances on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="97de7-145">N’oubliez pas que la libération de l’objet d’énumération efface les demandes d’énumération en attente.</span><span class="sxs-lookup"><span data-stu-id="97de7-145">Be aware that freeing the enumeration object clears pending enumeration requests.</span></span> <span data-ttu-id="97de7-146">La sous-routine DisplayOutput utilise le fichier de transformation XML de l’outil en ligne de commande WinRM (WsmTxt. Xsl) pour générer les données sous forme de tableau.</span><span class="sxs-lookup"><span data-stu-id="97de7-146">The DisplayOutput subroutine uses the Winrm command-line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

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



## <a name="requirements"></a><span data-ttu-id="97de7-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97de7-147">Requirements</span></span>



| <span data-ttu-id="97de7-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97de7-148">Requirement</span></span> | <span data-ttu-id="97de7-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="97de7-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="97de7-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97de7-150">Minimum supported client</span></span><br/> | <span data-ttu-id="97de7-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97de7-151">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="97de7-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97de7-152">Minimum supported server</span></span><br/> | <span data-ttu-id="97de7-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97de7-153">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="97de7-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="97de7-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="97de7-155"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="97de7-155"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="97de7-156">MIDL</span><span class="sxs-lookup"><span data-stu-id="97de7-156">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97de7-157"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97de7-157"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="97de7-158">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="97de7-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="97de7-159"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="97de7-159"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="97de7-160">DLL</span><span class="sxs-lookup"><span data-stu-id="97de7-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97de7-161"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97de7-161"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="97de7-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97de7-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97de7-163">**session**</span><span class="sxs-lookup"><span data-stu-id="97de7-163">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="97de7-164">Interrogation d’instances spécifiques d’une ressource</span><span class="sxs-lookup"><span data-stu-id="97de7-164">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="97de7-165">**BatchItems**</span><span class="sxs-lookup"><span data-stu-id="97de7-165">**BatchItems**</span></span>](session-batchitems.md)
</dt> <dt>

[<span data-ttu-id="97de7-166">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="97de7-166">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

