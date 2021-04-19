---
description: Décrit comment les scripts, les applications et les fournisseurs peuvent établir des connexions à WMI sur des ordinateurs distants pour obtenir des données ou contrôler le matériel et les logiciels.
ms.assetid: 16b00ee3-f721-4912-9e8e-2fdbc897a813
ms.tgt_platform: multiple
title: Connexion à WMI sur un ordinateur distant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d581d1be73013e57ef2193102f6e8afc287b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536760"
---
# <a name="connecting-to-wmi-on-a-remote-computer"></a><span data-ttu-id="fd8cd-103">Connexion à WMI sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="fd8cd-103">Connecting to WMI on a Remote Computer</span></span>

<span data-ttu-id="fd8cd-104">WMI peut être utilisé pour gérer et accéder aux données WMI sur des ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-104">WMI can be used to manage and access WMI data on remote computers.</span></span> <span data-ttu-id="fd8cd-105">Les connexions distantes dans WMI sont affectées par les paramètres du [pare-feu Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) et de DCOM.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) and DCOM settings.</span></span> <span data-ttu-id="fd8cd-106">[Le contrôle de compte d’utilisateur (UAC)](/previous-versions/aa905108(v=msdn.10)) peut également nécessiter des modifications de certains paramètres.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-106">[User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)) may also require changes to some settings.</span></span> <span data-ttu-id="fd8cd-107">Toutefois, une fois que vos paramètres sont corrects, l’appel à un système distant est très similaire à un appel WMI local.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-107">However, once your have your settings correct, the call to a remote system is very similar to a local WMI call.</span></span> <span data-ttu-id="fd8cd-108">Toutefois, vous pouvez choisir de le rendre plus complexe en utilisant des informations d’identification différentes, des protocoles d’authentification supplémentaires et d’autres fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-108">You may choose to make it more complex however, by using different credentials, alternate authentication protocols, and other security features.</span></span>

## <a name="configuring-a-computer-for-a-remote-connection"></a><span data-ttu-id="fd8cd-109">Configuration d’un ordinateur pour une connexion à distance</span><span class="sxs-lookup"><span data-stu-id="fd8cd-109">Configuring a Computer for a Remote Connection</span></span>

<span data-ttu-id="fd8cd-110">Avant de pouvoir accéder à un système distant avec WMI, vous devrez peut-être vérifier certains paramètres de sécurité pour confirmer que vous disposez d’un accès.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-110">Before you can access a remote system with WMI, you may need to check some security settings to confirm that you have access.</span></span> <span data-ttu-id="fd8cd-111">Plus précisément :</span><span class="sxs-lookup"><span data-stu-id="fd8cd-111">Specifically:</span></span>

-   <span data-ttu-id="fd8cd-112">Windows contient un certain nombre de fonctionnalités de sécurité qui peuvent bloquer l’accès aux scripts sur les systèmes distants.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-112">Windows contains a number of security features that may block access to scripts on remote systems.</span></span> <span data-ttu-id="fd8cd-113">Par conséquent, vous devrez peut-être modifier les paramètres de Active Directory et du pare-feu Windows de votre système avant d’effectuer un appel WMI.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-113">As such, you may need to modify your system's Active Directory and Windows Firewall settings before making a WMI call.</span></span> <span data-ttu-id="fd8cd-114">Pour plus d’informations, consultez [configuration d’une connexion WMI à distance](connecting-to-wmi-remotely-starting-with-vista.md) et [résolution des problèmes liés à une connexion WMI à distance](troubleshooting-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fd8cd-114">For more information, see [Setting up a Remote WMI Connection](connecting-to-wmi-remotely-starting-with-vista.md) and [Troubleshooting a Remote WMI Connection](troubleshooting-a-remote-wmi-connection.md).</span></span>

