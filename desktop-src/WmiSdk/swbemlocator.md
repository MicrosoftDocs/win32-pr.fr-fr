---
description: Vous pouvez utiliser les méthodes de l’objet SWbemLocator pour obtenir un objet SWbemServices qui représente une connexion à un espace de noms sur un ordinateur local ou un ordinateur hôte distant.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Objet SWbemLocator (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 964b040fa5046aa619dc08df92838dca343ba9b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521227"
---
# <a name="swbemlocator-object"></a><span data-ttu-id="87d7d-103">Objet SWbemLocator</span><span class="sxs-lookup"><span data-stu-id="87d7d-103">SWbemLocator object</span></span>

<span data-ttu-id="87d7d-104">Vous pouvez utiliser les méthodes de l’objet **SWbemLocator** pour obtenir un objet [**SWbemServices**](swbemservices.md) qui représente une connexion à un espace de noms sur un ordinateur local ou un ordinateur hôte distant.</span><span class="sxs-lookup"><span data-stu-id="87d7d-104">You can use the methods of the **SWbemLocator** object to obtain an [**SWbemServices**](swbemservices.md) object that represents a connection to a namespace on either a local computer or a remote host computer.</span></span> <span data-ttu-id="87d7d-105">Vous pouvez ensuite utiliser les méthodes de l’objet **SWbemServices** pour accéder à WMI.</span><span class="sxs-lookup"><span data-stu-id="87d7d-105">You can then use the methods of the **SWbemServices** object to access WMI.</span></span> <span data-ttu-id="87d7d-106">Cet objet peut être créé par l’appel VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="87d7d-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="87d7d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="87d7d-107">Members</span></span>

<span data-ttu-id="87d7d-108">L’objet **SWbemLocator** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="87d7d-108">The **SWbemLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="87d7d-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="87d7d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="87d7d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="87d7d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="87d7d-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="87d7d-111">Methods</span></span>

<span data-ttu-id="87d7d-112">L’objet **SWbemLocator** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="87d7d-112">The **SWbemLocator** object has these methods.</span></span>



| <span data-ttu-id="87d7d-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="87d7d-113">Method</span></span>                                              | <span data-ttu-id="87d7d-114">Description</span><span class="sxs-lookup"><span data-stu-id="87d7d-114">Description</span></span>                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="87d7d-115">**ConnectServer**</span><span class="sxs-lookup"><span data-stu-id="87d7d-115">**ConnectServer**</span></span>](swbemlocator-connectserver.md) | <span data-ttu-id="87d7d-116">Établit une connexion à WMI sur l’ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="87d7d-116">Connects to WMI on the specified computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="87d7d-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="87d7d-117">Properties</span></span>

<span data-ttu-id="87d7d-118">L’objet **SWbemLocator** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="87d7d-118">The **SWbemLocator** object has these properties.</span></span>



| <span data-ttu-id="87d7d-119">Propriété</span><span class="sxs-lookup"><span data-stu-id="87d7d-119">Property</span></span>                                                | <span data-ttu-id="87d7d-120">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="87d7d-120">Access type</span></span>          | <span data-ttu-id="87d7d-121">Description</span><span class="sxs-lookup"><span data-stu-id="87d7d-121">Description</span></span>                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="87d7d-122">**Sécurité\_**</span><span class="sxs-lookup"><span data-stu-id="87d7d-122">**Security\_**</span></span>](swbemlocator-security-.md)<br/> | <span data-ttu-id="87d7d-123">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87d7d-123">Read-only</span></span><br/> | <span data-ttu-id="87d7d-124">Utilisé pour lire ou modifier les paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="87d7d-124">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87d7d-125">Notes</span><span class="sxs-lookup"><span data-stu-id="87d7d-125">Remarks</span></span>

