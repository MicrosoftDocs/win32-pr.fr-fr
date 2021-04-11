---
title: Améliorations de l’infrastructure du shell distant
description: Windows Remote Management version 2,0 (WinRM 2,0) offre de nombreuses améliorations de l’infrastructure de l’interpréteur de commandes à distance.
ms.assetid: b22693ba-fa43-44bb-9b2d-0c64fad6e3cc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c67752222f1ca969ea254164a25144168d1eb3
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2020
ms.locfileid: "104030721"
---
# <a name="remote-shell-infrastructure-improvements"></a><span data-ttu-id="14b04-103">Améliorations de l’infrastructure du shell distant</span><span class="sxs-lookup"><span data-stu-id="14b04-103">Remote Shell Infrastructure Improvements</span></span>

<span data-ttu-id="14b04-104">Windows Remote Management version 2,0 (WinRM 2,0) offre de nombreuses améliorations de l’infrastructure de l’interpréteur de commandes à distance.</span><span class="sxs-lookup"><span data-stu-id="14b04-104">Windows Remote Management version 2.0 (WinRM 2.0) offers many remote shell infrastructure improvements.</span></span> <span data-ttu-id="14b04-105">Les rubriques suivantes décrivent ces améliorations en détail :</span><span class="sxs-lookup"><span data-stu-id="14b04-105">The following topics describe these improvements in detail:</span></span>

-   [<span data-ttu-id="14b04-106">Prise en charge de plusieurs tronçons</span><span class="sxs-lookup"><span data-stu-id="14b04-106">Multi-Hop Support</span></span>](multi-hop-support.md)
-   [<span data-ttu-id="14b04-107">Gestion des quotas pour les shells distants</span><span class="sxs-lookup"><span data-stu-id="14b04-107">Quota Management for Remote Shells</span></span>](quotas.md)

<span data-ttu-id="14b04-108">L’une des améliorations apportées à l’infrastructure de l’interpréteur de commandes distant WinRM est l’ajout d’un gestionnaire de Shell plus robuste qui gère les informations de l’interpréteur de commandes spécifiques à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="14b04-108">One of the improvements to the WinRM remote shell infrastructure is the addition of a more robust shell manager that maintains user-specific shell information.</span></span> <span data-ttu-id="14b04-109">Les utilisateurs WinRM peuvent créer des shells sur des ordinateurs distants pour exécuter des commandes ou des scripts.</span><span class="sxs-lookup"><span data-stu-id="14b04-109">WinRM users can create shells on remote computers to run commands or scripts.</span></span> <span data-ttu-id="14b04-110">En outre, les utilisateurs peuvent créer plusieurs shells sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="14b04-110">In addition, users can create multiple shells on a computer.</span></span> <span data-ttu-id="14b04-111">Les utilisateurs et les administrateurs doivent tous deux pouvoir gérer des shells.</span><span class="sxs-lookup"><span data-stu-id="14b04-111">Users and administrators both need the ability to manage shells.</span></span> <span data-ttu-id="14b04-112">Les utilisateurs peuvent énumérer, obtenir et supprimer les shells qu’ils ont créés.</span><span class="sxs-lookup"><span data-stu-id="14b04-112">Users can enumerate, get, and delete the shells that they have created.</span></span> <span data-ttu-id="14b04-113">Les administrateurs peuvent énumérer tous les shells actifs et récupérer des détails sur des shells spécifiques sur un hôte local ou distant.</span><span class="sxs-lookup"><span data-stu-id="14b04-113">Administrators can enumerate over all active shells and retrieve details about specific shells on a local or remote host.</span></span> <span data-ttu-id="14b04-114">Les administrateurs peuvent également supprimer des shells actifs sur un hôte local ou distant.</span><span class="sxs-lookup"><span data-stu-id="14b04-114">Administrators can also delete any active shells on a local or remote host.</span></span>

<span data-ttu-id="14b04-115">Lorsqu’un utilisateur ou un administrateur énumère les interpréteurs de commande actifs, les informations suivantes peuvent être retournées par le service WinRM.</span><span class="sxs-lookup"><span data-stu-id="14b04-115">When a user or administrator enumerates the active shells, the following information can be returned by the WinRM service.</span></span>

<dl> <dt>