-   <span data-ttu-id="fd8cd-115">Les paramètres DCOM corrects doivent être activés pour qu’une connexion à distance fonctionne.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-115">The correct DCOM settings must be enabled for a remote connection to work.</span></span> <span data-ttu-id="fd8cd-116">La modification des paramètres DCOM peut permettre aux utilisateurs avec des droits limités d’accéder à un ordinateur pour une connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-116">Changing DCOM settings can allow low rights users access to a computer for a remote connection.</span></span> <span data-ttu-id="fd8cd-117">Pour plus d’informations, consultez [sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fd8cd-117">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="fd8cd-118">En outre, dans certains cas, vous pouvez souhaiter exécuter WMI via un port fixe.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-118">In addition, there may be some circumstances in which you may wish to run WMI though a fixed port.</span></span> <span data-ttu-id="fd8cd-119">Pour ce faire, vous devez également modifier vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-119">To do this, you will also need to change your settings.</span></span> <span data-ttu-id="fd8cd-120">Pour plus d’informations, consultez [configuration d’un port fixe pour WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="fd8cd-120">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

## <a name="connecting-to-a-remote-computer"></a><span data-ttu-id="fd8cd-121">Connexion à un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="fd8cd-121">Connecting to a Remote Computer</span></span>

<span data-ttu-id="fd8cd-122">Le cœur de la connexion à un système distant avec WMI consiste à s’assurer que vous disposez des autorisations appropriées pour accéder au système et que votre connexion est correctement configurée.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-122">At its heart, connecting to a remote system with WMI consists of making sure that you have the appropriate permissions to access the system, and that your connection is properly configured.</span></span> <span data-ttu-id="fd8cd-123">Une fois que vous avez ces deux éléments, la connexion elle-même est relativement simple.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-123">Once you have those two elements, the connection itself is relatively simple.</span></span> <span data-ttu-id="fd8cd-124">Par exemple, si vous utilisez vos informations d’identification de sécurité par défaut, vous pouvez accéder à WMI sur un système distant à l’aide du code suivant :</span><span class="sxs-lookup"><span data-stu-id="fd8cd-124">For example, if you are using your default security credentials, you can access WMI on a remote system using the following code:</span></span>

<dl> <dt>

<span data-ttu-id="fd8cd-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Connexion à WMI à distance avec PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="fd8cd-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span></span>
</dt> <dd>

<span data-ttu-id="fd8cd-126">Utilisez le paramètre *-ComputerName* commun à la plupart des applets de commande WMI, telles que l’applet de commande- [WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="fd8cd-126">Use the *-ComputerName* parameter common to most WMI cmdlets, such as [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).</span></span>


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span data-ttu-id="fd8cd-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Connexion à WMI à distance avec VBScript](connecting-to-wmi-remotely-with-vbscript.md)</span><span class="sxs-lookup"><span data-stu-id="fd8cd-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md)</span></span>
</dt> <dd>

<span data-ttu-id="fd8cd-128">Utilisez un moniker qui contient le nom du système distant dans l’appel à [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="fd8cd-128">Use a moniker that contains the name of the remote system in the call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span data-ttu-id="fd8cd-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connexion à WMI à distance avec C #](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="fd8cd-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="fd8cd-130">Pour la version actuelle de l’interface managée WMI ([Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), utilisez l’objet [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) pour représenter une connexion à un hôte distant.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-130">For the current version of the WMI managed interface ([Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), use the [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object to represent a connection to a remote host.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span data-ttu-id="fd8cd-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connexion à WMI à distance avec C #](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="fd8cd-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="fd8cd-132">Pour la version V1 de l’interface managée WMI ([System. Management](/dotnet/api/system.management)), utilisez l’objet [ManagementScope](/dotnet/api/system.management.managementscope) pour représenter une connexion à un hôte distant.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-132">For the v1 version of the WMI managed interface ([System.Management](/dotnet/api/system.management)), use the [ManagementScope](/dotnet/api/system.management.managementscope) object to represent a connection to a remote host.</span></span>


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span data-ttu-id="fd8cd-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Exemple : obtention de données WMI à partir d’un ordinateur distant (C++)](example--getting-wmi-data-from-a-remote-computer.md)</span><span class="sxs-lookup"><span data-stu-id="fd8cd-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Example: Getting WMI Data from a Remote Computer (C++)](example--getting-wmi-data-from-a-remote-computer.md)</span></span>
</dt> <dd>

<span data-ttu-id="fd8cd-134">Utilisez la méthode [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) pour spécifier le nom de l’ordinateur distant dans le paramètre *strNetworkResource* .</span><span class="sxs-lookup"><span data-stu-id="fd8cd-134">Use the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method to specify the name of the remote computer in the *strNetworkResource* parameter.</span></span>


```CSharp
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTER_B\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
        );
```



</dd> </dl>

<span data-ttu-id="fd8cd-135">Les exemples de code précédents sont sans doute la connexion à distance la plus simple que vous pouvez effectuer avec WMI.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-135">The previous code samples are arguably the most basic remote connection you can perform with WMI.</span></span> <span data-ttu-id="fd8cd-136">Plus précisément, les exemples supposent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="fd8cd-136">Specifically, the samples assume the following:</span></span>

-   <span data-ttu-id="fd8cd-137">Vous êtes un administrateur sur la machine distante.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-137">You are an administrator on the remote machine.</span></span> <span data-ttu-id="fd8cd-138">En raison du [contrôle de compte d’utilisateur](/previous-versions/aa905108(v=msdn.10)), le compte sur le système distant doit être un compte de domaine dans le groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-138">Due to [User Account Control](/previous-versions/aa905108(v=msdn.10)), the account on the remote system must be a domain account in the Administrators group.</span></span> <span data-ttu-id="fd8cd-139">Pour plus d’informations, consultez contrôle de compte d’utilisateur et WMI.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-139">For more information, see User Account Control and WMI.</span></span>
-   <span data-ttu-id="fd8cd-140">Le mot de passe sur votre ordinateur local actuel n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-140">The password on your current local machine is not blank.</span></span> <span data-ttu-id="fd8cd-141">Il s’agit essentiellement d’une exigence de sécurité Windows que vous devez avoir connecté à votre système avec un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-141">This is essentially a Windows security requirement that you must have logged onto your system with a password.</span></span>
-   <span data-ttu-id="fd8cd-142">Vos ordinateurs locaux et distants se trouvent dans le même domaine.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-142">Both your local and remote computers are within the same domain.</span></span> <span data-ttu-id="fd8cd-143">Si vous avez besoin de franchir les limites d’un domaine, vous devez fournir des informations supplémentaires ou utiliser un modèle de programmation légèrement différent.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-143">If you need to cross domain boundaries, you would need to supply additional information or use a slightly different programming model.</span></span>
-   <span data-ttu-id="fd8cd-144">Vous utilisez votre propre compte pour accéder à la machine distante.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-144">You are using your own account to access the remote machine.</span></span> <span data-ttu-id="fd8cd-145">Si vous essayez d’accéder à un autre compte, vous devez fournir des informations d’identification supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-145">If you were trying to access a different account, you would need to supply additional credentials.</span></span> <span data-ttu-id="fd8cd-146">(Notez que la tentative d’accès à WMI localement avec des informations d’identification différentes de votre compte actuel n’est pas autorisée.)</span><span class="sxs-lookup"><span data-stu-id="fd8cd-146">(Note that trying to access WMI locally with credentials different than your current account is not permitted.)</span></span>
-   <span data-ttu-id="fd8cd-147">Les deux ordinateurs exécutent IPv6.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-147">Both computers are running IPv6.</span></span> <span data-ttu-id="fd8cd-148">WMI prend en charge les connexions aux ordinateurs exécutant IPv6.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-148">WMI supports connections to computers running IPv6.</span></span> <span data-ttu-id="fd8cd-149">Toutefois, votre ordinateur local et « ordinateur \_ B » doivent exécuter IPv6.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-149">However, both your local machine and "Computer\_B" must be running IPv6.</span></span> <span data-ttu-id="fd8cd-150">Les deux ordinateurs peuvent également exécuter IPv4.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-150">Either computer may be running IPv4 also.</span></span> <span data-ttu-id="fd8cd-151">Pour plus d’informations, consultez [prise en charge d’IPv6 et IPv6 dans WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="fd8cd-151">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>
-   <span data-ttu-id="fd8cd-152">Votre script n’a pas besoin de déléguer-autrement dit, il n’a pas besoin d’accéder à des ordinateurs distants supplémentaires par le biais de l’ordinateur distant ciblé.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-152">Your script does not need to delegate - that is, it does not need to access additional remote computers through the targeted remote computer.</span></span> <span data-ttu-id="fd8cd-153">Pour plus d’informations, consultez [délégation avec WMI](connecting-to-a-3rd-computer-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="fd8cd-153">For more information, see [Delegating with WMI](connecting-to-a-3rd-computer-delegation.md).</span></span>
-   <span data-ttu-id="fd8cd-154">Vous essayez d’effectuer un appel spécifique, plutôt que de créer un processus distant.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-154">You are trying to make a specific call, rather than creating a remote process.</span></span> <span data-ttu-id="fd8cd-155">Pour plus d’informations, consultez [création de processus à distance à l’aide de WMI](creating-processes-remotely.md).</span><span class="sxs-lookup"><span data-stu-id="fd8cd-155">For more information, see [Creating Processes Remotely using WMI](creating-processes-remotely.md).</span></span>

<span data-ttu-id="fd8cd-156">Avec ces restrictions à l’esprit, un appel WMI distant est très similaire à un appel WMI local. la seule différence réside dans le fait que vous devez spécifier le nom du système distant.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-156">With those restrictions in mind, a remote WMI call is very similar to a local WMI call - the only difference being that you must specify the name of the remote system.</span></span> <span data-ttu-id="fd8cd-157">Toutefois, vous pouvez choisir de modifier un grand nombre de ces fonctionnalités : en utilisant des informations d’identification différentes ou en acheminant votre appel via un ordinateur tiers, ou en accédant à un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="fd8cd-157">However, you may choose to change many of those features: using different credentials, or routing your call through a 3rd party computer, or accessing a different domain.</span></span>

 

 
