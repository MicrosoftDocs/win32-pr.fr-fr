---
description: Lorsque vous effectuez une sauvegarde ou une restauration VSS, l’état du système Windows est défini comme étant une collection de plusieurs éléments clés du système d’exploitation et de leurs fichiers. Ces éléments doivent toujours être traités comme une unité par les opérations de sauvegarde et de restauration.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Sauvegarde et restauration de l’état du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed61c3ccad51ebd8cd632fab292160c795741c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755541"
---
# <a name="backing-up-and-restoring-system-state"></a><span data-ttu-id="9a62f-104">Sauvegarde et restauration de l’état du système</span><span class="sxs-lookup"><span data-stu-id="9a62f-104">Backing Up and Restoring System State</span></span>

> [!Note]  
> <span data-ttu-id="9a62f-105">Cette rubrique s’applique à Windows Vista, Windows Server 2008 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9a62f-105">This topic applies to Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="9a62f-106">Pour plus d’informations sur Windows Server 2003, voir [sauvegarde et restauration de l’état du système dans Windows server 2003 R2 et Windows server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)</span><span class="sxs-lookup"><span data-stu-id="9a62f-106">For information about Windows Server 2003, see [Backing Up and Restoring System State in Windows Server 2003 R2 and Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)</span></span>

 

<span data-ttu-id="9a62f-107">Lorsque vous effectuez une sauvegarde ou une restauration VSS, l’état du système Windows est défini comme étant une collection de plusieurs éléments clés du système d’exploitation et de leurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="9a62f-107">When performing a VSS backup or restore, the Windows system state is defined as being a collection of several key operating system elements and their files.</span></span> <span data-ttu-id="9a62f-108">Ces éléments doivent toujours être traités comme une unité par les opérations de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="9a62f-108">These elements should always be treated as a unit by backup and restore operations.</span></span>

> [!Note]  
> <span data-ttu-id="9a62f-109">Microsoft ne fournit pas de support technique pour les développeurs ou les professionnels de l’informatique pour l’implémentation de restaurations en ligne sur l’état du système sur Windows (toutes les versions).</span><span class="sxs-lookup"><span data-stu-id="9a62f-109">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

 

<span data-ttu-id="9a62f-110">Lors de la sauvegarde et de la récupération de l’état du système, la stratégie recommandée consiste à sauvegarder et à récupérer les volumes système et de démarrage en plus des fichiers énumérés par les Writers d’État du système.</span><span class="sxs-lookup"><span data-stu-id="9a62f-110">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span> <span data-ttu-id="9a62f-111">Les Writers d’État du système sont des enregistreurs dont l’attribut de [**\_ \_ type d’utilisation VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) est défini sur VSS \_ ut \_ BOOTABLESYSTEMSTATE ou VSS \_ ut \_ SYSTEMSERVICE.</span><span class="sxs-lookup"><span data-stu-id="9a62f-111">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a62f-112">Si un enregistreur VSS est identifié par son [**\_ \_ type d’utilisation de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) comme un enregistreur de l’état du système, il doit être inclus dans une sauvegarde de l’état du système, même s’il peut être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="9a62f-112">If a VSS Writer is identified by its [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) as a system state writer it must be included in a system state backup even if it is selectable.</span></span>

 

<span data-ttu-id="9a62f-113">Outre les fichiers binaires du système d’exploitation et du pilote énumérés par les Writers d’État du système, certains autres fichiers doivent être sauvegardés dans le cadre de l’état du système.</span><span class="sxs-lookup"><span data-stu-id="9a62f-113">In addition to the enumerated operating system and driver binary files that are enumerated by the system state writers, there are certain other files that must be backed up as part of system state.</span></span>

<span data-ttu-id="9a62f-114">Tous les composants signalés par un enregistreur VSS du système font partie de l’état du système, à l’exception de ceux pour lesquels l' \_ indicateur VSS CF \_ not \_ System \_ State est défini.</span><span class="sxs-lookup"><span data-stu-id="9a62f-114">All the components reported by a VSS system state writer are part of system state except those for which the VSS\_CF\_NOT\_SYSTEM\_STATE flag is set.</span></span>

