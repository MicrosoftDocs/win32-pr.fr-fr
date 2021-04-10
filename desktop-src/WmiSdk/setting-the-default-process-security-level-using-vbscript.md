---
title: Définir le niveau de sécurité de processus par défaut avec VBScript
description: Un script peut utiliser les paramètres d’authentification et d’emprunt d’identité WMI par défaut. Toutefois, le script peut nécessiter une connexion avec davantage de sécurité ou peut se connecter à un espace de noms qui requiert une connexion chiffrée.
ms.assetid: cb477224-3117-45e4-9271-613b58e48b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03fe69228021fe8d3f36f03e60cb2366b6132f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210560"
---
# <a name="set-the-default-process-security-level-with-vbscript"></a><span data-ttu-id="7dc4a-104">Définir le niveau de sécurité de processus par défaut avec VBScript</span><span class="sxs-lookup"><span data-stu-id="7dc4a-104">Set the default process security level with VBScript</span></span>

<span data-ttu-id="7dc4a-105">Un script peut utiliser les paramètres d’authentification et d’emprunt d’identité WMI par défaut.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-105">A script can use the default WMI authentication and impersonation settings.</span></span> <span data-ttu-id="7dc4a-106">Toutefois, le script peut nécessiter une connexion avec davantage de sécurité ou peut se connecter à un espace de noms qui requiert une connexion chiffrée.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-106">However, the script may need a connection with more security or may connect to a namespace that requires an encrypted connection.</span></span> <span data-ttu-id="7dc4a-107">Pour plus d’informations, consultez [définition de descripteurs de sécurité espace](setting-namespace-security-descriptors.md) et [demande d’une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="7dc4a-107">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md) and [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="7dc4a-108">Dans le cas le plus simple, un script peut utiliser les paramètres d’authentification et d’emprunt d’identité par défaut.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-108">In the simplest case, a script can use the default authentication and impersonation settings.</span></span> <span data-ttu-id="7dc4a-109">WMI s’exécute normalement dans un hôte de service partagé et partage la même authentification que les autres processus de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-109">WMI normally runs in a shared service host and shares the same authentication as other processes in the host.</span></span> <span data-ttu-id="7dc4a-110">Si vous souhaitez exécuter le processus WMI avec un autre niveau d’authentification, exécutez WMI avec la commande [**winmgmt**](winmgmt.md) avec le commutateur **/standalonehost** et définissez le niveau d’authentification pour WMI en général.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-110">If you want to run the WMI process with a different level of authentication, run WMI with the [**winmgmt**](winmgmt.md) command with the **/standalonehost** switch and set the authentication level for WMI generally.</span></span> <span data-ttu-id="7dc4a-111">Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="7dc4a-111">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

<span data-ttu-id="7dc4a-112">Le script suivant utilise les paramètres par défaut pour l’emprunt d’identité et les niveaux d’authentification.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-112">The following script uses default settings for impersonation and authentication levels.</span></span>


```VB
strComputer = "." 
Set objServices = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="7dc4a-113">Vous pouvez également utiliser un [moniker](constructing-a-moniker-string.md) dans un appel à [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)et définir les paramètres de sécurité par défaut, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-113">You can also use a [moniker](constructing-a-moniker-string.md) in a call to [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), and set the default security settings, as in the following example.</span></span>


```VB
strComputer = "." 
Set objServices = GetObject( _
    "winmgmts:{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!root/cimv2")
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="7dc4a-114">Pour plus d’informations sur la définition d’un autre niveau d’emprunt d’identité ou d’authentification dans un script, ou pour définir les valeurs par défaut d’un ordinateur, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="7dc4a-114">For more information about setting different impersonation or authentication levels in a script, or for setting the default values for a computer, see the following topics:</span></span>

-   [<span data-ttu-id="7dc4a-115">Modification des informations d’authentification par défaut à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="7dc4a-115">Changing the Default Authentication Credentials Using VBScript</span></span>](#changing-the-default-authentication-credentials-using-vbscript)
-   [<span data-ttu-id="7dc4a-116">Modification des paramètres d’emprunt d’identité par défaut à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="7dc4a-116">Changing the Default Impersonation Settings Using VBScript</span></span>](#changing-the-default-impersonation-levels-using-vbscript)
-   [<span data-ttu-id="7dc4a-117">Définition du niveau d’emprunt d’identité par défaut à l’aide du Registre</span><span class="sxs-lookup"><span data-stu-id="7dc4a-117">Setting the Default Impersonation Level Using the Registry</span></span>](#setting-the-default-impersonation-level-using-the-registry)
-   [<span data-ttu-id="7dc4a-118">Accès à l’objet SWbemSecurity dans VBScript</span><span class="sxs-lookup"><span data-stu-id="7dc4a-118">Accessing the SWbemSecurity Object in VBScript</span></span>](#accessing-the-swbemsecurity-object-in-vbscript)
-   [<span data-ttu-id="7dc4a-119">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="7dc4a-119">**SWbemSecurity**</span></span>](swbemsecurity.md)

## <a name="changing-the-default-authentication-credentials-using-vbscript"></a><span data-ttu-id="7dc4a-120">Modification des informations d’authentification par défaut à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="7dc4a-120">Changing the Default Authentication Credentials Using VBScript</span></span>

<span data-ttu-id="7dc4a-121">Vous pouvez modifier le niveau d’authentification dans un script à l’aide d’une chaîne de [moniker](constructing-a-moniker-string.md) et des objets [**SWbemLocator**](swbemlocator.md) et [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc4a-121">You can change the authentication level in a script using a [moniker](constructing-a-moniker-string.md) string, and the [**SWbemLocator**](swbemlocator.md) and [**SWbemSecurity**](swbemsecurity.md) objects.</span></span>

<span data-ttu-id="7dc4a-122">Le niveau d’authentification doit être défini en fonction des exigences du système d’exploitation cible auquel vous vous connectez.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-122">The authentication level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="7dc4a-123">Pour plus d’informations, consultez [connexion entre différents systèmes d’exploitation](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span><span class="sxs-lookup"><span data-stu-id="7dc4a-123">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="7dc4a-124">L’exemple de code VBScript suivant montre comment modifier le niveau d’authentification dans un script qui obtient les données d’espace libre à partir d’un ordinateur distant nommé « Serveur1 ».</span><span class="sxs-lookup"><span data-stu-id="7dc4a-124">The following VBScript code example shows how to change the authentication level in a script that obtains the free space data from a remote computer named "Server1".</span></span>


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{authenticationLevel=Pkt}!\\" _
    & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
    Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
        "FreeSpace: " & vbTab & objDisk.FreeSpace 
    NextstrComputer = "." 
    Set objServices = GetObject( "winmgmts:{impersonationLevel=impersonate," _
                               & "authenticationLevel=pktPrivacy}!root/cimv2")
    Set objProcessSet = objServices.ExecQuery("SELECT Name FROM Win32_Process",,48)
    For Each Process in objProcessSet
        WScript.Echo Process.Name
    Next
Next
```



<span data-ttu-id="7dc4a-125">Dans connexions de moniker de script à WMI, utilisez le nom abrégé indiqué dans la colonne « Nom/Description du moniker » du tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-125">In script moniker connections to WMI, use the short name shown in the "Moniker name/description" column of the table below.</span></span> <span data-ttu-id="7dc4a-126">Par exemple, dans le script suivant, le niveau d’authentification est défini sur **WbemAuthenticationLevelPktIntegrity**.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-126">For example, in the following script, the authentication level is set to **WbemAuthenticationLevelPktIntegrity**.</span></span>


```VB
SetobjWMIService = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!root\cimv2")
```



<span data-ttu-id="7dc4a-127">Le tableau suivant répertorie les niveaux d’authentification que vous pouvez définir.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-127">The following table lists the authentication levels you can set.</span></span> <span data-ttu-id="7dc4a-128">Ces niveaux sont définis dans wbemdisp. tlb dans l’énumération [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="7dc4a-128">These levels are defined in Wbemdisp.tlb in the enumeration [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>



| <span data-ttu-id="7dc4a-129">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="7dc4a-129">Name/value</span></span>                                                      | <span data-ttu-id="7dc4a-130">Description</span><span class="sxs-lookup"><span data-stu-id="7dc4a-130">Description</span></span>                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc4a-131">**WbemAuthenticationLevelDefault**</span><span class="sxs-lookup"><span data-stu-id="7dc4a-131">**WbemAuthenticationLevelDefault**</span></span><br/> <span data-ttu-id="7dc4a-132">0</span><span class="sxs-lookup"><span data-stu-id="7dc4a-132">0</span></span><br/>      | <span data-ttu-id="7dc4a-133">Moniker : par défaut</span><span class="sxs-lookup"><span data-stu-id="7dc4a-133">Moniker: Default</span></span><br/> <span data-ttu-id="7dc4a-134">WMI utilise le paramètre d’authentification Windows par défaut.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-134">WMI uses the default Windows authentication setting.</span></span> <span data-ttu-id="7dc4a-135">Il s’agit du paramètre recommandé qui permet à WMI de négocier au niveau requis par le serveur qui retourne des données.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-135">This is the recommended setting that allows WMI to negotiate to the level required by the server returning data.</span></span> <span data-ttu-id="7dc4a-136">Toutefois, si l’espace de noms requiert le chiffrement, utilisez **WbemAuthenticationLevelPktPrivacy**.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-136">However, if the namespace requires encryption, use **WbemAuthenticationLevelPktPrivacy**.</span></span><br/> |
| <span data-ttu-id="7dc4a-137">**WbemAuthenticationLevelNone**</span><span class="sxs-lookup"><span data-stu-id="7dc4a-137">**WbemAuthenticationLevelNone**</span></span><br/> <span data-ttu-id="7dc4a-138">1</span><span class="sxs-lookup"><span data-stu-id="7dc4a-138">1</span></span><br/>         | <span data-ttu-id="7dc4a-139">Moniker : aucun</span><span class="sxs-lookup"><span data-stu-id="7dc4a-139">Moniker: None</span></span><br/> <span data-ttu-id="7dc4a-140">N’utilise aucune authentification.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-140">Uses no authentication.</span></span><br/>                                                                                                                                                                                                                                            |
| <span data-ttu-id="7dc4a-141">**WbemAuthenticationLevelConnect**</span><span class="sxs-lookup"><span data-stu-id="7dc4a-141">**WbemAuthenticationLevelConnect**</span></span><br/> <span data-ttu-id="7dc4a-142">2</span><span class="sxs-lookup"><span data-stu-id="7dc4a-142">2</span></span><br/>      | <span data-ttu-id="7dc4a-143">Moniker : se connecter</span><span class="sxs-lookup"><span data-stu-id="7dc4a-143">Moniker: Connect</span></span><br/> <span data-ttu-id="7dc4a-144">Authentifie les informations d’identification du client uniquement lorsque le client établit une relation avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-144">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span><br/>                                                                                                                                                    |
| <span data-ttu-id="7dc4a-145">**WbemAuthenticationLevelCall**</span><span class="sxs-lookup"><span data-stu-id="7dc4a-145">**WbemAuthenticationLevelCall**</span></span><br/> <span data-ttu-id="7dc4a-146">3</span><span class="sxs-lookup"><span data-stu-id="7dc4a-146">3</span></span><br/>         | <span data-ttu-id="7dc4a-147">Appeler</span><span class="sxs-lookup"><span data-stu-id="7dc4a-147">Call</span></span><br/> <span data-ttu-id="7dc4a-148">Authentifie uniquement au début de chaque appel lorsque le serveur reçoit la demande.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-148">Authenticates only at the beginning of each call when the server receives the request.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="7dc4a-149">**WbemAuthenticationLevelPkt**</span><span class="sxs-lookup"><span data-stu-id="7dc4a-149">**WbemAuthenticationLevelPkt**</span></span><br/> <span data-ttu-id="7dc4a-150">4</span><span class="sxs-lookup"><span data-stu-id="7dc4a-150">4</span></span><br/>          | <span data-ttu-id="7dc4a-151">Moniker : PKT</span><span class="sxs-lookup"><span data-stu-id="7dc4a-151">Moniker: Pkt</span></span><br/> <span data-ttu-id="7dc4a-152">Authentifie que toutes les données reçues proviennent du client attendu.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-152">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                                                                                   |
| <span data-ttu-id="7dc4a-153">**WbemAuthenticationLevelPktIntegrity**</span><span class="sxs-lookup"><span data-stu-id="7dc4a-153">**WbemAuthenticationLevelPktIntegrity**</span></span><br/> <span data-ttu-id="7dc4a-154">5</span><span class="sxs-lookup"><span data-stu-id="7dc4a-154">5</span></span><br/> | <span data-ttu-id="7dc4a-155">Moniker : PktIntegrity</span><span class="sxs-lookup"><span data-stu-id="7dc4a-155">Moniker: PktIntegrity</span></span><br/> <span data-ttu-id="7dc4a-156">Authentifie et vérifie qu’aucune des données transférées entre le client et le serveur n’a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-156">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="7dc4a-157">**WbemAuthenticationLevelPktPrivacy**</span><span class="sxs-lookup"><span data-stu-id="7dc4a-157">**WbemAuthenticationLevelPktPrivacy**</span></span><br/> <span data-ttu-id="7dc4a-158">6</span><span class="sxs-lookup"><span data-stu-id="7dc4a-158">6</span></span><br/>   | <span data-ttu-id="7dc4a-159">Moniker : PktPrivacy</span><span class="sxs-lookup"><span data-stu-id="7dc4a-159">Moniker: PktPrivacy</span></span><br/> <span data-ttu-id="7dc4a-160">Authentifie tous les niveaux d’emprunt d’identité précédents et chiffre la valeur d’argument de chaque appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-160">Authenticates all previous impersonation levels and encrypts the argument value of each remote procedure call.</span></span> <span data-ttu-id="7dc4a-161">Utilisez ce paramètre si l’espace de noms auquel vous vous connectez requiert une connexion chiffrée.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-161">Use this setting if the namespace to which you are connecting requires an encrypted connection.</span></span><br/>                                               |



 

<span data-ttu-id="7dc4a-162">Pour déterminer si un appel a réussi, vérifiez la valeur de retour après avoir modifié le niveau d’authentification.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-162">To determine a successful call, check the return value after you change the authentication level.</span></span>

<span data-ttu-id="7dc4a-163">Par exemple, étant donné que les connexions locales ont toujours un niveau d’authentification de **wbemAuthenticationLevelPktPrivacy**, l’exemple suivant ne parvient pas à définir le niveau d’authentification, car il se connecte à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-163">For example, because local connections always have an authentication level of **wbemAuthenticationLevelPktPrivacy**, the following example fails to set the authentication level because it connects to the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!" _
    & "\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="7dc4a-164">Un fournisseur peut définir la sécurité sur un espace de noms afin qu’aucune donnée ne soit retournée, sauf si vous utilisez la confidentialité des paquets (PktPrivacy) dans votre connexion à cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-164">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (PktPrivacy) in your connection to that namespace.</span></span> <span data-ttu-id="7dc4a-165">Cela permet de s’assurer que les données sont chiffrées lorsqu’elles traversent le réseau.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-165">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="7dc4a-166">Si vous essayez de définir un niveau d’authentification inférieur, vous obtiendrez un message d’accès refusé.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-166">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="7dc4a-167">Pour plus d’informations, consultez [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="7dc4a-167">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="changing-the-default-impersonation-levels-using-vbscript"></a><span data-ttu-id="7dc4a-168">Modification des niveaux d’emprunt d’identité par défaut à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="7dc4a-168">Changing the Default Impersonation Levels Using VBScript</span></span>

<span data-ttu-id="7dc4a-169">Lorsque vous effectuez des appels à l’API de script pour WMI, il est recommandé d’utiliser les valeurs par défaut fournies par WMI pour le niveau d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-169">When you make calls to the Scripting API for WMI, it is recommended that you use the defaults that WMI provides for the impersonation level.</span></span> <span data-ttu-id="7dc4a-170">Les appels distants et certains fournisseurs avec plusieurs sauts réseau nécessitent un niveau d’emprunt d’identité supérieur à celui utilisé par WMI.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-170">Remote calls and some providers with more than one network hop require a higher impersonation level than WMI uses.</span></span> <span data-ttu-id="7dc4a-171">Si le niveau d’emprunt d’identité n’est pas suffisant, un fournisseur peut refuser une demande ou fournir des informations incomplètes.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-171">If the impersonation level is not sufficient, a provider might refuse a request or provide incomplete information.</span></span>

<span data-ttu-id="7dc4a-172">Si vous ne définissez pas le niveau d’emprunt d’identité dans un moniker ou en définissant [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) sur un objet sécurisable, définissez le niveau d’emprunt d’identité DCOM par défaut pour le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-172">If you do not set the impersonation level in either a moniker or by setting [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on a securable object, then set the default DCOM impersonation level for the operating system.</span></span> <span data-ttu-id="7dc4a-173">Le niveau d’emprunt d’identité doit être défini en fonction des exigences du système d’exploitation cible auquel vous vous connectez.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-173">The impersonation level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="7dc4a-174">Pour plus d’informations, consultez [connexion entre différents systèmes d’exploitation](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span><span class="sxs-lookup"><span data-stu-id="7dc4a-174">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="7dc4a-175">L’exemple de code VBScript suivant illustre la modification du niveau d’emprunt d’identité dans le script indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-175">The following VBScript code example shows changing the impersonation level in the same script shown above.</span></span>


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" _
                              & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
             "FreeSpace: " & vbTab & objDisk.FreeSpace 
Next
```



<span data-ttu-id="7dc4a-176">Le tableau suivant répertorie les niveaux d’authentification dans [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) qui utilisent.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-176">The following table lists the authentication levels in [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) that use.</span></span>



| <span data-ttu-id="7dc4a-177">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="7dc4a-177">Name/value</span></span>                                                    | <span data-ttu-id="7dc4a-178">Description</span><span class="sxs-lookup"><span data-stu-id="7dc4a-178">Description</span></span>                                                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc4a-179">**wbemImpersonationLevelAnonymous**</span><span class="sxs-lookup"><span data-stu-id="7dc4a-179">**wbemImpersonationLevelAnonymous**</span></span><br/> <span data-ttu-id="7dc4a-180">1</span><span class="sxs-lookup"><span data-stu-id="7dc4a-180">1</span></span><br/>   | <span data-ttu-id="7dc4a-181">Moniker : anonyme</span><span class="sxs-lookup"><span data-stu-id="7dc4a-181">Moniker: Anonymous</span></span><br/> <span data-ttu-id="7dc4a-182">Masque les informations d'identification de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-182">Hides the credentials of the caller.</span></span> <span data-ttu-id="7dc4a-183">Les appels à WMI peuvent échouer avec ce niveau d'emprunt d'identité.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-183">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                                  |
| <span data-ttu-id="7dc4a-184">**wbemImpersonationLevelIdentify**</span><span class="sxs-lookup"><span data-stu-id="7dc4a-184">**wbemImpersonationLevelIdentify**</span></span><br/> <span data-ttu-id="7dc4a-185">2</span><span class="sxs-lookup"><span data-stu-id="7dc4a-185">2</span></span><br/>    | <span data-ttu-id="7dc4a-186">Moniker : identifier</span><span class="sxs-lookup"><span data-stu-id="7dc4a-186">Moniker: Identify</span></span><br/> <span data-ttu-id="7dc4a-187">Permet aux objets d'interroger les informations d'identification de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-187">Allows objects to query the credentials of the caller.</span></span> <span data-ttu-id="7dc4a-188">Les appels à WMI peuvent échouer avec ce niveau d'emprunt d'identité.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-188">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                 |
| <span data-ttu-id="7dc4a-189">**wbemImpersonationLevelImpersonate**</span><span class="sxs-lookup"><span data-stu-id="7dc4a-189">**wbemImpersonationLevelImpersonate**</span></span><br/> <span data-ttu-id="7dc4a-190">3</span><span class="sxs-lookup"><span data-stu-id="7dc4a-190">3</span></span><br/> | <span data-ttu-id="7dc4a-191">Moniker : emprunter l’identité</span><span class="sxs-lookup"><span data-stu-id="7dc4a-191">Moniker: Impersonate</span></span><br/> <span data-ttu-id="7dc4a-192">Permet aux objets d'utiliser les informations d'identification de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-192">Allows objects to use the credentials of the caller.</span></span> <span data-ttu-id="7dc4a-193">Il s’agit du niveau d’emprunt d’identité recommandé pour l’API de script pour les appels WMI.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-193">This is the recommended impersonation level for Scripting API for WMI calls.</span></span><br/>                                                        |
| <span data-ttu-id="7dc4a-194">**wbemImpersonationLevelDelegate**</span><span class="sxs-lookup"><span data-stu-id="7dc4a-194">**wbemImpersonationLevelDelegate**</span></span><br/> <span data-ttu-id="7dc4a-195">4</span><span class="sxs-lookup"><span data-stu-id="7dc4a-195">4</span></span><br/>    | <span data-ttu-id="7dc4a-196">Moniker : délégué</span><span class="sxs-lookup"><span data-stu-id="7dc4a-196">Moniker: Delegate</span></span><br/> <span data-ttu-id="7dc4a-197">Permet aux objets d'autoriser d'autres objets à utiliser les informations d'identification de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-197">Allows objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="7dc4a-198">Cet emprunt d’identité fonctionne avec l’API de script pour les appels WMI, mais peut constituer un risque de sécurité inutile.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-198">This impersonation will work with Scripting API for WMI calls but may constitute an unnecessary security risk.</span></span><br/> |



 

<span data-ttu-id="7dc4a-199">L’exemple suivant montre comment définir l’emprunt d’identité dans une chaîne de moniker lors de l’obtention d’une instance spécifique de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="7dc4a-199">The following example shows how to set the impersonation in a moniker string when obtaining a specific instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>


```VB
Set object = GetObject("winmgmts:{impersonationLevel=impersonate}!root\cimv2:Win32_Process.Handle='0'")
```



<span data-ttu-id="7dc4a-200">Pour plus d’informations, consultez [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="7dc4a-200">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

## <a name="setting-the-default-impersonation-level-using-the-registry"></a><span data-ttu-id="7dc4a-201">Définition du niveau d’emprunt d’identité par défaut à l’aide du Registre</span><span class="sxs-lookup"><span data-stu-id="7dc4a-201">Setting the Default Impersonation Level Using the Registry</span></span>

<span data-ttu-id="7dc4a-202">Si vous avez accès au registre, vous pouvez également définir la clé de registre de niveau d’emprunt d’identité par défaut.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-202">If you have access to the registry, you can also set the default impersonation level registry key.</span></span> <span data-ttu-id="7dc4a-203">Cette clé spécifie le niveau d’emprunt d’identité que l’API de script pour WMI utilise, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-203">This key specifies which impersonation level the Scripting API for WMI uses unless otherwise specified.</span></span> <span data-ttu-id="7dc4a-204">Le chemin d’accès suivant identifie le chemin d’accès au registre.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-204">The following path identifies the registry path.</span></span>

<span data-ttu-id="7dc4a-205">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **niveau d’emprunt d’identité par défaut**</span><span class="sxs-lookup"><span data-stu-id="7dc4a-205">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Impersonation Level**</span></span>

<span data-ttu-id="7dc4a-206">Par défaut, la clé de registre a la valeur 3, en spécifiant le niveau d’emprunt d’identité emprunter l’identité.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-206">By default, the registry key is set to 3, specifying the Impersonate impersonation level.</span></span> <span data-ttu-id="7dc4a-207">Certains fournisseurs peuvent nécessiter un niveau d’emprunt d’identité plus élevé.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-207">Some providers may require a higher level of impersonation.</span></span>

## <a name="accessing-the-swbemsecurity-object-in-vbscript"></a><span data-ttu-id="7dc4a-208">Accès à l’objet SWbemSecurity dans VBScript</span><span class="sxs-lookup"><span data-stu-id="7dc4a-208">Accessing the SWbemSecurity Object in VBScript</span></span>

<span data-ttu-id="7dc4a-209">Vous pouvez également définir le niveau d’emprunt d’identité à partir de l’objet de sécurité [**SWbemSecurity**](swbemsecurity.md) , qui apparaît en tant que propriété de [**sécurité \_**](swbemservices-security-.md) des objets [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md)et [**SwbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc4a-209">The other way you can set the impersonation level is from the [**SWbemSecurity**](swbemsecurity.md) security object, which appears as the [**Security\_**](swbemservices-security-.md) property of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects.</span></span>

<span data-ttu-id="7dc4a-210">WMI transmet le paramètre de sécurité d’un objet parent aux descendants de l’objet d’origine.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-210">WMI passes the security setting of a parent object to the descendants of the original object.</span></span> <span data-ttu-id="7dc4a-211">Par conséquent, vous pouvez définir le niveau d’emprunt d’identité d’un objet [**SWbemServices**](swbemservices.md) après vous être connecté à WMI et les appels d’API à l’aide de cet objet ou des objets créés à partir de celui-ci, tels que des objets de type [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="7dc4a-211">Therefore, you can set the impersonation level of an [**SWbemServices**](swbemservices.md) object after logging on to WMI and API calls using this object or objects created from it, such as objects of type [**SWbemObject**](swbemobject.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7dc4a-212">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7dc4a-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dc4a-213">Connexion à WMI sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="7dc4a-213">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="7dc4a-214">Sécurisation des clients de script</span><span class="sxs-lookup"><span data-stu-id="7dc4a-214">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

