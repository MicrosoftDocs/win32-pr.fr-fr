---
title: Gestion des quotas pour les shells distants
description: La gestion des quotas permet aux utilisateurs de gérer plus efficacement les ressources système.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1310efd37b913ae0bf8394015f6df792711ac6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310921"
---
# <a name="quota-management-for-remote-shells"></a><span data-ttu-id="e5b34-103">Gestion des quotas pour les shells distants</span><span class="sxs-lookup"><span data-stu-id="e5b34-103">Quota Management for Remote Shells</span></span>

<span data-ttu-id="e5b34-104">La gestion des quotas permet aux utilisateurs de gérer plus efficacement les ressources système.</span><span class="sxs-lookup"><span data-stu-id="e5b34-104">Quota management allows users to manage system resources more efficiently.</span></span> <span data-ttu-id="e5b34-105">Windows Remote Management (WinRM) a ajouté un ensemble spécifique de quotas qui offrent une meilleure qualité de service, permettent d’éviter des problèmes de déni de service et d’allouer des ressources serveur à des utilisateurs simultanés.</span><span class="sxs-lookup"><span data-stu-id="e5b34-105">Windows Remote Management (WinRM) has added a specific set of quotas that provide a better quality of service, help prevent denial of service issues, and allocate server resources to concurrent users.</span></span> <span data-ttu-id="e5b34-106">L’ensemble de quotas WinRM est basé sur l’infrastructure de quota qui est implémentée pour le service Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="e5b34-106">The WinRM quota set is based on the quota infrastructure that is implemented for the Internet Information Services (IIS) service.</span></span>

<span data-ttu-id="e5b34-107">L’implémentation de quotas permet d’éviter une dégradation des performances et des problèmes de déni de service en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="e5b34-107">Implementing quotas will help to prevent performance degradation and denial of service issues by doing the following:</span></span>

-   <span data-ttu-id="e5b34-108">Limitation du nombre de shells et de processus de Shell qu’un utilisateur peut créer</span><span class="sxs-lookup"><span data-stu-id="e5b34-108">Limiting the number of shells and shell processes that a user can create</span></span>
-   <span data-ttu-id="e5b34-109">Limitation du nombre maximal d’utilisateurs simultanés</span><span class="sxs-lookup"><span data-stu-id="e5b34-109">Limiting the maximum number of concurrent users</span></span>
-   <span data-ttu-id="e5b34-110">Gestion de la quantité de mémoire allouée à un interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="e5b34-110">Managing the amount of memory that is allocated to a shell</span></span>
-   <span data-ttu-id="e5b34-111">Définition d’un délai d’attente pour les shells inactifs</span><span class="sxs-lookup"><span data-stu-id="e5b34-111">Setting a time-out for shells that are inactive</span></span>

## <a name="quota-settings"></a><span data-ttu-id="e5b34-112">Paramètres de quota</span><span class="sxs-lookup"><span data-stu-id="e5b34-112">Quota Settings</span></span>

<span data-ttu-id="e5b34-113">Les quotas suivants doivent être appliqués pour la gestion des shells distants.</span><span class="sxs-lookup"><span data-stu-id="e5b34-113">The following quotas need to be enforced for remote shell management.</span></span> <span data-ttu-id="e5b34-114">Ces quotas peuvent être configurés via l’utilitaire WinRM ou via les paramètres de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e5b34-114">These quotas can be configured through the winrm utility or through Group Policy settings.</span></span> <span data-ttu-id="e5b34-115">Les paramètres configurés par un stratégie de groupe remplacent les quotas définis par l’utilitaire WinRM.</span><span class="sxs-lookup"><span data-stu-id="e5b34-115">Settings configured by a Group Policy supersede the quotas set by the winrm utility.</span></span> <span data-ttu-id="e5b34-116">Pour plus d’informations sur la définition de stratégies de groupe pour WinRM, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="e5b34-116">For more information about setting Group Policies for WinRM, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<dl> <dt>