<span data-ttu-id="14b04-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId</span><span class="sxs-lookup"><span data-stu-id="14b04-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId</span></span>
</dt> <dd>

<span data-ttu-id="14b04-117">Spécifie l’identificateur unique de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="14b04-117">Specifies the unique identifier for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="14b04-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Variables d’environnement</span><span class="sxs-lookup"><span data-stu-id="14b04-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Environment variables</span></span>
</dt> <dd>

<span data-ttu-id="14b04-119">Spécifie toutes les variables d’environnement définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="14b04-119">Specifies any environment variables set by the user.</span></span>

</dd> <dt>

<span data-ttu-id="14b04-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="14b04-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span></span>
</dt> <dd>

<span data-ttu-id="14b04-121">Spécifie le répertoire de démarrage de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="14b04-121">Specifies the starting directory for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="14b04-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>URI</span><span class="sxs-lookup"><span data-stu-id="14b04-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI</span></span>
</dt> <dd>

<span data-ttu-id="14b04-123">Spécifie l’URI de ressource pour l’opération de Shell.</span><span class="sxs-lookup"><span data-stu-id="14b04-123">Specifies the resource URI for the shell operation.</span></span> <span data-ttu-id="14b04-124">L’URI de ressource peut être utilisé pour récupérer la configuration de plug-in qui est spécifique à l’instance de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="14b04-124">The resource URI can be used to retrieve plug-in configuration that is specific to the shell instance.</span></span>

</dd> <dt>

<span data-ttu-id="14b04-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="14b04-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="14b04-126">Spécifie la durée maximale, en millisecondes, pendant laquelle l’interpréteur de commandes restera ouvert sans aucune demande.</span><span class="sxs-lookup"><span data-stu-id="14b04-126">Specifies the maximum duration, in milliseconds, that the shell will stay open without any request.</span></span>

</dd> <dt>

<span data-ttu-id="14b04-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams</span><span class="sxs-lookup"><span data-stu-id="14b04-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams</span></span>
</dt> <dd>

<span data-ttu-id="14b04-128">Spécifie les flux d’entrée pour l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="14b04-128">Specifies the input streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="14b04-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams</span><span class="sxs-lookup"><span data-stu-id="14b04-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams</span></span>
</dt> <dd>

<span data-ttu-id="14b04-130">Spécifie les flux de sortie de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="14b04-130">Specifies the output streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="14b04-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Heure de création de l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="14b04-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Shell creation time</span></span>
</dt> <dd>

<span data-ttu-id="14b04-132">Spécifie l’horodateur de création de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="14b04-132">Specifies the creation timestamp for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="14b04-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime</span><span class="sxs-lookup"><span data-stu-id="14b04-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime</span></span>
</dt> <dd>

<span data-ttu-id="14b04-134">Spécifie la durée, en millisecondes, pendant laquelle l’interpréteur de commandes a été inactif.</span><span class="sxs-lookup"><span data-stu-id="14b04-134">Specifies the duration, in milliseconds, that the shell has been idle.</span></span>

</dd> <dt>

<span data-ttu-id="14b04-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>IDutilisateur</span><span class="sxs-lookup"><span data-stu-id="14b04-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserId</span></span>
</dt> <dd>

<span data-ttu-id="14b04-136">Spécifie l’ID utilisateur.</span><span class="sxs-lookup"><span data-stu-id="14b04-136">Specifies the user ID.</span></span>

</dd> <dt>

<span data-ttu-id="14b04-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Nom d’hôte ou adresse IP</span><span class="sxs-lookup"><span data-stu-id="14b04-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Hostname or IP address</span></span>
</dt> <dd>

<span data-ttu-id="14b04-138">Spécifie le nom d’hôte ou l’adresse IP de l’ordinateur qui a créé l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="14b04-138">Specifies either the host name or IP address of the computer that created the shell.</span></span>

</dd> <dt>

<span data-ttu-id="14b04-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Utilisation de la mémoire de l’environnement</span><span class="sxs-lookup"><span data-stu-id="14b04-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Shell memory usage</span></span>
</dt> <dd>

<span data-ttu-id="14b04-140">Spécifie la quantité de mémoire qui a été utilisée par l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="14b04-140">Specifies the amount of memory that has been used by the shell.</span></span>