<span data-ttu-id="9a62f-115">Les programmes de sauvegarde doivent également définir la clé de Registre **LastRestoreId** .</span><span class="sxs-lookup"><span data-stu-id="9a62f-115">Backup programs should also set the **LastRestoreId** registry key.</span></span> <span data-ttu-id="9a62f-116">Pour plus d’informations, consultez [clés et valeurs de Registre pour la sauvegarde et la restauration](../backup/registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="9a62f-116">For more information, see [Registry Keys and Values for Backup and Restore](../backup/registry-keys-for-backup-and-restore.md).</span></span>

> [!Note]  
> <span data-ttu-id="9a62f-117">Dans Windows Vista, Windows Server 2008 et versions ultérieures, les noms et les emplacements de certains fichiers système ont été modifiés comme suit.</span><span class="sxs-lookup"><span data-stu-id="9a62f-117">In Windows Vista, Windows Server 2008, and later, the names and locations of some system files have been changed as follows.</span></span>

 

## <a name="system-state"></a><span data-ttu-id="9a62f-118">État du système</span><span class="sxs-lookup"><span data-stu-id="9a62f-118">System State</span></span>

<span data-ttu-id="9a62f-119">Pour Windows Server 2012 et versions ultérieures, en plus des fichiers signalés par les différents enregistreurs d’état système VSS, seuls les fichiers de licence suivants doivent être inclus explicitement et les fichiers DRM suivants doivent être exclus explicitement.</span><span class="sxs-lookup"><span data-stu-id="9a62f-119">For Windows Server 2012 and later, in addition to the files reported by the various VSS system-state writers, only the following licensing files need to be included explicitly, and the following DRM files need to be excluded explicitly.</span></span>

## <a name="windows-media-digital-rights-management-files"></a><span data-ttu-id="9a62f-120">Fichiers Rights Management numériques Windows Media</span><span class="sxs-lookup"><span data-stu-id="9a62f-120">Windows Media Digital Rights Management Files</span></span>

<span data-ttu-id="9a62f-121">Dans Windows Server 2008 et versions ultérieures, les fichiers suivants, y compris tous les sous-répertoires sous le chemin d’accès suivant, sont exclus de l’état du système et ne doivent pas être sauvegardés :</span><span class="sxs-lookup"><span data-stu-id="9a62f-121">In Windows Server 2008 and later, the following files, including all subdirectories under the following path, are excluded from system state and must not be backed up:</span></span>

-   <span data-ttu-id="9a62f-122">% ProgramData% \\ Microsoft \\ Windows \\ DRM</span><span class="sxs-lookup"><span data-stu-id="9a62f-122">%ProgramData%\\Microsoft\\Windows\\DRM</span></span>\\

<span data-ttu-id="9a62f-123">Cela remplace les informations de la section Windows Media Digital Rights Management de l' [utilisation des fonctionnalités de sécurité et de système de fichiers](working-with-file-system-and-security-features.md).</span><span class="sxs-lookup"><span data-stu-id="9a62f-123">This supersedes the information in the Windows Media Digital Rights Management section of [Working with File System and Security Features](working-with-file-system-and-security-features.md).</span></span>

## <a name="performance-counter-configuration-files"></a><span data-ttu-id="9a62f-124">Fichiers de configuration du compteur de performances</span><span class="sxs-lookup"><span data-stu-id="9a62f-124">Performance Counter Configuration Files</span></span>

<span data-ttu-id="9a62f-125">Les fichiers de configuration des compteurs de performances se trouvent dans le répertoire% SystemRoot% \\ system32 \\ et portent les noms suivants :</span><span class="sxs-lookup"><span data-stu-id="9a62f-125">The performance counter configuration files are located in the %SystemRoot%\\System32\\ directory and have the following names:</span></span>

<dl> <span data-ttu-id="9a62f-126">Perf ? 00 ?. anciens</span><span class="sxs-lookup"><span data-stu-id="9a62f-126">Perf?00?.dat</span></span>  
<span data-ttu-id="9a62f-127">Perfc0 ??. anciens</span><span class="sxs-lookup"><span data-stu-id="9a62f-127">Perfc0??.dat</span></span>  
<span data-ttu-id="9a62f-128">Perfd0 ??. anciens</span><span class="sxs-lookup"><span data-stu-id="9a62f-128">Perfd0??.dat</span></span>  
<span data-ttu-id="9a62f-129">Perfh0 ??. anciens</span><span class="sxs-lookup"><span data-stu-id="9a62f-129">Perfh0??.dat</span></span>  
<span data-ttu-id="9a62f-130">Perfi0 ??. anciens</span><span class="sxs-lookup"><span data-stu-id="9a62f-130">Perfi0??.dat</span></span>  
<span data-ttu-id="9a62f-131">Prfc0 ???. anciens</span><span class="sxs-lookup"><span data-stu-id="9a62f-131">Prfc0???.dat</span></span>  
<span data-ttu-id="9a62f-132">Prfd0 ???. anciens</span><span class="sxs-lookup"><span data-stu-id="9a62f-132">Prfd0???.dat</span></span>  
<span data-ttu-id="9a62f-133">Prfh0 ???. anciens</span><span class="sxs-lookup"><span data-stu-id="9a62f-133">Prfh0???.dat</span></span>  
<span data-ttu-id="9a62f-134">Prfi0 ???. anciens</span><span class="sxs-lookup"><span data-stu-id="9a62f-134">Prfi0???.dat</span></span>  
</dl>

<span data-ttu-id="9a62f-135">Ces fichiers sont modifiés uniquement lors de l’installation de l’application et doivent être sauvegardés et restaurés au cours des sauvegardes et restaurations de l’état du système.</span><span class="sxs-lookup"><span data-stu-id="9a62f-135">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

## <a name="iis-configuration-files"></a><span data-ttu-id="9a62f-136">Fichiers de configuration IIS</span><span class="sxs-lookup"><span data-stu-id="9a62f-136">IIS Configuration Files</span></span>

> [!Note]  
> <span data-ttu-id="9a62f-137">Dans Windows Vista avec Service Pack 1 (SP1) et versions ultérieures, vous ne devez pas sauvegarder ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="9a62f-137">In Windows Vista with Service Pack 1 (SP1) and later, you should not back up these files.</span></span> <span data-ttu-id="9a62f-138">Au lieu de cela, utilisez l’enregistreur de configuration IIS dans la zone.</span><span class="sxs-lookup"><span data-stu-id="9a62f-138">Instead, use the in-box IIS configuration writer.</span></span> <span data-ttu-id="9a62f-139">Pour plus d’informations sur ce writer, consultez [la page enregistreurs VSS intégrés](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="9a62f-139">For more information about this writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

<span data-ttu-id="9a62f-140">Les fichiers de configuration IIS appropriés et leurs emplacements sont répertoriés ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="9a62f-140">The relevant IIS configuration files and their locations are listed below:</span></span>

-   <span data-ttu-id="9a62f-141">Le fichier de machine.config .NET FX se trouve dans le répertoire de la version du Framework.</span><span class="sxs-lookup"><span data-stu-id="9a62f-141">The .NET FX machine.config file is located in the framework version directory.</span></span>
-   <span data-ttu-id="9a62f-142">Le fichier web.config racine ASP.NET se trouve dans le répertoire de la version du Framework.</span><span class="sxs-lookup"><span data-stu-id="9a62f-142">The ASP.NET root web.config file is located in the framework version directory.</span></span>
    > [!Note]  
    > <span data-ttu-id="9a62f-143">Les fichiers de configuration pour .NET FX et ASP.NET se trouvent dans le répertoire de la version du Framework.</span><span class="sxs-lookup"><span data-stu-id="9a62f-143">The configuration files for both .NET FX and ASP.NET are in the framework version directory.</span></span> <span data-ttu-id="9a62f-144">Si plusieurs versions du Framework sont installées sur l’ordinateur, ce répertoire contiendra un fichier de configuration pour chaque version installée.</span><span class="sxs-lookup"><span data-stu-id="9a62f-144">If multiple versions of the framework are installed on the computer, this directory will contain one configuration file for each installed version.</span></span>

     

-   <span data-ttu-id="9a62f-145">Le fichier de configuration central IIS applicationHost.config se trouve dans le répertoire% windir% \\ system32 \\ inetsrv \\ config.</span><span class="sxs-lookup"><span data-stu-id="9a62f-145">The IIS applicationHost.config central configuration file is located in the %windir%\\system32\\inetsrv\\config directory.</span></span> <span data-ttu-id="9a62f-146">Pour que le serveur comprenne ce fichier de configuration, il existe des fichiers de schéma qui déterminent sa grammaire et sa structure.</span><span class="sxs-lookup"><span data-stu-id="9a62f-146">For the server to understand this configuration file, there are schema files that determine its grammar and structure.</span></span> <span data-ttu-id="9a62f-147">Ces fichiers se trouvent dans le répertoire du schéma de configuration% windir% \\ system32 \\ inetsrv \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="9a62f-147">These files are located in the %windir%\\system32\\inetsrv\\config\\schema directory.</span></span>

<span data-ttu-id="9a62f-148">Le chemin d’accès au répertoire de la version du Framework est stocké dans la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="9a62f-148">The framework version directory path is stored in the following registry key:</span></span>

<span data-ttu-id="9a62f-149">**HKEY \_ logiciel de l' \_ ordinateur local \\ \\ Microsoft \\ . NETFramework \\ InstallRoot**</span><span class="sxs-lookup"><span data-stu-id="9a62f-149">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\.NETFramework\\InstallRoot**</span></span>

<span data-ttu-id="9a62f-150">En outre, les clés de chiffrement suivantes doivent être sauvegardées :</span><span class="sxs-lookup"><span data-stu-id="9a62f-150">In addition, the following cryptography keys must be backed up:</span></span><dl> <span data-ttu-id="9a62f-151">% ProgramData% \\ Microsoft \\ crypto \\ RSA \\ MachineKeys\\\*</span><span class="sxs-lookup"><span data-stu-id="9a62f-151">%ProgramData%\\Microsoft\\Crypto\\RSA\\MachineKeys\\\*</span></span>  
<span data-ttu-id="9a62f-152">% SystemRoot% \\ system32 \\ Microsoft \\ Protect\\\*</span><span class="sxs-lookup"><span data-stu-id="9a62f-152">%SystemRoot%\\System32\\Microsoft\\Protect\\\*</span></span>  
</dl>

## <a name="framework-files"></a><span data-ttu-id="9a62f-153">Fichiers du Framework</span><span class="sxs-lookup"><span data-stu-id="9a62f-153">Framework Files</span></span>

<span data-ttu-id="9a62f-154">Toutes les versions du .NET Framework doivent être sauvegardées.</span><span class="sxs-lookup"><span data-stu-id="9a62f-154">All versions of the .NET framework must be backed up.</span></span> <span data-ttu-id="9a62f-155">Les fichiers se trouvent dans l’un des répertoires suivants (ou les deux) :</span><span class="sxs-lookup"><span data-stu-id="9a62f-155">The files are located in one or both of the following directories:</span></span>

<dl> <span data-ttu-id="9a62f-156">% windir% \\ Microsoft.NET \\ Framework</span><span class="sxs-lookup"><span data-stu-id="9a62f-156">%windir%\\Microsoft.Net\\Framework</span></span>  
<span data-ttu-id="9a62f-157">% windir% \\ Microsoft.NET \\ Framework64</span><span class="sxs-lookup"><span data-stu-id="9a62f-157">%windir%\\Microsoft.Net\\Framework64</span></span>  
</dl>

<span data-ttu-id="9a62f-158">En outre, les fichiers d’assembly doivent être sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="9a62f-158">In addition, the assembly files must be backed up.</span></span> <span data-ttu-id="9a62f-159">Ces fichiers se trouvent dans le répertoire suivant :</span><span class="sxs-lookup"><span data-stu-id="9a62f-159">These files are located in the following directory:</span></span><dl> <span data-ttu-id="9a62f-160">assembly% windir% \\</span><span class="sxs-lookup"><span data-stu-id="9a62f-160">%windir%\\assembly</span></span>  
</dl>

## <a name="task-scheduler-task-files"></a><span data-ttu-id="9a62f-161">Fichiers de tâches Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="9a62f-161">Task Scheduler Task Files</span></span>

<span data-ttu-id="9a62f-162">Les fichiers de tâches du planificateur de tâches doivent être sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="9a62f-162">The task scheduler's task files must be backed up.</span></span> <span data-ttu-id="9a62f-163">Les fichiers se trouvent dans l’un ou l’autre des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="9a62f-163">The files are located in one or both of the following locations:</span></span>

<dl> <span data-ttu-id="9a62f-164">% windir% \\ system32 \\ tâches et tous les sous-répertoires (de manière récursive)</span><span class="sxs-lookup"><span data-stu-id="9a62f-164">%windir%\\system32\\tasks and any subdirectories (recursively)</span></span>  
<span data-ttu-id="9a62f-165">% windir% \\ tâches (aucun sous-répertoire)</span><span class="sxs-lookup"><span data-stu-id="9a62f-165">%windir%\\tasks (no subdirectories)</span></span>  
</dl>

 

 