<span data-ttu-id="e5b34-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="e5b34-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="e5b34-118">Durée maximale, en millisecondes, avant la suppression d’un shell distant inactif.</span><span class="sxs-lookup"><span data-stu-id="e5b34-118">The maximum time in milliseconds before an inactive remote shell is deleted.</span></span> <span data-ttu-id="e5b34-119">La valeur par défaut est 180000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="e5b34-119">The default is 180000 milliseconds.</span></span> <span data-ttu-id="e5b34-120">La durée minimale est de 1000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="e5b34-120">The minimum time is 1000 milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="e5b34-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell</span><span class="sxs-lookup"><span data-stu-id="e5b34-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell</span></span>
</dt> <dd>

<span data-ttu-id="e5b34-122">Nombre maximal de processus autorisés par Shell, y compris les processus enfants de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="e5b34-122">The maximum number of processes allowed per shell, including the shell's child processes.</span></span> <span data-ttu-id="e5b34-123">La valeur par défaut est 25.</span><span class="sxs-lookup"><span data-stu-id="e5b34-123">The default is 25.</span></span>

</dd> <dt>

<span data-ttu-id="e5b34-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB</span><span class="sxs-lookup"><span data-stu-id="e5b34-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB</span></span>
</dt> <dd>

<span data-ttu-id="e5b34-125">Quantité maximale de mémoire allouée par Shell, y compris les processus enfants de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="e5b34-125">The maximum amount of memory allocated per shell, including the shell's child processes.</span></span> <span data-ttu-id="e5b34-126">La valeur par défaut est 1024 Mo.</span><span class="sxs-lookup"><span data-stu-id="e5b34-126">The default is 1024 MB.</span></span>

> [!Note]  
> <span data-ttu-id="e5b34-127">Le comportement n’est pas pris en charge si MaxMemoryPerShellMB est défini sur une valeur inférieure à la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e5b34-127">The behavior is unsupported if the MaxMemoryPerShellMB is set to a value that is less than the default.</span></span>

 

</dd> <dt>

<span data-ttu-id="e5b34-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser</span><span class="sxs-lookup"><span data-stu-id="e5b34-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser</span></span>
</dt> <dd>

<span data-ttu-id="e5b34-129">Nombre maximal de shells par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e5b34-129">The maximum number of shells per user.</span></span> <span data-ttu-id="e5b34-130">La valeur par défaut est 30.</span><span class="sxs-lookup"><span data-stu-id="e5b34-130">The default is 30.</span></span>

</dd> <dt>

<span data-ttu-id="e5b34-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="e5b34-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers</span></span>
</dt> <dd>

<span data-ttu-id="e5b34-132">Nombre maximal d’utilisateurs simultanés qui peuvent ouvrir des shells.</span><span class="sxs-lookup"><span data-stu-id="e5b34-132">The maximum number of concurrent users who can open shells.</span></span> <span data-ttu-id="e5b34-133">La valeur par défaut est de 10.</span><span class="sxs-lookup"><span data-stu-id="e5b34-133">The default is 10.</span></span>

</dd> </dl>

## <a name="deprecated-quotas"></a><span data-ttu-id="e5b34-134">Quotas déconseillés</span><span class="sxs-lookup"><span data-stu-id="e5b34-134">Deprecated Quotas</span></span>

<span data-ttu-id="e5b34-135">WinRM 2,0 définit le quota MaxShellRunTime en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e5b34-135">WinRM 2.0 sets the MaxShellRunTime quota to read-only.</span></span> <span data-ttu-id="e5b34-136">La modification de la valeur de ce quota n’aura aucun effet sur les shells distants.</span><span class="sxs-lookup"><span data-stu-id="e5b34-136">Changing the value for this quota will have no effect on the remote shells.</span></span>

## <a name="retrieving-quota-configuration-information"></a><span data-ttu-id="e5b34-137">Récupération des informations de configuration de quota</span><span class="sxs-lookup"><span data-stu-id="e5b34-137">Retrieving Quota Configuration Information</span></span>