</dd> <dt>

<span data-ttu-id="14b04-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Nombre de processus</span><span class="sxs-lookup"><span data-stu-id="14b04-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Number of processes</span></span>
</dt> <dd>

<span data-ttu-id="14b04-142">Spécifie le nombre de processus qui ont été créés par l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="14b04-142">Specifies the number of processes that have been created by the shell.</span></span>

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a><span data-ttu-id="14b04-143">Énumération d’un interpréteur de commandes sur un hôte local</span><span class="sxs-lookup"><span data-stu-id="14b04-143">Enumerating a Shell on a Local Host</span></span>

<span data-ttu-id="14b04-144">La commande suivante montre comment utiliser l’utilitaire WinRM pour énumérer des shells sur un client WinRM : **WinRM Enumerate Shell**.</span><span class="sxs-lookup"><span data-stu-id="14b04-144">The following command demonstrates how to use the winrm utility to enumerate shells on a WinRM client: **winrm enumerate shell**.</span></span>

<span data-ttu-id="14b04-145">L’exemple de texte suivant affiche la sortie de l’énumération de l’interpréteur de commandes :</span><span class="sxs-lookup"><span data-stu-id="14b04-145">The following text-based example displays the output for shell enumeration:</span></span>

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S

Shell
    ShellId = EE3F11CE-FB3C-4C4E-B113-6F4D643C97D8
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M46S
    ShellInactivity = P0DT0H0M45S
    MemoryUsed = 48MB
    ChildProcesses = 0

Shell
    ShellId = 8FD7F2C4-A434-4D58-A7E8-46F8BF202D0B
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M47S
    ShellInactivity = P0DT0H0M47S
    MemoryUsed = 48MB
    ChildProcesses = 0
```

<span data-ttu-id="14b04-146">Pour plus d’informations, consultez l’aide en ligne fournie en exécutant la commande suivante : **WinRM Enumerate- ?**.</span><span class="sxs-lookup"><span data-stu-id="14b04-146">For more information, see the online help provided by running the following command: **winrm enumerate -?**.</span></span>

## <a name="retrieving-information-about-a-specific-shell"></a><span data-ttu-id="14b04-147">Récupération d’informations sur un interpréteur de commandes spécifique</span><span class="sxs-lookup"><span data-stu-id="14b04-147">Retrieving Information About a Specific Shell</span></span>

<span data-ttu-id="14b04-148">Un administrateur ou un utilisateur peut également utiliser l’identificateur ShellId pour récupérer des informations sur l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="14b04-148">An administrator or user can also use the ShellId identifier to retrieve information about the shell.</span></span> <span data-ttu-id="14b04-149">La commande suivante montre comment utiliser l’utilitaire WinRM pour obtenir des informations sur un interpréteur de commandes spécifique : **WinRM obtenir l’interpréteur de commandes ? ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.</span><span class="sxs-lookup"><span data-stu-id="14b04-149">The following command demonstrates how to use the winrm utility to get information about a specific shell: **winrm get shell?ShellId=0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.</span></span>

<span data-ttu-id="14b04-150">L’exemple de texte suivant affiche la sortie des informations de l’interpréteur de commandes :</span><span class="sxs-lookup"><span data-stu-id="14b04-150">The following text-based example displays the output for shell information:</span></span>

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S
```

<span data-ttu-id="14b04-151">Pour plus d’informations, consultez l’aide en ligne fournie par la commande suivante : **WinRM obtenir- ?**.</span><span class="sxs-lookup"><span data-stu-id="14b04-151">For more information, see the online help provided by the following command: **winrm get -?**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14b04-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14b04-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14b04-153">Prise en charge de plusieurs tronçons</span><span class="sxs-lookup"><span data-stu-id="14b04-153">Multi-Hop Support</span></span>](multi-hop-support.md)
</dt> <dt>

[<span data-ttu-id="14b04-154">Gestion des quotas pour les shells distants</span><span class="sxs-lookup"><span data-stu-id="14b04-154">Quota Management for Remote Shells</span></span>](quotas.md)
</dt> <dt>

[<span data-ttu-id="14b04-155">Référence managée pour les commandes WS-Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="14b04-155">Managed Reference for WS-Management PowerShell Commands</span></span>](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