<span data-ttu-id="87d7d-126">En haut du modèle d’objet de la bibliothèque de scripts WMI se trouve l’objet SWbemLocator.</span><span class="sxs-lookup"><span data-stu-id="87d7d-126">At the top of the WMI scripting library object model is the SWbemLocator object.</span></span> <span data-ttu-id="87d7d-127">SWbemLocator est utilisé pour établir une connexion authentifiée à un espace de noms WMI, de la même façon que la fonction GetObject de VBScript et le moniker WMI « winmgmts : » sont utilisés pour établir une connexion authentifiée à WMI.</span><span class="sxs-lookup"><span data-stu-id="87d7d-127">SWbemLocator is used to establish an authenticated connection to a WMI namespace, much as the VBScript GetObject function and the WMI moniker "winmgmts:" are used to establish an authenticated connection to WMI.</span></span> <span data-ttu-id="87d7d-128">Toutefois, SWbemLocator est conçu pour traiter deux scénarios de script spécifiques qui ne peuvent pas être exécutés à l’aide de GetObject et du moniker WMI.</span><span class="sxs-lookup"><span data-stu-id="87d7d-128">However, SWbemLocator is designed to address two specific scripting scenarios that cannot be performed using GetObject and the WMI moniker.</span></span> <span data-ttu-id="87d7d-129">Vous devez utiliser SWbemLocator si vous avez besoin de :</span><span class="sxs-lookup"><span data-stu-id="87d7d-129">You must use SWbemLocator if you need to:</span></span>

-   <span data-ttu-id="87d7d-130">Fournissez les informations d’identification de l’utilisateur et du mot de passe pour se connecter à WMI sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="87d7d-130">Provide user and password credentials to connect to WMI on a remote computer.</span></span> <span data-ttu-id="87d7d-131">Le moniker WMI utilisé avec la fonction GetObject n’inclut pas de mécanisme permettant de spécifier les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="87d7d-131">The WMI moniker used with the GetObject function does not include a mechanism for specifying credentials.</span></span> <span data-ttu-id="87d7d-132">La plupart des activités WMI (y compris toutes celles effectuées sur des ordinateurs distants) requièrent des droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="87d7d-132">Most WMI activities (including all of those carried out on remote computers) require administrator rights.</span></span> <span data-ttu-id="87d7d-133">Si vous vous connectez généralement à l’aide d’un compte d’utilisateur standard au lieu d’un compte d’administrateur, vous ne pourrez pas effectuer la plupart des tâches WMI, sauf si vous exécutez le script sous autres informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="87d7d-133">If you typically log on using a regular user account instead of an administrator account, you will not be able to perform most WMI tasks unless you run the script under alternate credentials.</span></span>
-   <span data-ttu-id="87d7d-134">Connectez-vous à WMI si vous exécutez un script WMI à partir d’une page Web.</span><span class="sxs-lookup"><span data-stu-id="87d7d-134">Connect to WMI if you are running a WMI script from within a Web page.</span></span> <span data-ttu-id="87d7d-135">Vous ne pouvez pas utiliser la fonction GetObject lors de l’exécution de scripts incorporés dans une page HTML, car Internet Explorer interdit l’utilisation de GetObject pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="87d7d-135">You cannot use the GetObject function when running scripts embedded within an HTML page because Internet Explorer disallows the use of GetObject for security reasons.</span></span>

<span data-ttu-id="87d7d-136">En outre, vous souhaiterez peut-être utiliser SWbemLocator pour vous connecter à WMI si vous trouvez la chaîne de connexion WMI utilisée avec la fonction GetObject déroutante ou difficile.</span><span class="sxs-lookup"><span data-stu-id="87d7d-136">In addition, you might want to use SWbemLocator to connect to WMI if you find the WMI connection string used with GetObject confusing or difficult.</span></span>