<span data-ttu-id="e5b34-138">Pour vérifier les paramètres de configuration de quota, tapez **WinRM-Télécharger winrm/config**.</span><span class="sxs-lookup"><span data-stu-id="e5b34-138">To check the quota configuration settings, type **winrm get winrm/config**.</span></span>

<span data-ttu-id="e5b34-139">L’extrait de code suivant est un exemple basé sur du texte d’une configuration WinRM avec les paramètres de quota par défaut.</span><span class="sxs-lookup"><span data-stu-id="e5b34-139">The following snippet is a text-based example of a WinRM configuration with the default quota settings.</span></span>

``` syntax
Config

          ...         

          Winrs

                   AllowRemoteShellAccess = true

                   IdleTimeout = 7200000

                   MaxConcurrentUsers = 10

                   MaxProcessesPerShell = 25

                   MaxMemoryPerShellMB = 1024

                   MaxShellsPerUser = 30
```

## <a name="configuring-shell-quotas"></a><span data-ttu-id="e5b34-140">Configuration des quotas de l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="e5b34-140">Configuring Shell Quotas</span></span>

<span data-ttu-id="e5b34-141">Les quotas peuvent être définis à l’aide d’un paramètre stratégie de groupe ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="e5b34-141">Quotas can be set through a Group Policy setting or manually.</span></span> <span data-ttu-id="e5b34-142">Pour plus d’informations sur les paramètres de configuration spécifiques, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="e5b34-142">For more information about specific configuration settings, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="e5b34-143">**Pour définir un quota avec stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="e5b34-143">**To set a quota with Group Policy**</span></span>

1.  <span data-ttu-id="e5b34-144">Ouvrez une fenêtre d’invite de commandes en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="e5b34-144">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="e5b34-145">À l’invite de commandes, tapez **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="e5b34-145">At the Command Prompt, type **gpedit.msc**.</span></span> <span data-ttu-id="e5b34-146">La fenêtre de l' **éditeur d’objets stratégie de groupe** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="e5b34-146">The **Group Policy Object Editor** window opens.</span></span>
3.  <span data-ttu-id="e5b34-147">Recherchez les **Windows Remote Management** et **windows Remote Shell** stratégie de groupe objets (GPO) sous **Configuration ordinateur \\ modèles d’administration \\ composants Windows**.</span><span class="sxs-lookup"><span data-stu-id="e5b34-147">Find the **Windows Remote Management** and **Windows Remote Shell** Group Policy Objects (GPO) under **Computer Configuration\\Administrative Templates\\Windows Components**.</span></span>
4.  <span data-ttu-id="e5b34-148">Sous l’onglet **étendue** , sélectionnez un paramètre pour afficher une description.</span><span class="sxs-lookup"><span data-stu-id="e5b34-148">On the **Extended** tab, select a setting to see a description.</span></span> <span data-ttu-id="e5b34-149">Double-cliquez sur un paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="e5b34-149">Double click a setting to edit it.</span></span>

<span data-ttu-id="e5b34-150">**Pour définir un quota manuellement**</span><span class="sxs-lookup"><span data-stu-id="e5b34-150">**To set a quota manually**</span></span>

1.  <span data-ttu-id="e5b34-151">Ouvrez une fenêtre d’invite de commandes en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="e5b34-151">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="e5b34-152">À l’invite de commandes, tapez **winrm set winrm/config/Winrs' @ { ***<Quota>*** = " ***<Value>*** "} '**</span><span class="sxs-lookup"><span data-stu-id="e5b34-152">At the Command Prompt, type **winrm set winrm/config/winrs '@{***<Quota>***="***<Value>***"}'**</span></span>

<span data-ttu-id="e5b34-153">Par exemple, pour augmenter le nombre maximal de shells par utilisateur de 5 à 7, tapez **winrm set winrm/config/Winrs' @ {MaxShellsPerUser = "7"} '**.</span><span class="sxs-lookup"><span data-stu-id="e5b34-153">For example, to increase the maximum number of shells per user from 5 to 7, type **winrm set winrm/config/winrs '@{MaxShellsPerUser="7"}'**.</span></span>

 

 




