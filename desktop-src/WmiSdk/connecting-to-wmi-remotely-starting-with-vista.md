---
description: La connexion à un espace de noms WMI sur un ordinateur distant peut nécessiter la modification des paramètres du pare-feu Windows, du contrôle de compte d’utilisateur (UAC, User Account Control), de DCOM ou de Common Information Model Object Manager (CIMOM).
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: Configuration d’une connexion WMI à distance
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6ee254e12ecd806cd286d4a55746e203a3136b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528617"
---
# <a name="setting-up-a-remote-wmi-connection"></a><span data-ttu-id="491d1-103">Configuration d’une connexion WMI à distance</span><span class="sxs-lookup"><span data-stu-id="491d1-103">Setting up a Remote WMI Connection</span></span>

<span data-ttu-id="491d1-104">La connexion à un espace de noms WMI sur un ordinateur distant peut nécessiter la modification des paramètres du [pare-feu Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), du [contrôle de compte d’utilisateur (UAC, User Account Control)](/previous-versions/aa905108(v=msdn.10)), de DCOM ou de Common Information Model Object Manager (CIMOM).</span><span class="sxs-lookup"><span data-stu-id="491d1-104">Connecting to a WMI namespace on a remote computer may require that you change the settings for [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM, or Common Information Model Object Manager (CIMOM).</span></span>

<span data-ttu-id="491d1-105">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="491d1-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="491d1-106">Paramètres du pare-feu Windows</span><span class="sxs-lookup"><span data-stu-id="491d1-106">Windows Firewall Settings</span></span>](#windows-firewall-settings)
-   [<span data-ttu-id="491d1-107">Paramètres du contrôle de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="491d1-107">User Account Control Settings</span></span>](#user-account-control-settings)
-   [<span data-ttu-id="491d1-108">Paramètres DCOM</span><span class="sxs-lookup"><span data-stu-id="491d1-108">DCOM Settings</span></span>](#dcom-settings)
-   [<span data-ttu-id="491d1-109">Paramètres CIMOM</span><span class="sxs-lookup"><span data-stu-id="491d1-109">CIMOM Settings</span></span>](#cimom-settings)
-   [<span data-ttu-id="491d1-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="491d1-110">Related topics</span></span>](#related-topics)

## <a name="windows-firewall-settings"></a><span data-ttu-id="491d1-111">Paramètres de pare-feu Windows</span><span class="sxs-lookup"><span data-stu-id="491d1-111">Windows Firewall Settings</span></span>

<span data-ttu-id="491d1-112">Les paramètres WMI pour les paramètres du pare-feu Windows activent uniquement les connexions WMI, plutôt que d’autres applications DCOM.</span><span class="sxs-lookup"><span data-stu-id="491d1-112">WMI settings for Windows Firewall settings enable only WMI connections, rather than other DCOM applications as well.</span></span>

<span data-ttu-id="491d1-113">Une exception doit être définie dans le pare-feu pour WMI sur l’ordinateur cible distant.</span><span class="sxs-lookup"><span data-stu-id="491d1-113">An exception must be set in the firewall for WMI on the remote target computer.</span></span> <span data-ttu-id="491d1-114">L’exception pour WMI permet à WMI de recevoir des connexions à distance et des rappels asynchrones pour Unsecapp.exe.</span><span class="sxs-lookup"><span data-stu-id="491d1-114">The exception for WMI allows WMI to receive remote connections and asynchronous callbacks to Unsecapp.exe.</span></span> <span data-ttu-id="491d1-115">Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="491d1-115">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="491d1-116">Si une application cliente crée son propre récepteur, ce récepteur doit être explicitement ajouté aux exceptions de pare-feu pour permettre aux rappels de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="491d1-116">If a client application creates its own sink, that sink must be explicitly added to the firewall exceptions to allow callbacks to succeed.</span></span>

<span data-ttu-id="491d1-117">L’exception pour WMI fonctionne également si WMI a été démarré avec un port fixe, à l’aide de la commande **winmgmt/standalonehost** .</span><span class="sxs-lookup"><span data-stu-id="491d1-117">The exception for WMI also works if WMI has been started with a fixed port, using the **winmgmt /standalonehost** command.</span></span> <span data-ttu-id="491d1-118">Pour plus d’informations, consultez [configuration d’un port fixe pour WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="491d1-118">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="491d1-119">Vous pouvez activer ou désactiver le trafic WMI par le biais de l’interface utilisateur du pare-feu Windows.</span><span class="sxs-lookup"><span data-stu-id="491d1-119">You can enable or disable WMI traffic through the Windows Firewall UI.</span></span>

<span data-ttu-id="491d1-120">**Pour activer ou désactiver le trafic WMI à l’aide de l’interface utilisateur du pare-feu**</span><span class="sxs-lookup"><span data-stu-id="491d1-120">**To enable or disable WMI traffic using firewall UI**</span></span>

1.  <span data-ttu-id="491d1-121">Dans le **panneau de configuration**, cliquez sur **sécurité** , puis sur **pare-feu Windows**.</span><span class="sxs-lookup"><span data-stu-id="491d1-121">In the **Control Panel**, click **Security** and then click **Windows Firewall**.</span></span>
2.  <span data-ttu-id="491d1-122">Cliquez sur **modifier les paramètres** , puis sur l’onglet **exceptions** .</span><span class="sxs-lookup"><span data-stu-id="491d1-122">Click **Change Settings** and then click the **Exceptions** tab.</span></span>
3.  <span data-ttu-id="491d1-123">Dans la fenêtre exceptions, activez la case à cocher **Windows Management Instrumentation (WMI)** pour activer le trafic WMI via le pare-feu.</span><span class="sxs-lookup"><span data-stu-id="491d1-123">In the Exceptions window, select the check box for **Windows Management Instrumentation (WMI)** to enable WMI traffic through the firewall.</span></span> <span data-ttu-id="491d1-124">Pour désactiver le trafic WMI, désactivez la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="491d1-124">To disable WMI traffic, clear the check box.</span></span>

<span data-ttu-id="491d1-125">Vous pouvez activer ou désactiver le trafic WMI via le pare-feu à partir de l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="491d1-125">You can enable or disable WMI traffic through the firewall at the command prompt.</span></span>

<span data-ttu-id="491d1-126">**Pour activer ou désactiver le trafic WMI à l’invite de commandes à l’aide du groupe de règles WMI**</span><span class="sxs-lookup"><span data-stu-id="491d1-126">**To enable or disable WMI traffic at command prompt using WMI rule group**</span></span>

-   <span data-ttu-id="491d1-127">Utilisez les commandes suivantes à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="491d1-127">Use the following commands at a command prompt.</span></span> <span data-ttu-id="491d1-128">Tapez la commande suivante pour activer le trafic WMI via le pare-feu.</span><span class="sxs-lookup"><span data-stu-id="491d1-128">Type the following to enable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="491d1-129">**netsh advfirewall firewall set Rule Group = « Windows Management Instrumentation (WMI) » New Enable = Oui**</span><span class="sxs-lookup"><span data-stu-id="491d1-129">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes**</span></span>

    <span data-ttu-id="491d1-130">Tapez la commande suivante pour désactiver le trafic WMI via le pare-feu.</span><span class="sxs-lookup"><span data-stu-id="491d1-130">Type the following command to disable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="491d1-131">**netsh advfirewall firewall set Rule Group = « Windows Management Instrumentation (WMI) » New Enable = no**</span><span class="sxs-lookup"><span data-stu-id="491d1-131">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=no**</span></span>

<span data-ttu-id="491d1-132">Au lieu d’utiliser la commande de groupe de règles WMI unique, vous pouvez également utiliser des commandes individuelles pour chaque DCOM, service WMI et récepteur.</span><span class="sxs-lookup"><span data-stu-id="491d1-132">Rather than using the single WMI rule group command, you also can use individual commands for each of the DCOM, WMI service, and sink.</span></span>

<span data-ttu-id="491d1-133">**Pour activer le trafic WMI à l’aide de règles distinctes pour DCOM, WMI, le récepteur de rappel et les connexions sortantes**</span><span class="sxs-lookup"><span data-stu-id="491d1-133">**To enable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="491d1-134">Pour établir une exception de pare-feu pour le port DCOM 135, utilisez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="491d1-134">To establish a firewall exception for DCOM port 135, use the following command.</span></span>

    <span data-ttu-id="491d1-135">**netsh advfirewall Firewall Add Rule dir = in Name = "DCOM" programme =% systemroot% \\ system32 \\svchost.exe service = RPCSS action = allow Protocol = TCP localPort = 135**</span><span class="sxs-lookup"><span data-stu-id="491d1-135">**netsh advfirewall firewall add rule dir=in name="DCOM" program=%systemroot%\\system32\\svchost.exe service=rpcss action=allow protocol=TCP localport=135**</span></span>

2.  <span data-ttu-id="491d1-136">Pour établir une exception de pare-feu pour le service WMI, utilisez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="491d1-136">To establish a firewall exception for the WMI service, use the following command.</span></span>

    <span data-ttu-id="491d1-137">**netsh advfirewall Firewall Add Rule dir = in Name = "WMI" Program =% systemroot% \\ system32 \\svchost.exe service = WinMgmt action = autoriser Protocol = TCP localPort = any**</span><span class="sxs-lookup"><span data-stu-id="491d1-137">**netsh advfirewall firewall add rule dir=in name ="WMI" program=%systemroot%\\system32\\svchost.exe service=winmgmt action = allow protocol=TCP localport=any**</span></span>

3.  <span data-ttu-id="491d1-138">Pour établir une exception de pare-feu pour le récepteur qui reçoit des rappels à partir d’un ordinateur distant, utilisez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="491d1-138">To establish a firewall exception for the sink that receives callbacks from a remote computer, use the following command.</span></span>

    <span data-ttu-id="491d1-139">**netsh advfirewall Firewall Add Rule dir = in Name = "UnsecApp" programme =% systemroot% \\ system32 \\ WBEM \\unsecapp.exe action = allow**</span><span class="sxs-lookup"><span data-stu-id="491d1-139">**netsh advfirewall firewall add rule dir=in name ="UnsecApp" program=%systemroot%\\system32\\wbem\\unsecapp.exe action=allow**</span></span>

4.  <span data-ttu-id="491d1-140">Pour établir une exception de pare-feu pour les connexions sortantes à un ordinateur distant avec lequel l’ordinateur local communique de façon asynchrone, utilisez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="491d1-140">To establish a firewall exception for outgoing connections to a remote computer that the local computer is communicating with asynchronously, use the following command.</span></span>

    <span data-ttu-id="491d1-141">**netsh advfirewall Firewall Add Rule dir = out Name = "WMI \_ out" programme =% systemroot% \\ system32 \\svchost.exe service = WinMgmt action = autoriser Protocol = TCP localPort = any**</span><span class="sxs-lookup"><span data-stu-id="491d1-141">**netsh advfirewall firewall add rule dir=out name ="WMI\_OUT" program=%systemroot%\\system32\\svchost.exe service=winmgmt action=allow protocol=TCP localport=any**</span></span>

<span data-ttu-id="491d1-142">Pour désactiver les exceptions de pare-feu séparément, utilisez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="491d1-142">To disable the firewall exceptions separately, use the following commands.</span></span>

<span data-ttu-id="491d1-143">**Pour désactiver le trafic WMI à l’aide de règles distinctes pour DCOM, WMI, le récepteur de rappel et les connexions sortantes**</span><span class="sxs-lookup"><span data-stu-id="491d1-143">**To disable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="491d1-144">Pour désactiver l’exception DCOM.</span><span class="sxs-lookup"><span data-stu-id="491d1-144">To disable the DCOM exception.</span></span>

    <span data-ttu-id="491d1-145">**nom de la règle de suppression du pare-feu netsh advfirewall = « DCOM »**</span><span class="sxs-lookup"><span data-stu-id="491d1-145">**netsh advfirewall firewall delete rule name="DCOM"**</span></span>

2.  <span data-ttu-id="491d1-146">Pour désactiver l’exception du service WMI.</span><span class="sxs-lookup"><span data-stu-id="491d1-146">To disable the WMI service exception.</span></span>

    <span data-ttu-id="491d1-147">**nom de la règle de suppression du pare-feu netsh advfirewall = « WMI »**</span><span class="sxs-lookup"><span data-stu-id="491d1-147">**netsh advfirewall firewall delete rule name="WMI"**</span></span>

3.  <span data-ttu-id="491d1-148">Pour désactiver l’exception du récepteur.</span><span class="sxs-lookup"><span data-stu-id="491d1-148">To disable the sink exception.</span></span>

    <span data-ttu-id="491d1-149">**nom de la règle de suppression du pare-feu netsh advfirewall = "UnsecApp"**</span><span class="sxs-lookup"><span data-stu-id="491d1-149">**netsh advfirewall firewall delete rule name="UnsecApp"**</span></span>

4.  <span data-ttu-id="491d1-150">Pour désactiver l’exception sortante.</span><span class="sxs-lookup"><span data-stu-id="491d1-150">To disable the outgoing exception.</span></span>

    <span data-ttu-id="491d1-151">**nom de la règle de suppression du pare-feu netsh advfirewall = « WMI \_ out »**</span><span class="sxs-lookup"><span data-stu-id="491d1-151">**netsh advfirewall firewall delete rule name="WMI\_OUT"**</span></span>

## <a name="user-account-control-settings"></a><span data-ttu-id="491d1-152">Paramètres du contrôle de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="491d1-152">User Account Control Settings</span></span>

<span data-ttu-id="491d1-153">Le filtrage des jetons d’accès du contrôle de compte d’utilisateur peut avoir un impact sur les opérations autorisées dans les espaces de noms WMI ou sur les données retournées.</span><span class="sxs-lookup"><span data-stu-id="491d1-153">User Account Control (UAC) access-token filtering can affect which operations are allowed in WMI namespaces or what data is returned.</span></span> <span data-ttu-id="491d1-154">Sous UAC, tous les comptes du groupe Administrateurs local s’exécutent avec un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly)utilisateur standard, également appelé filtrage des jetons d’accès UAC.</span><span class="sxs-lookup"><span data-stu-id="491d1-154">Under UAC, all accounts in the local Administrators group run with a standard user [*access token*](/windows/desktop/SecGloss/a-gly), also known as UAC access-token filtering.</span></span> <span data-ttu-id="491d1-155">Un compte d’administrateur peut exécuter un script avec privilèges élevés, « exécuter en tant qu’administrateur ».</span><span class="sxs-lookup"><span data-stu-id="491d1-155">An administrator account can run a script with an elevated privilege—"Run as Administrator".</span></span>

<span data-ttu-id="491d1-156">Lorsque vous n’êtes pas connecté au compte administrateur intégré, le contrôle de compte d’utilisateur affecte les connexions à un ordinateur distant différemment selon que les deux ordinateurs se trouvent dans un domaine ou un groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="491d1-156">When you are not connecting to the built-in Administrator account, UAC affects connections to a remote computer differently depending on whether the two computers are in a domain or a workgroup.</span></span> <span data-ttu-id="491d1-157">Pour plus d’informations sur UAC et les connexions à distance, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="491d1-157">For more information about UAC and remote connections, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="dcom-settings"></a><span data-ttu-id="491d1-158">Paramètres DCOM</span><span class="sxs-lookup"><span data-stu-id="491d1-158">DCOM Settings</span></span>

<span data-ttu-id="491d1-159">Pour plus d’informations sur les paramètres DCOM, consultez [sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="491d1-159">For more information on DCOM settings, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span> <span data-ttu-id="491d1-160">Toutefois, le contrôle de compte d’utilisateur affecte les connexions pour les comptes d’utilisateurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="491d1-160">However, UAC affects connections for nondomain user accounts.</span></span> <span data-ttu-id="491d1-161">Si vous vous connectez à un ordinateur distant à l’aide d’un compte d’utilisateur qui n’est pas un compte de domaine inclus dans le groupe Administrateurs local de l’ordinateur distant, vous devez accorder explicitement les droits d’accès et d’activation DCOM à distance au compte.</span><span class="sxs-lookup"><span data-stu-id="491d1-161">If you connect to a remote computer using a nondomain user account included in the local Administrators group of the remote computer, then you must explicitly grant remote DCOM access, activation, and launch rights to the account.</span></span>

## <a name="cimom-settings"></a><span data-ttu-id="491d1-162">Paramètres CIMOM</span><span class="sxs-lookup"><span data-stu-id="491d1-162">CIMOM Settings</span></span>

<span data-ttu-id="491d1-163">Les paramètres CIMOM doivent être mis à jour si la connexion à distance se fait entre des ordinateurs qui n’ont pas de relation d’approbation ; dans le cas contraire, une connexion asynchrone échoue.</span><span class="sxs-lookup"><span data-stu-id="491d1-163">The CIMOM settings need to be updated if the remote connection is between computers that do not have a trust relationship; otherwise, an asynchronous connection will fail.</span></span> <span data-ttu-id="491d1-164">Ce paramètre ne doit pas être modifié pour les ordinateurs situés dans le même domaine ou dans des domaines approuvés.</span><span class="sxs-lookup"><span data-stu-id="491d1-164">This setting should not be modified for computers in the same domain or in trusted domains.</span></span>

<span data-ttu-id="491d1-165">L’entrée de Registre suivante doit être modifiée pour permettre les rappels anonymes :</span><span class="sxs-lookup"><span data-stu-id="491d1-165">The following registry entry needs to be modified to allow anonymous callbacks:</span></span>

<span data-ttu-id="491d1-166">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**</span><span class="sxs-lookup"><span data-stu-id="491d1-166">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**AllowAnonymousCallback**</span></span><dl> <dt>

               Data type
</dt> <dd>               <span data-ttu-id="491d1-167">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="491d1-167">REG\_DWORD</span></span></dd> </dl>

<span data-ttu-id="491d1-168">Si la valeur **AllowAnonymousCallback** est définie sur 0, le service WMI empêche les rappels anonymes sur le client.</span><span class="sxs-lookup"><span data-stu-id="491d1-168">If the **AllowAnonymousCallback** value is set to 0, the WMI service prevents anonymous callbacks to the client.</span></span> <span data-ttu-id="491d1-169">Si la valeur est définie sur 1, le service WMI autorise les rappels anonymes au client.</span><span class="sxs-lookup"><span data-stu-id="491d1-169">If the value is set to 1, the WMI service allows anonymous callbacks to the client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="491d1-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="491d1-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="491d1-171">Connexion à WMI sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="491d1-171">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