<span data-ttu-id="87d7d-137">Vous utilisez CreateObject au lieu de GetObject pour créer une référence à SWbemLocator.</span><span class="sxs-lookup"><span data-stu-id="87d7d-137">You use CreateObject rather than GetObject to create a reference to SWbemLocator.</span></span> <span data-ttu-id="87d7d-138">Pour créer la référence, vous devez passer à la fonction CreateObject l’identificateur programmatique SWbemLocator (ProgID) « WbemScripting. SWbemLocator », comme indiqué sur la ligne 2 dans l’exemple de script suivant.</span><span class="sxs-lookup"><span data-stu-id="87d7d-138">To create the reference, you must pass the CreateObject function the SWbemLocator programmatic identifier (ProgID) "WbemScripting.SWbemLocator", as shown on line 2 in the following script sample.</span></span> <span data-ttu-id="87d7d-139">Après avoir obtenu une référence à un objet SWbemLocator, vous appelez la méthode ConnectServer pour vous connecter à WMI et obtenir une référence à un objet SWbemServices.</span><span class="sxs-lookup"><span data-stu-id="87d7d-139">After you obtain a reference to an SWbemLocator object, you call the ConnectServer method to connect to WMI and obtain a reference to an SWbemServices object.</span></span> <span data-ttu-id="87d7d-140">Cela est illustré à la ligne 3 du script suivant.</span><span class="sxs-lookup"><span data-stu-id="87d7d-140">This is demonstrated on line 3 of the following script.</span></span>


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="87d7d-141">Pour exécuter un script sous d’autres informations d’identification, incluez le nom d’utilisateur et le mot de passe en tant que paramètres supplémentaires passés à ConnectServer.</span><span class="sxs-lookup"><span data-stu-id="87d7d-141">To run a script under alternate credentials, include the user name and password as additional parameters passed to ConnectServer.</span></span> <span data-ttu-id="87d7d-142">Par exemple, ce script s’exécute sous les informations d’identification d’un utilisateur nommé kenmyer, avec le mot de passe HomerJ.</span><span class="sxs-lookup"><span data-stu-id="87d7d-142">For example, this script runs under the credentials of a user named kenmyer, with the password homerj.</span></span>


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="87d7d-143">Vous pouvez également utiliser le \\ format de nom d’utilisateur de domaine pour spécifier un nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="87d7d-143">You can also use the Domain\\User Name format to specify a user name.</span></span> <span data-ttu-id="87d7d-144">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="87d7d-144">For example:</span></span>

`" fabrikam\kenmyer"`

## <a name="examples"></a><span data-ttu-id="87d7d-145">Exemples</span><span class="sxs-lookup"><span data-stu-id="87d7d-145">Examples</span></span>

<span data-ttu-id="87d7d-146">L’exemple PowerShell suivant utilise **SWbemLocator** pour se connecter à un serveur.</span><span class="sxs-lookup"><span data-stu-id="87d7d-146">The following PowerShell example uses **SWbemLocator** to connect to a server.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="87d7d-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87d7d-147">Requirements</span></span>



| <span data-ttu-id="87d7d-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87d7d-148">Requirement</span></span> | <span data-ttu-id="87d7d-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="87d7d-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87d7d-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87d7d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="87d7d-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87d7d-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87d7d-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87d7d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="87d7d-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87d7d-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87d7d-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="87d7d-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="87d7d-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="87d7d-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="87d7d-156">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="87d7d-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="87d7d-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="87d7d-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="87d7d-158">DLL</span><span class="sxs-lookup"><span data-stu-id="87d7d-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87d7d-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87d7d-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="87d7d-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="87d7d-160">CLSID</span></span><br/>                    | <span data-ttu-id="87d7d-161">CLSID \_ SWbemLocator</span><span class="sxs-lookup"><span data-stu-id="87d7d-161">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="87d7d-162">IID</span><span class="sxs-lookup"><span data-stu-id="87d7d-162">IID</span></span><br/>                      | <span data-ttu-id="87d7d-163">IID \_ ISWbemLocator</span><span class="sxs-lookup"><span data-stu-id="87d7d-163">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="87d7d-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87d7d-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d7d-165">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="87d7d-165">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




