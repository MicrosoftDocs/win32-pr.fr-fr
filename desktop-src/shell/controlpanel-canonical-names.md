---
description: À compter de Windows Vista, les éléments du panneau de configuration inclus avec Windows reçoivent un nom canonique qui peut être utilisé dans un appel d’API ou une instruction de ligne de commande pour lancer par programmation cet élément.
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: Noms canoniques des éléments du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55fc360b0d3db0f85a057977d1898c59d09d5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951021"
---
# <a name="canonical-names-of-control-panel-items"></a><span data-ttu-id="02246-103">Noms canoniques des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="02246-103">Canonical Names of Control Panel Items</span></span>

<span data-ttu-id="02246-104">À compter de Windows Vista, les éléments du panneau de configuration inclus avec Windows reçoivent un nom canonique qui peut être utilisé dans un [appel d’API ou une instruction de ligne de commande](executing-control-panel-items.md) pour lancer par programmation cet élément.</span><span class="sxs-lookup"><span data-stu-id="02246-104">As of Windows Vista, Control Panel items included with Windows are given a canonical name that can be used in an [API call or a command-line instruction](executing-control-panel-items.md) to programmatically launch that item.</span></span> <span data-ttu-id="02246-105">À compter de Windows 7 et de Windows Server 2008 R2, les noms canoniques peuvent être utilisés dans une stratégie de groupe pour masquer des éléments spécifiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="02246-105">As of Windows 7 and Windows Server 2008 R2, canonical names can be used in a group policy to hide specific Control Panel items.</span></span> <span data-ttu-id="02246-106">Cette rubrique fournit des détails sur chaque élément du panneau de configuration : le nom canonique, le GUID, le nom du module et les versions de système d’exploitation qui reconnaissent le nom canonique.</span><span class="sxs-lookup"><span data-stu-id="02246-106">This topic provides details for each Control Panel item: canonical name, GUID, module name, and the operating system versions that recognize the canonical name.</span></span>

> [!Note]  
> <span data-ttu-id="02246-107">Les noms canoniques des éléments du panneau de configuration ne sont pas pris en charge avant Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="02246-107">Canonical names for Control Panel items are not supported prior to Windows Vista.</span></span>

 

-   [<span data-ttu-id="02246-108">Noms canoniques du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="02246-108">Control Panel Canonical Names</span></span>](#control-panel-canonical-names)
-   [<span data-ttu-id="02246-109">Noms canoniques du panneau de configuration déconseillés</span><span class="sxs-lookup"><span data-stu-id="02246-109">Deprecated Control Panel Canonical Names</span></span>](#deprecated-control-panel-canonical-names)
-   [<span data-ttu-id="02246-110">Utilisation de noms canoniques dans les stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="02246-110">Using Canonical Names in Group Policy</span></span>](#using-canonical-names-in-local-group-policy)
-   [<span data-ttu-id="02246-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="02246-111">Remarks</span></span>](#remarks)

## <a name="control-panel-canonical-names"></a><span data-ttu-id="02246-112">Noms canoniques du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="02246-112">Control Panel Canonical Names</span></span>

<span data-ttu-id="02246-113">Points à retenir lors de l’utilisation de ces valeurs :</span><span class="sxs-lookup"><span data-stu-id="02246-113">Points to remember when working with these values:</span></span>

-   <span data-ttu-id="02246-114">Par définition, les noms canoniques ne changent pas en fonction de la langue du système. ils sont toujours en anglais, même si la langue du système ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="02246-114">By definition, canonical names do not change based on the system language; they're always in English, even if the system's language is not.</span></span>
-   <span data-ttu-id="02246-115">Tous les éléments du panneau de configuration ne sont pas présents dans toutes les variétés de Windows.</span><span class="sxs-lookup"><span data-stu-id="02246-115">Not all Control Panel items are present in all varieties of Windows.</span></span>
-   <span data-ttu-id="02246-116">Certains éléments du panneau de configuration ne s’affichent que si le matériel approprié est détecté sur le système.</span><span class="sxs-lookup"><span data-stu-id="02246-116">Some Control Panel items only appear if the right hardware is detected on the system.</span></span>
-   <span data-ttu-id="02246-117">Les tiers peuvent également ajouter des éléments du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="02246-117">Third parties can also add Control Panel items.</span></span> <span data-ttu-id="02246-118">Les noms canoniques répertoriés ici ne concernent que les éléments du panneau de configuration qui sont inclus avec Windows.</span><span class="sxs-lookup"><span data-stu-id="02246-118">The canonical names listed here are only for Control Panel items that are included with Windows.</span></span>

<span data-ttu-id="02246-119">Voici les éléments du panneau de configuration disponibles dans Windows 8.1 :</span><span class="sxs-lookup"><span data-stu-id="02246-119">The following are the Control Panel items available in Windows 8.1:</span></span>

-   [<span data-ttu-id="02246-120">Centre de maintenance</span><span class="sxs-lookup"><span data-stu-id="02246-120">Action Center</span></span>](#action-center)
-   [<span data-ttu-id="02246-121">Outils d’administration</span><span class="sxs-lookup"><span data-stu-id="02246-121">Administrative Tools</span></span>](#administrative-tools)
-   [<span data-ttu-id="02246-122">Exécution automatique</span><span class="sxs-lookup"><span data-stu-id="02246-122">AutoPlay</span></span>](#autoplay)
-   [<span data-ttu-id="02246-123">Périphériques biométriques</span><span class="sxs-lookup"><span data-stu-id="02246-123">Biometric Devices</span></span>](#biometric-devices)
-   [<span data-ttu-id="02246-124">Chiffrement de lecteur BitLocker</span><span class="sxs-lookup"><span data-stu-id="02246-124">BitLocker Drive Encryption</span></span>](#bitlocker-drive-encryption)
-   [<span data-ttu-id="02246-125">Gestion des couleurs</span><span class="sxs-lookup"><span data-stu-id="02246-125">Color Management</span></span>](#color-management)
-   [<span data-ttu-id="02246-126">Gestionnaire d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="02246-126">Credential Manager</span></span>](#credential-manager)
-   [<span data-ttu-id="02246-127">Date et heure</span><span class="sxs-lookup"><span data-stu-id="02246-127">Date and Time</span></span>](#date-and-time)
-   [<span data-ttu-id="02246-128">Programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="02246-128">Default Programs</span></span>](#default-programs)
-   [<span data-ttu-id="02246-129">Gestionnaire de périphériques</span><span class="sxs-lookup"><span data-stu-id="02246-129">Device Manager</span></span>](#device-manager)
-   [<span data-ttu-id="02246-130">Périphériques et imprimantes</span><span class="sxs-lookup"><span data-stu-id="02246-130">Devices and Printers</span></span>](#devices-and-printers)
-   [<span data-ttu-id="02246-131">Affichage</span><span class="sxs-lookup"><span data-stu-id="02246-131">Display</span></span>](#display)
-   [<span data-ttu-id="02246-132">Options d’ergonomie</span><span class="sxs-lookup"><span data-stu-id="02246-132">Ease of Access Center</span></span>](#ease-of-access-center)
-   [<span data-ttu-id="02246-133">Contrôle parental</span><span class="sxs-lookup"><span data-stu-id="02246-133">Family Safety</span></span>](#family-safety)
-   [<span data-ttu-id="02246-134">Historique des fichiers</span><span class="sxs-lookup"><span data-stu-id="02246-134">File History</span></span>](#file-history)
-   [<span data-ttu-id="02246-135">Options des dossiers</span><span class="sxs-lookup"><span data-stu-id="02246-135">Folder Options</span></span>](#folder-options)
-   [<span data-ttu-id="02246-136">Polices</span><span class="sxs-lookup"><span data-stu-id="02246-136">Fonts</span></span>](#fonts)
-   [<span data-ttu-id="02246-137">HomeGroup</span><span class="sxs-lookup"><span data-stu-id="02246-137">HomeGroup</span></span>](#homegroup)
-   [<span data-ttu-id="02246-138">Options d’indexation</span><span class="sxs-lookup"><span data-stu-id="02246-138">Indexing Options</span></span>](#indexing-options)
-   [<span data-ttu-id="02246-139">Infrarouge</span><span class="sxs-lookup"><span data-stu-id="02246-139">Infrared</span></span>](#infrared)
-   [<span data-ttu-id="02246-140">Options Internet</span><span class="sxs-lookup"><span data-stu-id="02246-140">Internet Options</span></span>](#internet-options)
-   [<span data-ttu-id="02246-141">Initiateur iSCSI</span><span class="sxs-lookup"><span data-stu-id="02246-141">iSCSI Initiator</span></span>](#iscsi-initiator)
-   [<span data-ttu-id="02246-142">Serveur iSNS</span><span class="sxs-lookup"><span data-stu-id="02246-142">iSNS Server</span></span>](#isns-server)
-   [<span data-ttu-id="02246-143">Clavier</span><span class="sxs-lookup"><span data-stu-id="02246-143">Keyboard</span></span>](#keyboard)
-   [<span data-ttu-id="02246-144">Paramètres d’emplacement</span><span class="sxs-lookup"><span data-stu-id="02246-144">Location Settings</span></span>](#location-settings)
-   [<span data-ttu-id="02246-145">Souris</span><span class="sxs-lookup"><span data-stu-id="02246-145">Mouse</span></span>](#mouse)
-   [<span data-ttu-id="02246-146">MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="02246-146">MPIOConfiguration</span></span>](#mpioconfiguration)
-   [<span data-ttu-id="02246-147">Centre Réseau et partage</span><span class="sxs-lookup"><span data-stu-id="02246-147">Network and Sharing Center</span></span>](#network-and-sharing-center)
-   [<span data-ttu-id="02246-148">Icônes de la zone de notification</span><span class="sxs-lookup"><span data-stu-id="02246-148">Notification Area Icons</span></span>](#notification-area-icons)
-   [<span data-ttu-id="02246-149">Pen et Touch</span><span class="sxs-lookup"><span data-stu-id="02246-149">Pen and Touch</span></span>](#pen-and-touch)
-   [<span data-ttu-id="02246-150">Personnalisation</span><span class="sxs-lookup"><span data-stu-id="02246-150">Personalization</span></span>](#personalization)
-   [<span data-ttu-id="02246-151">Téléphone et modem</span><span class="sxs-lookup"><span data-stu-id="02246-151">Phone and Modem</span></span>](#phone-and-modem)
-   [<span data-ttu-id="02246-152">Options d’alimentation</span><span class="sxs-lookup"><span data-stu-id="02246-152">Power Options</span></span>](#power-options)
-   [<span data-ttu-id="02246-153">Programmes et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="02246-153">Programs and Features</span></span>](#programs-and-features)
-   [<span data-ttu-id="02246-154">Récupération</span><span class="sxs-lookup"><span data-stu-id="02246-154">Recovery</span></span>](#recovery)
-   [<span data-ttu-id="02246-155">Région</span><span class="sxs-lookup"><span data-stu-id="02246-155">Region</span></span>](#region)
-   [<span data-ttu-id="02246-156">Connexions aux programmes RemoteApp et aux services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="02246-156">RemoteApp and Desktop Connections</span></span>](#remoteapp-and-desktop-connections)
-   [<span data-ttu-id="02246-157">Son</span><span class="sxs-lookup"><span data-stu-id="02246-157">Sound</span></span>](#sound)
-   [<span data-ttu-id="02246-158">Reconnaissance vocale</span><span class="sxs-lookup"><span data-stu-id="02246-158">Speech Recognition</span></span>](#speech-recognition)
-   [<span data-ttu-id="02246-159">Espaces de stockage</span><span class="sxs-lookup"><span data-stu-id="02246-159">Storage Spaces</span></span>](#storage-spaces)
-   [<span data-ttu-id="02246-160">Centre de synchronisation</span><span class="sxs-lookup"><span data-stu-id="02246-160">Sync Center</span></span>](#sync-center)
-   [<span data-ttu-id="02246-161">Système</span><span class="sxs-lookup"><span data-stu-id="02246-161">System</span></span>](#system)
-   [<span data-ttu-id="02246-162">Paramètres du Tablet PC</span><span class="sxs-lookup"><span data-stu-id="02246-162">Tablet PC Settings</span></span>](#tablet-pc-settings)
-   [<span data-ttu-id="02246-163">Barre des tâches et navigation</span><span class="sxs-lookup"><span data-stu-id="02246-163">Taskbar and Navigation</span></span>](#taskbar-and-navigation)
-   [<span data-ttu-id="02246-164">Dépannage</span><span class="sxs-lookup"><span data-stu-id="02246-164">Troubleshooting</span></span>](#troubleshooting)
-   [<span data-ttu-id="02246-165">TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="02246-165">TSAppInstall</span></span>](#tsappinstall)
-   [<span data-ttu-id="02246-166">Comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="02246-166">User Accounts</span></span>](#user-accounts)
-   [<span data-ttu-id="02246-167">Mise à niveau express</span><span class="sxs-lookup"><span data-stu-id="02246-167">Windows Anytime Upgrade</span></span>](#windows-anytime-upgrade)
-   [<span data-ttu-id="02246-168">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="02246-168">Windows Defender</span></span>](#windows-defender)
-   [<span data-ttu-id="02246-169">Pare-feu Windows</span><span class="sxs-lookup"><span data-stu-id="02246-169">Windows Firewall</span></span>](#windows-firewall)
-   [<span data-ttu-id="02246-170">Centre de mobilité Windows</span><span class="sxs-lookup"><span data-stu-id="02246-170">Windows Mobility Center</span></span>](#windows-mobility-center)
-   [<span data-ttu-id="02246-171">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="02246-171">Windows To Go</span></span>](#windows-to-go)
-   [<span data-ttu-id="02246-172">Windows Update</span><span class="sxs-lookup"><span data-stu-id="02246-172">Windows Update</span></span>](#windows-update)
-   [<span data-ttu-id="02246-173">Dossiers de travail</span><span class="sxs-lookup"><span data-stu-id="02246-173">Work Folders</span></span>](#work-folders)

### <a name="action-center"></a><span data-ttu-id="02246-174">Centre de maintenance</span><span class="sxs-lookup"><span data-stu-id="02246-174">Action Center</span></span>

-   <span data-ttu-id="02246-175">**Nom canonique**: Microsoft. ActionCenter</span><span class="sxs-lookup"><span data-stu-id="02246-175">**Canonical name**: Microsoft.ActionCenter</span></span>
-   <span data-ttu-id="02246-176">**GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span><span class="sxs-lookup"><span data-stu-id="02246-176">**GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span></span>
-   <span data-ttu-id="02246-177">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-177">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-178">**Nom du module**: @% systemroot% \\ system32 \\ActionCenterCPL.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-178">**Module name**: @%SystemRoot%\\System32\\ActionCenterCPL.dll,-1</span></span>
-   <span data-ttu-id="02246-179">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-179">**Pages**</span></span>

    | <span data-ttu-id="02246-180">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-180">Page Name</span></span>           | <span data-ttu-id="02246-181">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-181">Opens</span></span>                      |
    |---------------------|----------------------------|
    | <span data-ttu-id="02246-182">MaintenanceSettings</span><span class="sxs-lookup"><span data-stu-id="02246-182">MaintenanceSettings</span></span> | <span data-ttu-id="02246-183">Maintenance automatique</span><span class="sxs-lookup"><span data-stu-id="02246-183">Automatic Maintenance</span></span>      |
    | <span data-ttu-id="02246-184">pageProblems</span><span class="sxs-lookup"><span data-stu-id="02246-184">pageProblems</span></span>        | <span data-ttu-id="02246-185">Rapports de problèmes</span><span class="sxs-lookup"><span data-stu-id="02246-185">Problem Reports</span></span>            |
    | <span data-ttu-id="02246-186">pageReliabilityView</span><span class="sxs-lookup"><span data-stu-id="02246-186">pageReliabilityView</span></span> | <span data-ttu-id="02246-187">Moniteur de fiabilité</span><span class="sxs-lookup"><span data-stu-id="02246-187">Reliability Monitor</span></span>        |
    | <span data-ttu-id="02246-188">pageResponseArchive</span><span class="sxs-lookup"><span data-stu-id="02246-188">pageResponseArchive</span></span> | <span data-ttu-id="02246-189">Messages archivés</span><span class="sxs-lookup"><span data-stu-id="02246-189">Archived Messages</span></span>          |
    | <span data-ttu-id="02246-190">pageSettings</span><span class="sxs-lookup"><span data-stu-id="02246-190">pageSettings</span></span>        | <span data-ttu-id="02246-191">Paramètres de signalement de problèmes</span><span class="sxs-lookup"><span data-stu-id="02246-191">Problem Reporting Settings</span></span> |

    

     

### <a name="administrative-tools"></a><span data-ttu-id="02246-192">Outils d'administration</span><span class="sxs-lookup"><span data-stu-id="02246-192">Administrative Tools</span></span>

-   <span data-ttu-id="02246-193">**Nom canonique**: Microsoft. AdministrativeTools</span><span class="sxs-lookup"><span data-stu-id="02246-193">**Canonical name**: Microsoft.AdministrativeTools</span></span>
-   <span data-ttu-id="02246-194">**GUID**: {D20EA4E1-3957-11D2-A40B-0C5020524153}</span><span class="sxs-lookup"><span data-stu-id="02246-194">**GUID**: {D20EA4E1-3957-11d2-A40B-0C5020524153}</span></span>
-   <span data-ttu-id="02246-195">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-195">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-196">**Nom du module**: @% systemroot% \\ system32 \\shell32.dll,-22982</span><span class="sxs-lookup"><span data-stu-id="02246-196">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22982</span></span>

### <a name="autoplay"></a><span data-ttu-id="02246-197">Lecture automatique</span><span class="sxs-lookup"><span data-stu-id="02246-197">AutoPlay</span></span>

-   <span data-ttu-id="02246-198">**Nom canonique**: Microsoft. AutoPlay</span><span class="sxs-lookup"><span data-stu-id="02246-198">**Canonical name**: Microsoft.AutoPlay</span></span>
-   <span data-ttu-id="02246-199">**GUID**: {9C60DE1E-E5FC-40F4-A487-460851A8D915}</span><span class="sxs-lookup"><span data-stu-id="02246-199">**GUID**: {9C60DE1E-E5FC-40f4-A487-460851A8D915}</span></span>
-   <span data-ttu-id="02246-200">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-200">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-201">**Nom du module**: @% systemroot% \\ system32 \\autoplay.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-201">**Module name**: @%SystemRoot%\\System32\\autoplay.dll,-1</span></span>

### <a name="biometric-devices"></a><span data-ttu-id="02246-202">Périphériques biométriques</span><span class="sxs-lookup"><span data-stu-id="02246-202">Biometric Devices</span></span>

-   <span data-ttu-id="02246-203">**Nom canonique**: Microsoft. BiometricDevices</span><span class="sxs-lookup"><span data-stu-id="02246-203">**Canonical name**: Microsoft.BiometricDevices</span></span>
-   <span data-ttu-id="02246-204">**GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span><span class="sxs-lookup"><span data-stu-id="02246-204">**GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span></span>
-   <span data-ttu-id="02246-205">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-205">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-206">**Nom du module**: @% systemroot% \\ system32 \\biocpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-206">**Module name**: @%SystemRoot%\\System32\\biocpl.dll,-1</span></span>

### <a name="bitlocker-drive-encryption"></a><span data-ttu-id="02246-207">Chiffrement de lecteur BitLocker</span><span class="sxs-lookup"><span data-stu-id="02246-207">BitLocker Drive Encryption</span></span>

-   <span data-ttu-id="02246-208">**Nom canonique**: Microsoft. BitLockerDriveEncryption</span><span class="sxs-lookup"><span data-stu-id="02246-208">**Canonical name**: Microsoft.BitLockerDriveEncryption</span></span>
-   <span data-ttu-id="02246-209">**GUID**: {D9EF8727-CaC2-4e60-809e-86F80A666C91}</span><span class="sxs-lookup"><span data-stu-id="02246-209">**GUID**: {D9EF8727-CAC2-4e60-809E-86F80A666C91}</span></span>
-   <span data-ttu-id="02246-210">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-210">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-211">**Nom du module**: @% systemroot% \\ system32 \\fvecpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-211">**Module name**: @%SystemRoot%\\System32\\fvecpl.dll,-1</span></span>

### <a name="color-management"></a><span data-ttu-id="02246-212">Gestion des couleurs</span><span class="sxs-lookup"><span data-stu-id="02246-212">Color Management</span></span>

-   <span data-ttu-id="02246-213">**Nom canonique**: Microsoft. colormanagement</span><span class="sxs-lookup"><span data-stu-id="02246-213">**Canonical name**: Microsoft.ColorManagement</span></span>
-   <span data-ttu-id="02246-214">**GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}</span><span class="sxs-lookup"><span data-stu-id="02246-214">**GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}</span></span>
-   <span data-ttu-id="02246-215">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-215">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-216">**Nom du module**: @% systemroot% \\ system32 \\colorcpl.exe,-6</span><span class="sxs-lookup"><span data-stu-id="02246-216">**Module name**: @%systemroot%\\system32\\colorcpl.exe,-6</span></span>

### <a name="credential-manager"></a><span data-ttu-id="02246-217">Gestionnaire d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="02246-217">Credential Manager</span></span>

-   <span data-ttu-id="02246-218">**Nom canonique**: Microsoft. CredentialManager</span><span class="sxs-lookup"><span data-stu-id="02246-218">**Canonical name**: Microsoft.CredentialManager</span></span>
-   <span data-ttu-id="02246-219">**GUID**: {1206F5F1-0569-412c-8FEC-3204630DFB70}</span><span class="sxs-lookup"><span data-stu-id="02246-219">**GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}</span></span>
-   <span data-ttu-id="02246-220">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-220">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-221">**Nom du module**: @% systemroot% \\ system32 \\Vault.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-221">**Module name**: @%SystemRoot%\\system32\\Vault.dll,-1</span></span>
-   <span data-ttu-id="02246-222">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-222">**Pages**</span></span>

    | <span data-ttu-id="02246-223">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-223">Page Name</span></span>                   | <span data-ttu-id="02246-224">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-224">Opens</span></span>               |
    |-----------------------------|---------------------|
    | <span data-ttu-id="02246-225">? SelectedVault = CredmanVault</span><span class="sxs-lookup"><span data-stu-id="02246-225">?SelectedVault=CredmanVault</span></span> | <span data-ttu-id="02246-226">Informations d’identification Windows</span><span class="sxs-lookup"><span data-stu-id="02246-226">Windows Credentials</span></span> |

    

     

### <a name="date-and-time"></a><span data-ttu-id="02246-227">Date et heure</span><span class="sxs-lookup"><span data-stu-id="02246-227">Date and Time</span></span>

-   <span data-ttu-id="02246-228">**Nom canonique**: Microsoft. DateAndTime</span><span class="sxs-lookup"><span data-stu-id="02246-228">**Canonical name**: Microsoft.DateAndTime</span></span>
-   <span data-ttu-id="02246-229">**GUID**: {E2E7934B-DCE5-43c4-9576-7FE4F75E7480}</span><span class="sxs-lookup"><span data-stu-id="02246-229">**GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}</span></span>
-   <span data-ttu-id="02246-230">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-230">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-231">**Nom du module**: @% systemroot% \\ system32 \\timedate.cpl,-51</span><span class="sxs-lookup"><span data-stu-id="02246-231">**Module name**: @%SystemRoot%\\System32\\timedate.cpl,-51</span></span>
-   <span data-ttu-id="02246-232">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-232">**Pages**</span></span>

    | <span data-ttu-id="02246-233">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-233">Page Name</span></span> | <span data-ttu-id="02246-234">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-234">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="02246-235">1</span><span class="sxs-lookup"><span data-stu-id="02246-235">1</span></span>         | <span data-ttu-id="02246-236">Horloges supplémentaires</span><span class="sxs-lookup"><span data-stu-id="02246-236">Additional Clocks</span></span> |

    

     

### <a name="default-programs"></a><span data-ttu-id="02246-237">Programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="02246-237">Default Programs</span></span>

-   <span data-ttu-id="02246-238">**Nom canonique**: Microsoft. DefaultPrograms</span><span class="sxs-lookup"><span data-stu-id="02246-238">**Canonical name**: Microsoft.DefaultPrograms</span></span>
-   <span data-ttu-id="02246-239">**GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}</span><span class="sxs-lookup"><span data-stu-id="02246-239">**GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}</span></span>
-   <span data-ttu-id="02246-240">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-240">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-241">**Nom du module**: @% systemroot% \\ system32 \\sud.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-241">**Module name**: @%SystemRoot%\\System32\\sud.dll,-1</span></span>
-   <span data-ttu-id="02246-242">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-242">**Pages**</span></span>

    | <span data-ttu-id="02246-243">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-243">Page Name</span></span>          | <span data-ttu-id="02246-244">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-244">Opens</span></span>                |
    |--------------------|----------------------|
    | <span data-ttu-id="02246-245">pageDefaultProgram</span><span class="sxs-lookup"><span data-stu-id="02246-245">pageDefaultProgram</span></span> | <span data-ttu-id="02246-246">Définir les programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="02246-246">Set Default Programs</span></span> |
    | <span data-ttu-id="02246-247">pageFileAssoc</span><span class="sxs-lookup"><span data-stu-id="02246-247">pageFileAssoc</span></span>      | <span data-ttu-id="02246-248">Définir des associations</span><span class="sxs-lookup"><span data-stu-id="02246-248">Set Associations</span></span>     |

    

     

### <a name="device-manager"></a><span data-ttu-id="02246-249">Gestionnaire de périphériques</span><span class="sxs-lookup"><span data-stu-id="02246-249">Device Manager</span></span>

-   <span data-ttu-id="02246-250">**Nom canonique**: Microsoft. DeviceManager</span><span class="sxs-lookup"><span data-stu-id="02246-250">**Canonical name**: Microsoft.DeviceManager</span></span>
-   <span data-ttu-id="02246-251">**GUID**: {74246bfc-4C96-11D0-ABEF-0020af6b0b7a}</span><span class="sxs-lookup"><span data-stu-id="02246-251">**GUID**: {74246bfc-4c96-11d0-abef-0020af6b0b7a}</span></span>
-   <span data-ttu-id="02246-252">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-252">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-253">**Nom du module**: @% systemroot% \\ system32 \\devmgr.dll,-4</span><span class="sxs-lookup"><span data-stu-id="02246-253">**Module name**: @%SystemRoot%\\System32\\devmgr.dll,-4</span></span>

### <a name="devices-and-printers"></a><span data-ttu-id="02246-254">Périphériques et imprimantes</span><span class="sxs-lookup"><span data-stu-id="02246-254">Devices and Printers</span></span>

-   <span data-ttu-id="02246-255">**Nom canonique**: Microsoft. DevicesAndPrinters</span><span class="sxs-lookup"><span data-stu-id="02246-255">**Canonical name**: Microsoft.DevicesAndPrinters</span></span>
-   <span data-ttu-id="02246-256">**GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span><span class="sxs-lookup"><span data-stu-id="02246-256">**GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span></span>
-   <span data-ttu-id="02246-257">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-257">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-258">**Nom du module**: @% systemroot% \\ system32 \\DeviceCenter.dll,-1000</span><span class="sxs-lookup"><span data-stu-id="02246-258">**Module name**: @%systemroot%\\system32\\DeviceCenter.dll,-1000</span></span>

### <a name="display"></a><span data-ttu-id="02246-259">Afficher</span><span class="sxs-lookup"><span data-stu-id="02246-259">Display</span></span>

-   <span data-ttu-id="02246-260">**Nom canonique**: Microsoft. Display</span><span class="sxs-lookup"><span data-stu-id="02246-260">**Canonical name**: Microsoft.Display</span></span>
-   <span data-ttu-id="02246-261">**GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span><span class="sxs-lookup"><span data-stu-id="02246-261">**GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span></span>
-   <span data-ttu-id="02246-262">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-262">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-263">**Nom du module**: @% systemroot% \\ system32 \\Display.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-263">**Module name**: @%SystemRoot%\\System32\\Display.dll,-1</span></span>
-   <span data-ttu-id="02246-264">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-264">**Pages**</span></span>

    | <span data-ttu-id="02246-265">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-265">Page Name</span></span> | <span data-ttu-id="02246-266">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-266">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="02246-267">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02246-267">Settings</span></span>  | <span data-ttu-id="02246-268">Résolution d’écran</span><span class="sxs-lookup"><span data-stu-id="02246-268">Screen Resolution</span></span> |

    

     

### <a name="ease-of-access-center"></a><span data-ttu-id="02246-269">Options d’ergonomie</span><span class="sxs-lookup"><span data-stu-id="02246-269">Ease of Access Center</span></span>

-   <span data-ttu-id="02246-270">**Nom canonique**: Microsoft. EaseOfAccessCenter</span><span class="sxs-lookup"><span data-stu-id="02246-270">**Canonical name**: Microsoft.EaseOfAccessCenter</span></span>
-   <span data-ttu-id="02246-271">**GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span><span class="sxs-lookup"><span data-stu-id="02246-271">**GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span></span>
-   <span data-ttu-id="02246-272">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-272">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-273">**Nom du module**: @% systemroot% \\ system32 \\accessibilitycpl.dll,-10</span><span class="sxs-lookup"><span data-stu-id="02246-273">**Module name**: @%SystemRoot%\\System32\\accessibilitycpl.dll,-10</span></span>
-   <span data-ttu-id="02246-274">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-274">**Pages**</span></span>

    | <span data-ttu-id="02246-275">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-275">Page Name</span></span>               | <span data-ttu-id="02246-276">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-276">Opens</span></span>                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | <span data-ttu-id="02246-277">pageEasierToClick</span><span class="sxs-lookup"><span data-stu-id="02246-277">pageEasierToClick</span></span>       | <span data-ttu-id="02246-278">Faciliter l’utilisation de la souris</span><span class="sxs-lookup"><span data-stu-id="02246-278">Make the mouse easier to use</span></span>                                        |
    | <span data-ttu-id="02246-279">pageEasierToSee</span><span class="sxs-lookup"><span data-stu-id="02246-279">pageEasierToSee</span></span>         | <span data-ttu-id="02246-280">Rendre l’ordinateur plus facile à voir</span><span class="sxs-lookup"><span data-stu-id="02246-280">Make the computer easier to see</span></span>                                     |
    | <span data-ttu-id="02246-281">pageEasierWithSounds</span><span class="sxs-lookup"><span data-stu-id="02246-281">pageEasierWithSounds</span></span>    | <span data-ttu-id="02246-282">Utiliser du texte ou des alternatives visuelles pour les sons</span><span class="sxs-lookup"><span data-stu-id="02246-282">Use text or visual alternatives for sounds</span></span>                          |
    | <span data-ttu-id="02246-283">pageFilterKeysSettings</span><span class="sxs-lookup"><span data-stu-id="02246-283">pageFilterKeysSettings</span></span>  | <span data-ttu-id="02246-284">Configurer des clés de filtre</span><span class="sxs-lookup"><span data-stu-id="02246-284">Set up Filter Keys</span></span>                                                  |
    | <span data-ttu-id="02246-285">pageKeyboardEasierToUse</span><span class="sxs-lookup"><span data-stu-id="02246-285">pageKeyboardEasierToUse</span></span> | <span data-ttu-id="02246-286">Faciliter l’utilisation du clavier</span><span class="sxs-lookup"><span data-stu-id="02246-286">Make the keyboard easier to use</span></span>                                     |
    | <span data-ttu-id="02246-287">pageNoMouseOrKeyboard</span><span class="sxs-lookup"><span data-stu-id="02246-287">pageNoMouseOrKeyboard</span></span>   | <span data-ttu-id="02246-288">Utiliser l’ordinateur sans clavier ni souris</span><span class="sxs-lookup"><span data-stu-id="02246-288">Use the computer without a mouse or keyboard</span></span>                        |
    | <span data-ttu-id="02246-289">pageNoVisual</span><span class="sxs-lookup"><span data-stu-id="02246-289">pageNoVisual</span></span>            | <span data-ttu-id="02246-290">Utiliser l’ordinateur sans affichage</span><span class="sxs-lookup"><span data-stu-id="02246-290">Use the computer without a display</span></span>                                  |
    | <span data-ttu-id="02246-291">pageQuestionsCognitive</span><span class="sxs-lookup"><span data-stu-id="02246-291">pageQuestionsCognitive</span></span>  | <span data-ttu-id="02246-292">Recevez des recommandations pour faciliter l’utilisation de votre ordinateur (cognitive)</span><span class="sxs-lookup"><span data-stu-id="02246-292">Get recommendations to make your computer easier to use (cognitive)</span></span> |
    | <span data-ttu-id="02246-293">pageQuestionsEyesight</span><span class="sxs-lookup"><span data-stu-id="02246-293">pageQuestionsEyesight</span></span>   | <span data-ttu-id="02246-294">Recevoir des recommandations pour faciliter l’utilisation de votre ordinateur (vue)</span><span class="sxs-lookup"><span data-stu-id="02246-294">Get recommendations to make your computer easier to use (eyesight)</span></span>  |

    

     

### <a name="family-safety"></a><span data-ttu-id="02246-295">Contrôle parental</span><span class="sxs-lookup"><span data-stu-id="02246-295">Family Safety</span></span>

-   <span data-ttu-id="02246-296">**Nom canonique**: Microsoft. parentalcontrols</span><span class="sxs-lookup"><span data-stu-id="02246-296">**Canonical name**: Microsoft.ParentalControls</span></span>
-   <span data-ttu-id="02246-297">**GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}</span><span class="sxs-lookup"><span data-stu-id="02246-297">**GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}</span></span>
-   <span data-ttu-id="02246-298">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-298">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-299">**Nom du module**: @% systemroot% \\ system32 \\wpccpl.dll,-100</span><span class="sxs-lookup"><span data-stu-id="02246-299">**Module name**: @%SystemRoot%\\System32\\wpccpl.dll,-100</span></span>
-   <span data-ttu-id="02246-300">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-300">**Pages**</span></span>

    | <span data-ttu-id="02246-301">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-301">Page Name</span></span>   | <span data-ttu-id="02246-302">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-302">Opens</span></span>                                  |
    |-------------|----------------------------------------|
    | <span data-ttu-id="02246-303">pageUserHub</span><span class="sxs-lookup"><span data-stu-id="02246-303">pageUserHub</span></span> | <span data-ttu-id="02246-304">Choisir un utilisateur et configurer la sécurité de la famille</span><span class="sxs-lookup"><span data-stu-id="02246-304">Choose a user and set up Family Safety</span></span> |

    

     

### <a name="file-history"></a><span data-ttu-id="02246-305">Historique des fichiers</span><span class="sxs-lookup"><span data-stu-id="02246-305">File History</span></span>

-   <span data-ttu-id="02246-306">**Nom canonique**: Microsoft. FileHistory</span><span class="sxs-lookup"><span data-stu-id="02246-306">**Canonical name**: Microsoft.FileHistory</span></span>
-   <span data-ttu-id="02246-307">**GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span><span class="sxs-lookup"><span data-stu-id="02246-307">**GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span></span>
-   <span data-ttu-id="02246-308">**Système d’exploitation pris en charge**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-308">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-309">**Nom du module**: @% systemroot% \\ system32 \\fhcpl.dll,-52</span><span class="sxs-lookup"><span data-stu-id="02246-309">**Module name**: @%SystemRoot%\\System32\\fhcpl.dll,-52</span></span>
-   <span data-ttu-id="02246-310">L’historique des fichiers comprend une version plus récente de l’élément de sauvegarde et de restauration, mais ce nom canonique de l’ancien élément n’est pas remappé à l’historique des fichiers.</span><span class="sxs-lookup"><span data-stu-id="02246-310">File History includes a newer version of the Backup and Restore item, but that older item's canonical name does not remap to File History.</span></span>

### <a name="folder-options"></a><span data-ttu-id="02246-311">Options des dossiers</span><span class="sxs-lookup"><span data-stu-id="02246-311">Folder Options</span></span>

-   <span data-ttu-id="02246-312">**Nom canonique**: Microsoft. FolderOptions</span><span class="sxs-lookup"><span data-stu-id="02246-312">**Canonical name**: Microsoft.FolderOptions</span></span>
-   <span data-ttu-id="02246-313">**GUID**: {6DFD7C5C-2451-11D3-A299-00C04F8EF6AF}</span><span class="sxs-lookup"><span data-stu-id="02246-313">**GUID**: {6DFD7C5C-2451-11d3-A299-00C04F8EF6AF}</span></span>
-   <span data-ttu-id="02246-314">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-314">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-315">**Nom du module**: @% systemroot% \\ system32 \\shell32.dll,-22985</span><span class="sxs-lookup"><span data-stu-id="02246-315">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22985</span></span>

### <a name="fonts"></a><span data-ttu-id="02246-316">Polices</span><span class="sxs-lookup"><span data-stu-id="02246-316">Fonts</span></span>

-   <span data-ttu-id="02246-317">**Nom canonique**: Microsoft. fonts</span><span class="sxs-lookup"><span data-stu-id="02246-317">**Canonical name**: Microsoft.Fonts</span></span>
-   <span data-ttu-id="02246-318">**GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}</span><span class="sxs-lookup"><span data-stu-id="02246-318">**GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}</span></span>
-   <span data-ttu-id="02246-319">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-319">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-320">**Nom du module**: @% systemroot% \\ system32 \\FontExt.dll,-8007</span><span class="sxs-lookup"><span data-stu-id="02246-320">**Module name**: @%SystemRoot%\\System32\\FontExt.dll,-8007</span></span>

### <a name="homegroup"></a><span data-ttu-id="02246-321">Groupement résidentiel</span><span class="sxs-lookup"><span data-stu-id="02246-321">HomeGroup</span></span>

-   <span data-ttu-id="02246-322">**Nom canonique**: Microsoft. groupe résidentiel</span><span class="sxs-lookup"><span data-stu-id="02246-322">**Canonical name**: Microsoft.HomeGroup</span></span>
-   <span data-ttu-id="02246-323">**GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}</span><span class="sxs-lookup"><span data-stu-id="02246-323">**GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}</span></span>
-   <span data-ttu-id="02246-324">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-324">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-325">**Nom du module**: @% systemroot% \\ system32 \\hgcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-325">**Module name**: @%SystemRoot%\\System32\\hgcpl.dll,-1</span></span>

### <a name="indexing-options"></a><span data-ttu-id="02246-326">Options d’indexation</span><span class="sxs-lookup"><span data-stu-id="02246-326">Indexing Options</span></span>

-   <span data-ttu-id="02246-327">**Nom canonique**: Microsoft. IndexingOptions</span><span class="sxs-lookup"><span data-stu-id="02246-327">**Canonical name**: Microsoft.IndexingOptions</span></span>
-   <span data-ttu-id="02246-328">**GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}</span><span class="sxs-lookup"><span data-stu-id="02246-328">**GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}</span></span>
-   <span data-ttu-id="02246-329">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-329">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-330">**Nom du module**: @% systemroot% \\ system32 \\srchadmin.dll,-601</span><span class="sxs-lookup"><span data-stu-id="02246-330">**Module name**: @%SystemRoot%\\System32\\srchadmin.dll,-601</span></span>

### <a name="infrared"></a><span data-ttu-id="02246-331">Infrarouge</span><span class="sxs-lookup"><span data-stu-id="02246-331">Infrared</span></span>

-   <span data-ttu-id="02246-332">**Nom canonique**: Microsoft. infrarouge</span><span class="sxs-lookup"><span data-stu-id="02246-332">**Canonical name**: Microsoft.Infrared</span></span>
-   <span data-ttu-id="02246-333">**GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="02246-333">**GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span>
-   <span data-ttu-id="02246-334">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-334">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-335">**Nom du module**: @% systemroot% \\ system32 \\irprops.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="02246-335">**Module name**: @%SystemRoot%\\System32\\irprops.cpl,-1</span></span>

### <a name="internet-options"></a><span data-ttu-id="02246-336">Options Internet</span><span class="sxs-lookup"><span data-stu-id="02246-336">Internet Options</span></span>

-   <span data-ttu-id="02246-337">**Nom canonique**: Microsoft. InternetOptions</span><span class="sxs-lookup"><span data-stu-id="02246-337">**Canonical name**: Microsoft.InternetOptions</span></span>
-   <span data-ttu-id="02246-338">**GUID**: {A3DD4F92-658A-410f-84FD-6FBBBEF2FFFE}</span><span class="sxs-lookup"><span data-stu-id="02246-338">**GUID**: {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}</span></span>
-   <span data-ttu-id="02246-339">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-339">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-340">**Nom du module**: @C: \\ Windows \\ system32 \\inetcpl.cpl,-4312</span><span class="sxs-lookup"><span data-stu-id="02246-340">**Module name**: @C:\\Windows\\System32\\inetcpl.cpl,-4312</span></span>
-   <span data-ttu-id="02246-341">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-341">**Pages**</span></span>

    | <span data-ttu-id="02246-342">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-342">Page Name</span></span> | <span data-ttu-id="02246-343">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-343">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="02246-344">1</span><span class="sxs-lookup"><span data-stu-id="02246-344">1</span></span>         | <span data-ttu-id="02246-345">Sécurité</span><span class="sxs-lookup"><span data-stu-id="02246-345">Security</span></span>    |
    | <span data-ttu-id="02246-346">2</span><span class="sxs-lookup"><span data-stu-id="02246-346">2</span></span>         | <span data-ttu-id="02246-347">Confidentialité</span><span class="sxs-lookup"><span data-stu-id="02246-347">Privacy</span></span>     |
    | <span data-ttu-id="02246-348">3</span><span class="sxs-lookup"><span data-stu-id="02246-348">3</span></span>         | <span data-ttu-id="02246-349">Content</span><span class="sxs-lookup"><span data-stu-id="02246-349">Content</span></span>     |
    | <span data-ttu-id="02246-350">4</span><span class="sxs-lookup"><span data-stu-id="02246-350">4</span></span>         | <span data-ttu-id="02246-351">Connexions</span><span class="sxs-lookup"><span data-stu-id="02246-351">Connections</span></span> |
    | <span data-ttu-id="02246-352">5</span><span class="sxs-lookup"><span data-stu-id="02246-352">5</span></span>         | <span data-ttu-id="02246-353">Programmes</span><span class="sxs-lookup"><span data-stu-id="02246-353">Programs</span></span>    |
    | <span data-ttu-id="02246-354">6</span><span class="sxs-lookup"><span data-stu-id="02246-354">6</span></span>         | <span data-ttu-id="02246-355">Avancé</span><span class="sxs-lookup"><span data-stu-id="02246-355">Advanced</span></span>    |

    

     

### <a name="iscsi-initiator"></a><span data-ttu-id="02246-356">Initiateur iSCSI</span><span class="sxs-lookup"><span data-stu-id="02246-356">iSCSI Initiator</span></span>

-   <span data-ttu-id="02246-357">**Nom canonique**: Microsoft. iSCSIInitiator</span><span class="sxs-lookup"><span data-stu-id="02246-357">**Canonical name**: Microsoft.iSCSIInitiator</span></span>
-   <span data-ttu-id="02246-358">**GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span><span class="sxs-lookup"><span data-stu-id="02246-358">**GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span></span>
-   <span data-ttu-id="02246-359">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-359">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-360">**Nom du module**: @% systemroot% \\ system32 \\iscsicpl.dll,-5001</span><span class="sxs-lookup"><span data-stu-id="02246-360">**Module name**: @%SystemRoot%\\System32\\iscsicpl.dll,-5001</span></span>

### <a name="isns-server"></a><span data-ttu-id="02246-361">Serveur iSNS</span><span class="sxs-lookup"><span data-stu-id="02246-361">iSNS Server</span></span>

-   <span data-ttu-id="02246-362">**Nom canonique**: Microsoft. iSNSServer</span><span class="sxs-lookup"><span data-stu-id="02246-362">**Canonical name**: Microsoft.iSNSServer</span></span>
-   <span data-ttu-id="02246-363">**GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}</span><span class="sxs-lookup"><span data-stu-id="02246-363">**GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}</span></span>
-   <span data-ttu-id="02246-364">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-364">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-365">**Nom du module**: @% systemroot% \\ system32 \\isnssrv.dll,-5005</span><span class="sxs-lookup"><span data-stu-id="02246-365">**Module name**: @%SystemRoot%\\System32\\isnssrv.dll,-5005</span></span>
-   <span data-ttu-id="02246-366">Cet élément du panneau de configuration est visible uniquement dans les versions serveur de Windows.</span><span class="sxs-lookup"><span data-stu-id="02246-366">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="keyboard"></a><span data-ttu-id="02246-367">Clavier</span><span class="sxs-lookup"><span data-stu-id="02246-367">Keyboard</span></span>

-   <span data-ttu-id="02246-368">**Nom canonique**: Microsoft. Keyboard</span><span class="sxs-lookup"><span data-stu-id="02246-368">**Canonical name**: Microsoft.Keyboard</span></span>
-   <span data-ttu-id="02246-369">**GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}</span><span class="sxs-lookup"><span data-stu-id="02246-369">**GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}</span></span>
-   <span data-ttu-id="02246-370">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-370">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-371">**Nom du module**: @% systemroot% \\ system32 \\main.cpl,-102</span><span class="sxs-lookup"><span data-stu-id="02246-371">**Module name**: @%SystemRoot%\\System32\\main.cpl,-102</span></span>

### <a name="location-settings"></a><span data-ttu-id="02246-372">Paramètres d’emplacement</span><span class="sxs-lookup"><span data-stu-id="02246-372">Location Settings</span></span>

-   <span data-ttu-id="02246-373">**Nom canonique**: Microsoft. LocationSettings</span><span class="sxs-lookup"><span data-stu-id="02246-373">**Canonical name**: Microsoft.LocationSettings</span></span>
-   <span data-ttu-id="02246-374">**GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="02246-374">**GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}</span></span>
-   <span data-ttu-id="02246-375">**Système d’exploitation pris en charge**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-375">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-376">**Nom du module**: @% systemroot% \\ system32 \\SensorsCpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-376">**Module name**: @%SystemRoot%\\System32\\SensorsCpl.dll,-1</span></span>

### <a name="mouse"></a><span data-ttu-id="02246-377">Souris</span><span class="sxs-lookup"><span data-stu-id="02246-377">Mouse</span></span>

-   <span data-ttu-id="02246-378">**Nom canonique**: Microsoft. Mouse</span><span class="sxs-lookup"><span data-stu-id="02246-378">**Canonical name**: Microsoft.Mouse</span></span>
-   <span data-ttu-id="02246-379">**GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}</span><span class="sxs-lookup"><span data-stu-id="02246-379">**GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}</span></span>
-   <span data-ttu-id="02246-380">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-380">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-381">**Nom du module**: @% systemroot% \\ system32 \\main.cpl,-100</span><span class="sxs-lookup"><span data-stu-id="02246-381">**Module name**: @%SystemRoot%\\System32\\main.cpl,-100</span></span>
-   <span data-ttu-id="02246-382">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-382">**Pages**</span></span>

    | <span data-ttu-id="02246-383">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-383">Page Name</span></span> | <span data-ttu-id="02246-384">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-384">Opens</span></span>           |
    |-----------|-----------------|
    | <span data-ttu-id="02246-385">1</span><span class="sxs-lookup"><span data-stu-id="02246-385">1</span></span>         | <span data-ttu-id="02246-386">Pointeurs</span><span class="sxs-lookup"><span data-stu-id="02246-386">Pointers</span></span>        |
    | <span data-ttu-id="02246-387">2</span><span class="sxs-lookup"><span data-stu-id="02246-387">2</span></span>         | <span data-ttu-id="02246-388">Options du pointeur</span><span class="sxs-lookup"><span data-stu-id="02246-388">Pointer Options</span></span> |
    | <span data-ttu-id="02246-389">3</span><span class="sxs-lookup"><span data-stu-id="02246-389">3</span></span>         | <span data-ttu-id="02246-390">Roulette</span><span class="sxs-lookup"><span data-stu-id="02246-390">Wheel</span></span>           |
    | <span data-ttu-id="02246-391">4</span><span class="sxs-lookup"><span data-stu-id="02246-391">4</span></span>         | <span data-ttu-id="02246-392">Matériel</span><span class="sxs-lookup"><span data-stu-id="02246-392">Hardware</span></span>        |

    

     

### <a name="mpioconfiguration"></a><span data-ttu-id="02246-393">MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="02246-393">MPIOConfiguration</span></span>

-   <span data-ttu-id="02246-394">**Nom canonique**: Microsoft. MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="02246-394">**Canonical name**: Microsoft.MPIOConfiguration</span></span>
-   <span data-ttu-id="02246-395">**GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}</span><span class="sxs-lookup"><span data-stu-id="02246-395">**GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}</span></span>
-   <span data-ttu-id="02246-396">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-396">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-397">**Nom du module**: @% systemroot% \\ system32 \\mpiocpl.dll,-1000</span><span class="sxs-lookup"><span data-stu-id="02246-397">**Module name**: @%SystemRoot%\\System32\\mpiocpl.dll,-1000</span></span>
-   <span data-ttu-id="02246-398">Cet élément du panneau de configuration est visible uniquement dans les versions serveur de Windows.</span><span class="sxs-lookup"><span data-stu-id="02246-398">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="network-and-sharing-center"></a><span data-ttu-id="02246-399">Centre Réseau et partage</span><span class="sxs-lookup"><span data-stu-id="02246-399">Network and Sharing Center</span></span>

-   <span data-ttu-id="02246-400">**Nom canonique**: Microsoft. NetworkAndSharingCenter</span><span class="sxs-lookup"><span data-stu-id="02246-400">**Canonical name**: Microsoft.NetworkAndSharingCenter</span></span>
-   <span data-ttu-id="02246-401">**GUID**: {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}</span><span class="sxs-lookup"><span data-stu-id="02246-401">**GUID**: {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}</span></span>
-   <span data-ttu-id="02246-402">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-402">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-403">**Nom du module**: @% systemroot% \\ system32 \\netcenter.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-403">**Module name**: @%SystemRoot%\\System32\\netcenter.dll,-1</span></span>
-   <span data-ttu-id="02246-404">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-404">**Pages**</span></span>

    | <span data-ttu-id="02246-405">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-405">Page Name</span></span>  | <span data-ttu-id="02246-406">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-406">Opens</span></span>                     |
    |------------|---------------------------|
    | <span data-ttu-id="02246-407">Avancé</span><span class="sxs-lookup"><span data-stu-id="02246-407">Advanced</span></span>   | <span data-ttu-id="02246-408">Paramètres de partage avancés</span><span class="sxs-lookup"><span data-stu-id="02246-408">Advanced sharing settings</span></span> |
    | <span data-ttu-id="02246-409">ShareMedia</span><span class="sxs-lookup"><span data-stu-id="02246-409">ShareMedia</span></span> | <span data-ttu-id="02246-410">Options de diffusion multimédia en continu</span><span class="sxs-lookup"><span data-stu-id="02246-410">Media streaming options</span></span>   |

    

     

### <a name="notification-area-icons"></a><span data-ttu-id="02246-411">Icônes de la zone de notification</span><span class="sxs-lookup"><span data-stu-id="02246-411">Notification Area Icons</span></span>

-   <span data-ttu-id="02246-412">**Nom canonique**: Microsoft. NotificationAreaIcons</span><span class="sxs-lookup"><span data-stu-id="02246-412">**Canonical name**: Microsoft.NotificationAreaIcons</span></span>
-   <span data-ttu-id="02246-413">**GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}</span><span class="sxs-lookup"><span data-stu-id="02246-413">**GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}</span></span>
-   <span data-ttu-id="02246-414">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-414">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-415">**Nom du module**: @% systemroot% \\ system32 \\taskbarcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-415">**Module name**: @%SystemRoot%\\System32\\taskbarcpl.dll,-1</span></span>

### <a name="pen-and-touch"></a><span data-ttu-id="02246-416">Pen et Touch</span><span class="sxs-lookup"><span data-stu-id="02246-416">Pen and Touch</span></span>

-   <span data-ttu-id="02246-417">**Nom canonique**: Microsoft. PenAndTouch</span><span class="sxs-lookup"><span data-stu-id="02246-417">**Canonical name**: Microsoft.PenAndTouch</span></span>
-   <span data-ttu-id="02246-418">**GUID**: {F82DF8F7-8B9F-442e-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="02246-418">**GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span>
-   <span data-ttu-id="02246-419">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-419">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-420">**Nom du module**: @% systemroot% \\ system32 \\tabletpc.cpl,-10103</span><span class="sxs-lookup"><span data-stu-id="02246-420">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10103</span></span>
-   <span data-ttu-id="02246-421">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-421">**Pages**</span></span>

    | <span data-ttu-id="02246-422">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-422">Page Name</span></span> | <span data-ttu-id="02246-423">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-423">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="02246-424">1</span><span class="sxs-lookup"><span data-stu-id="02246-424">1</span></span>         | <span data-ttu-id="02246-425">Les raccourcis</span><span class="sxs-lookup"><span data-stu-id="02246-425">Flicks</span></span>      |
    | <span data-ttu-id="02246-426">2</span><span class="sxs-lookup"><span data-stu-id="02246-426">2</span></span>         | <span data-ttu-id="02246-427">Écriture manuscrite</span><span class="sxs-lookup"><span data-stu-id="02246-427">Handwriting</span></span> |

    

     

### <a name="personalization"></a><span data-ttu-id="02246-428">Personnalisation</span><span class="sxs-lookup"><span data-stu-id="02246-428">Personalization</span></span>

-   <span data-ttu-id="02246-429">**Nom canonique**: Microsoft. Personalization</span><span class="sxs-lookup"><span data-stu-id="02246-429">**Canonical name**: Microsoft.Personalization</span></span>
-   <span data-ttu-id="02246-430">**GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span><span class="sxs-lookup"><span data-stu-id="02246-430">**GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span></span>
-   <span data-ttu-id="02246-431">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-431">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-432">**Nom du module**: @% systemroot% \\ system32 \\themecpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-432">**Module name**: @%SystemRoot%\\System32\\themecpl.dll,-1</span></span>
-   <span data-ttu-id="02246-433">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-433">**Pages**</span></span>

    | <span data-ttu-id="02246-434">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-434">Page Name</span></span>        | <span data-ttu-id="02246-435">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-435">Opens</span></span>                |
    |------------------|----------------------|
    | <span data-ttu-id="02246-436">pageColorization</span><span class="sxs-lookup"><span data-stu-id="02246-436">pageColorization</span></span> | <span data-ttu-id="02246-437">Couleur et apparence</span><span class="sxs-lookup"><span data-stu-id="02246-437">Color and Appearance</span></span> |
    | <span data-ttu-id="02246-438">pageWallpaper</span><span class="sxs-lookup"><span data-stu-id="02246-438">pageWallpaper</span></span>    | <span data-ttu-id="02246-439">Arrière-plan du Bureau</span><span class="sxs-lookup"><span data-stu-id="02246-439">Desktop Background</span></span>   |

    

     

### <a name="phone-and-modem"></a><span data-ttu-id="02246-440">Téléphone et modem</span><span class="sxs-lookup"><span data-stu-id="02246-440">Phone and Modem</span></span>

-   <span data-ttu-id="02246-441">**Nom canonique**: Microsoft. PhoneAndModem</span><span class="sxs-lookup"><span data-stu-id="02246-441">**Canonical name**: Microsoft.PhoneAndModem</span></span>
-   <span data-ttu-id="02246-442">**GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}</span><span class="sxs-lookup"><span data-stu-id="02246-442">**GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}</span></span>
-   <span data-ttu-id="02246-443">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-443">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-444">**Nom du module**: @% systemroot% \\ system32 \\telephon.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="02246-444">**Module name**: @%SystemRoot%\\System32\\telephon.cpl,-1</span></span>
-   <span data-ttu-id="02246-445">La fenêtre lancée par cette valeur est intitulée « informations sur l’emplacement » dans les versions de Windows antérieures à Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02246-445">The window that this value launches is titled "Location Information" in versions of Windows prior to Windows 8.</span></span> <span data-ttu-id="02246-446">L’interface utilisateur de l’élément est considérablement modifiée à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02246-446">The item's UI is considerably changed as of Windows 8.</span></span>

### <a name="power-options"></a><span data-ttu-id="02246-447">Options d’alimentation</span><span class="sxs-lookup"><span data-stu-id="02246-447">Power Options</span></span>

-   <span data-ttu-id="02246-448">**Nom canonique**: Microsoft. PowerOptions</span><span class="sxs-lookup"><span data-stu-id="02246-448">**Canonical name**: Microsoft.PowerOptions</span></span>
-   <span data-ttu-id="02246-449">**GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}</span><span class="sxs-lookup"><span data-stu-id="02246-449">**GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}</span></span>
-   <span data-ttu-id="02246-450">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-450">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-451">**Nom du module**: @% systemroot% \\ system32 \\powercpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-451">**Module name**: @%SystemRoot%\\System32\\powercpl.dll,-1</span></span>
-   <span data-ttu-id="02246-452">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-452">**Pages**</span></span>

    | <span data-ttu-id="02246-453">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-453">Page Name</span></span>          | <span data-ttu-id="02246-454">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-454">Opens</span></span>              |
    |--------------------|--------------------|
    | <span data-ttu-id="02246-455">pageGlobalSettings</span><span class="sxs-lookup"><span data-stu-id="02246-455">pageGlobalSettings</span></span> | <span data-ttu-id="02246-456">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="02246-456">System Settings</span></span>    |
    | <span data-ttu-id="02246-457">pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="02246-457">pagePlanSettings</span></span>   | <span data-ttu-id="02246-458">Modifier les paramètres du plan</span><span class="sxs-lookup"><span data-stu-id="02246-458">Edit Plan Settings</span></span> |

    

     

### <a name="programs-and-features"></a><span data-ttu-id="02246-459">Programmes et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="02246-459">Programs and Features</span></span>

-   <span data-ttu-id="02246-460">**Nom canonique**: Microsoft. ProgramsAndFeatures</span><span class="sxs-lookup"><span data-stu-id="02246-460">**Canonical name**: Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="02246-461">**GUID**: {7b81be6a-ce2b-4676-A29E-eb907a5126c5}</span><span class="sxs-lookup"><span data-stu-id="02246-461">**GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}</span></span>
-   <span data-ttu-id="02246-462">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-462">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-463">**Nom du module**: @% systemroot% \\ system32 \\appwiz.cpl,-159</span><span class="sxs-lookup"><span data-stu-id="02246-463">**Module name**: @%systemroot%\\system32\\appwiz.cpl,-159</span></span>
-   <span data-ttu-id="02246-464">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-464">**Pages**</span></span>

    | <span data-ttu-id="02246-465">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-465">Page Name</span></span>                                | <span data-ttu-id="02246-466">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-466">Opens</span></span>             |
    |------------------------------------------|-------------------|
    | <span data-ttu-id="02246-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span><span class="sxs-lookup"><span data-stu-id="02246-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span></span> | <span data-ttu-id="02246-468">Mises à jour installées</span><span class="sxs-lookup"><span data-stu-id="02246-468">Installed Updates</span></span> |

    

     

### <a name="recovery"></a><span data-ttu-id="02246-469">Récupération</span><span class="sxs-lookup"><span data-stu-id="02246-469">Recovery</span></span>

-   <span data-ttu-id="02246-470">**Nom canonique**: Microsoft. Recovery</span><span class="sxs-lookup"><span data-stu-id="02246-470">**Canonical name**: Microsoft.Recovery</span></span>
-   <span data-ttu-id="02246-471">**GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}</span><span class="sxs-lookup"><span data-stu-id="02246-471">**GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}</span></span>
-   <span data-ttu-id="02246-472">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-472">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-473">**Nom du module**: @% systemroot% \\ system32 \\recovery.dll,-101</span><span class="sxs-lookup"><span data-stu-id="02246-473">**Module name**: @%SystemRoot%\\System32\\recovery.dll,-101</span></span>

### <a name="region"></a><span data-ttu-id="02246-474">Région</span><span class="sxs-lookup"><span data-stu-id="02246-474">Region</span></span>

-   <span data-ttu-id="02246-475">**Nom canonique**: Microsoft. RegionAndLanguage</span><span class="sxs-lookup"><span data-stu-id="02246-475">**Canonical name**: Microsoft.RegionAndLanguage</span></span>
-   <span data-ttu-id="02246-476">**GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span><span class="sxs-lookup"><span data-stu-id="02246-476">**GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span>
-   <span data-ttu-id="02246-477">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-477">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-478">**Nom du module**: @% systemroot% \\ system32 \\intl.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="02246-478">**Module name**: @%SystemRoot%\\System32\\intl.cpl,-1</span></span>
-   <span data-ttu-id="02246-479">La région et l’élément de langue trouvés dans Windows 7 ont été fractionnés à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02246-479">The Region and Language item found in Windows 7 was split as of Windows 8.</span></span> <span data-ttu-id="02246-480">Microsoft. RegionAndLanguage lance maintenant l’élément Region.</span><span class="sxs-lookup"><span data-stu-id="02246-480">Microsoft.RegionAndLanguage now launches the Region item.</span></span> <span data-ttu-id="02246-481">Pour lancer l’élément de langue, utilisez [Microsoft. Language](#location-settings).</span><span class="sxs-lookup"><span data-stu-id="02246-481">To launch the Language item, use [Microsoft.Language](#location-settings).</span></span>
-   <span data-ttu-id="02246-482">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-482">**Pages**</span></span>

    | <span data-ttu-id="02246-483">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-483">Page Name</span></span> | <span data-ttu-id="02246-484">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-484">Opens</span></span>          |
    |-----------|----------------|
    | <span data-ttu-id="02246-485">1</span><span class="sxs-lookup"><span data-stu-id="02246-485">1</span></span>         | <span data-ttu-id="02246-486">Emplacement</span><span class="sxs-lookup"><span data-stu-id="02246-486">Location</span></span>       |
    | <span data-ttu-id="02246-487">2</span><span class="sxs-lookup"><span data-stu-id="02246-487">2</span></span>         | <span data-ttu-id="02246-488">Administratif</span><span class="sxs-lookup"><span data-stu-id="02246-488">Administrative</span></span> |

    

     

### <a name="remoteapp-and-desktop-connections"></a><span data-ttu-id="02246-489">Connexions aux programmes RemoteApp et aux services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="02246-489">RemoteApp and Desktop Connections</span></span>

-   <span data-ttu-id="02246-490">**Nom canonique**: Microsoft. RemoteAppAndDesktopConnections</span><span class="sxs-lookup"><span data-stu-id="02246-490">**Canonical name**: Microsoft.RemoteAppAndDesktopConnections</span></span>
-   <span data-ttu-id="02246-491">**GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}</span><span class="sxs-lookup"><span data-stu-id="02246-491">**GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}</span></span>
-   <span data-ttu-id="02246-492">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-492">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-493">**Nom du module**: @% systemroot% \\ system32 \\tsworkspace.dll,-15300</span><span class="sxs-lookup"><span data-stu-id="02246-493">**Module name**: @%SystemRoot%\\System32\\tsworkspace.dll,-15300</span></span>

### <a name="sound"></a><span data-ttu-id="02246-494">Son</span><span class="sxs-lookup"><span data-stu-id="02246-494">Sound</span></span>

-   <span data-ttu-id="02246-495">**Nom canonique**: Microsoft. Sound</span><span class="sxs-lookup"><span data-stu-id="02246-495">**Canonical name**: Microsoft.Sound</span></span>
-   <span data-ttu-id="02246-496">**GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="02246-496">**GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span>
-   <span data-ttu-id="02246-497">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-497">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-498">**Nom du module**: @% systemroot% \\ system32 \\mmsys.cpl,-300</span><span class="sxs-lookup"><span data-stu-id="02246-498">**Module name**: @%SystemRoot%\\System32\\mmsys.cpl,-300</span></span>

### <a name="speech-recognition"></a><span data-ttu-id="02246-499">Reconnaissance vocale</span><span class="sxs-lookup"><span data-stu-id="02246-499">Speech Recognition</span></span>

-   <span data-ttu-id="02246-500">**Nom canonique**: Microsoft. SpeechRecognition</span><span class="sxs-lookup"><span data-stu-id="02246-500">**Canonical name**: Microsoft.SpeechRecognition</span></span>
-   <span data-ttu-id="02246-501">**GUID**: {58E3C745-D971-4081-9034-86E34B30836A}</span><span class="sxs-lookup"><span data-stu-id="02246-501">**GUID**: {58E3C745-D971-4081-9034-86E34B30836A}</span></span>
-   <span data-ttu-id="02246-502">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-502">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-503">**Nom du module**: @% systemroot% \\ System32 \\ Speech \\ SpeechUX \\speechuxcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-503">**Module name**: @%SystemRoot%\\System32\\Speech\\SpeechUX\\speechuxcpl.dll,-1</span></span>

### <a name="storage-spaces"></a><span data-ttu-id="02246-504">Espaces de stockage</span><span class="sxs-lookup"><span data-stu-id="02246-504">Storage Spaces</span></span>

-   <span data-ttu-id="02246-505">**Nom canonique**: Microsoft. StorageSpaces</span><span class="sxs-lookup"><span data-stu-id="02246-505">**Canonical name**: Microsoft.StorageSpaces</span></span>
-   <span data-ttu-id="02246-506">**GUID**: {F942C606-0914-47AB-BE56-1321B8035096}</span><span class="sxs-lookup"><span data-stu-id="02246-506">**GUID**: {F942C606-0914-47AB-BE56-1321B8035096}</span></span>
-   <span data-ttu-id="02246-507">**Système d’exploitation pris en charge**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-507">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-508">**Nom du module**: @C: \\ Windows \\ system32 \\SpaceControl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-508">**Module name**: @C:\\Windows\\System32\\SpaceControl.dll,-1</span></span>

### <a name="sync-center"></a><span data-ttu-id="02246-509">Centre de synchronisation</span><span class="sxs-lookup"><span data-stu-id="02246-509">Sync Center</span></span>

-   <span data-ttu-id="02246-510">**Nom canonique**: Microsoft. synccenter</span><span class="sxs-lookup"><span data-stu-id="02246-510">**Canonical name**: Microsoft.SyncCenter</span></span>
-   <span data-ttu-id="02246-511">**GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}</span><span class="sxs-lookup"><span data-stu-id="02246-511">**GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}</span></span>
-   <span data-ttu-id="02246-512">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-512">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-513">**Nom du module**: @% systemroot% \\ system32 \\SyncCenter.dll,-3000</span><span class="sxs-lookup"><span data-stu-id="02246-513">**Module name**: @%SystemRoot%\\System32\\SyncCenter.dll,-3000</span></span>

### <a name="system"></a><span data-ttu-id="02246-514">Système</span><span class="sxs-lookup"><span data-stu-id="02246-514">System</span></span>

-   <span data-ttu-id="02246-515">**Nom canonique**: Microsoft.SysTEM</span><span class="sxs-lookup"><span data-stu-id="02246-515">**Canonical name**: Microsoft.System</span></span>
-   <span data-ttu-id="02246-516">**GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span><span class="sxs-lookup"><span data-stu-id="02246-516">**GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span></span>
-   <span data-ttu-id="02246-517">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-517">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-518">**Nom du module**: @% systemroot% \\ system32 \\systemcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-518">**Module name**: @%SystemRoot%\\System32\\systemcpl.dll,-1</span></span>

### <a name="tablet-pc-settings"></a><span data-ttu-id="02246-519">Paramètres du Tablet PC</span><span class="sxs-lookup"><span data-stu-id="02246-519">Tablet PC Settings</span></span>

-   <span data-ttu-id="02246-520">**Nom canonique**: Microsoft. TabletPCSettings</span><span class="sxs-lookup"><span data-stu-id="02246-520">**Canonical name**: Microsoft.TabletPCSettings</span></span>
-   <span data-ttu-id="02246-521">**GUID**: {80F3F1D5-FECA-45F3-BC32-752C152E456E}</span><span class="sxs-lookup"><span data-stu-id="02246-521">**GUID**: {80F3F1D5-FECA-45F3-BC32-752C152E456E}</span></span>
-   <span data-ttu-id="02246-522">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-522">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-523">**Nom du module**: @% systemroot% \\ system32 \\tabletpc.cpl,-10100</span><span class="sxs-lookup"><span data-stu-id="02246-523">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10100</span></span>

### <a name="taskbar-and-navigation"></a><span data-ttu-id="02246-524">Barre des tâches et navigation</span><span class="sxs-lookup"><span data-stu-id="02246-524">Taskbar and Navigation</span></span>

-   <span data-ttu-id="02246-525">**Nom canonique**: Microsoft. Taskbar</span><span class="sxs-lookup"><span data-stu-id="02246-525">**Canonical name**: Microsoft.Taskbar</span></span>
-   <span data-ttu-id="02246-526">**GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}</span><span class="sxs-lookup"><span data-stu-id="02246-526">**GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span>
-   <span data-ttu-id="02246-527">**Système d’exploitation pris en charge**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-527">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-528">**Nom du module**: @% systemroot% \\ system32 \\shell32.dll,-32517</span><span class="sxs-lookup"><span data-stu-id="02246-528">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-32517</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="02246-529">Dépannage</span><span class="sxs-lookup"><span data-stu-id="02246-529">Troubleshooting</span></span>

-   <span data-ttu-id="02246-530">**Nom canonique**: Microsoft. Troubleshooting</span><span class="sxs-lookup"><span data-stu-id="02246-530">**Canonical name**: Microsoft.Troubleshooting</span></span>
-   <span data-ttu-id="02246-531">**GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span><span class="sxs-lookup"><span data-stu-id="02246-531">**GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span></span>
-   <span data-ttu-id="02246-532">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-532">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-533">**Nom du module**: @% systemroot% \\ system32 \\DiagCpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-533">**Module name**: @%SystemRoot%\\System32\\DiagCpl.dll,-1</span></span>
-   <span data-ttu-id="02246-534">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-534">**Pages**</span></span>

    | <span data-ttu-id="02246-535">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-535">Page Name</span></span>   | <span data-ttu-id="02246-536">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-536">Opens</span></span>   |
    |-------------|---------|
    | <span data-ttu-id="02246-537">HistoryPage</span><span class="sxs-lookup"><span data-stu-id="02246-537">HistoryPage</span></span> | <span data-ttu-id="02246-538">Historique</span><span class="sxs-lookup"><span data-stu-id="02246-538">History</span></span> |

    

     

### <a name="tsappinstall"></a><span data-ttu-id="02246-539">TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="02246-539">TSAppInstall</span></span>

-   <span data-ttu-id="02246-540">**Nom canonique**: Microsoft. TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="02246-540">**Canonical name**: Microsoft.TSAppInstall</span></span>
-   <span data-ttu-id="02246-541">**GUID**: {BAA884F4-3432-48B8-AA72-9BF20EEF31D5}</span><span class="sxs-lookup"><span data-stu-id="02246-541">**GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}</span></span>
-   <span data-ttu-id="02246-542">**Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-542">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-543">**Nom du module**: @% systemroot% \\ system32 \\tsappinstall.exe,-2001</span><span class="sxs-lookup"><span data-stu-id="02246-543">**Module name**: @%systemroot%\\system32\\tsappinstall.exe,-2001</span></span>

### <a name="user-accounts"></a><span data-ttu-id="02246-544">Comptes d'utilisateurs</span><span class="sxs-lookup"><span data-stu-id="02246-544">User Accounts</span></span>

-   <span data-ttu-id="02246-545">**Nom canonique**: Microsoft. UserAccounts</span><span class="sxs-lookup"><span data-stu-id="02246-545">**Canonical name**: Microsoft.UserAccounts</span></span>
-   <span data-ttu-id="02246-546">**GUID**: {60632754-C523-4B62-b45c-4172da012619}</span><span class="sxs-lookup"><span data-stu-id="02246-546">**GUID**: {60632754-c523-4b62-b45c-4172da012619}</span></span>
-   <span data-ttu-id="02246-547">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-547">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-548">**Nom du module**: @% systemroot% \\ system32 \\usercpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-548">**Module name**: @%SystemRoot%\\System32\\usercpl.dll,-1</span></span>

### <a name="windows-anytime-upgrade"></a><span data-ttu-id="02246-549">Mise à niveau express</span><span class="sxs-lookup"><span data-stu-id="02246-549">Windows Anytime Upgrade</span></span>

-   <span data-ttu-id="02246-550">**Nom canonique**: Microsoft. WindowsAnytimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="02246-550">**Canonical name**: Microsoft.WindowsAnytimeUpgrade</span></span>
-   <span data-ttu-id="02246-551">**GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}</span><span class="sxs-lookup"><span data-stu-id="02246-551">**GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}</span></span>
-   <span data-ttu-id="02246-552">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-552">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-553">**Nom du module**: @ $ (resourceString. \_ SYS \_ Mod \_ chemin d’accès),-1</span><span class="sxs-lookup"><span data-stu-id="02246-553">**Module name**: @$(resourceString.\_SYS\_MOD\_PATH),-1</span></span>

### <a name="windows-defender"></a><span data-ttu-id="02246-554">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="02246-554">Windows Defender</span></span>

-   <span data-ttu-id="02246-555">**Nom canonique**: Microsoft. Windowsdefender</span><span class="sxs-lookup"><span data-stu-id="02246-555">**Canonical name**: Microsoft.WindowsDefender</span></span>
-   <span data-ttu-id="02246-556">**GUID**: {D8559EB9-20C0-410E-Beda-7ED416AECC2A}</span><span class="sxs-lookup"><span data-stu-id="02246-556">**GUID**: {D8559EB9-20C0-410E-BEDA-7ED416AECC2A}</span></span>
-   <span data-ttu-id="02246-557">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-557">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-558">**Nom du module**: @% ProgramFiles% \\ Windows Defender \\MsMpRes.dll,-104</span><span class="sxs-lookup"><span data-stu-id="02246-558">**Module name**: @%ProgramFiles%\\Windows Defender\\MsMpRes.dll,-104</span></span>

### <a name="windows-firewall"></a><span data-ttu-id="02246-559">Pare-feu Windows</span><span class="sxs-lookup"><span data-stu-id="02246-559">Windows Firewall</span></span>

-   <span data-ttu-id="02246-560">**Nom canonique**: Microsoft. WindowsFirewall</span><span class="sxs-lookup"><span data-stu-id="02246-560">**Canonical name**: Microsoft.WindowsFirewall</span></span>
-   <span data-ttu-id="02246-561">**GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}</span><span class="sxs-lookup"><span data-stu-id="02246-561">**GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}</span></span>
-   <span data-ttu-id="02246-562">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-562">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-563">**Nom du module**: @C: \\ Windows \\ system32 \\FirewallControlPanel.dll,-12122</span><span class="sxs-lookup"><span data-stu-id="02246-563">**Module name**: @C:\\Windows\\system32\\FirewallControlPanel.dll,-12122</span></span>
-   <span data-ttu-id="02246-564">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-564">**Pages**</span></span>

    | <span data-ttu-id="02246-565">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-565">Page Name</span></span>         | <span data-ttu-id="02246-566">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-566">Opens</span></span>        |
    |-------------------|--------------|
    | <span data-ttu-id="02246-567">pageConfigureApps</span><span class="sxs-lookup"><span data-stu-id="02246-567">pageConfigureApps</span></span> | <span data-ttu-id="02246-568">Applications autorisées</span><span class="sxs-lookup"><span data-stu-id="02246-568">Allowed apps</span></span> |

    

     

### <a name="windows-mobility-center"></a><span data-ttu-id="02246-569">Centre de mobilité Windows</span><span class="sxs-lookup"><span data-stu-id="02246-569">Windows Mobility Center</span></span>

-   <span data-ttu-id="02246-570">**Nom canonique**: Microsoft. MobilityCenter</span><span class="sxs-lookup"><span data-stu-id="02246-570">**Canonical name**: Microsoft.MobilityCenter</span></span>
-   <span data-ttu-id="02246-571">**GUID**: {5ea4f148-308C-46d7-98a9-49041b1dd468}</span><span class="sxs-lookup"><span data-stu-id="02246-571">**GUID**: {5ea4f148-308c-46d7-98a9-49041b1dd468}</span></span>
-   <span data-ttu-id="02246-572">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-572">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-573">**Nom du module**: @% systemroot% \\ system32 \\mblctr.exe,-1002</span><span class="sxs-lookup"><span data-stu-id="02246-573">**Module name**: @%SystemRoot%\\system32\\mblctr.exe,-1002</span></span>

### <a name="windows-to-go"></a><span data-ttu-id="02246-574">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="02246-574">Windows To Go</span></span>

-   <span data-ttu-id="02246-575">**Nom canonique**: Microsoft. PortableWorkspaceCreator</span><span class="sxs-lookup"><span data-stu-id="02246-575">**Canonical name**: Microsoft.PortableWorkspaceCreator</span></span>
-   <span data-ttu-id="02246-576">**GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}</span><span class="sxs-lookup"><span data-stu-id="02246-576">**GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}</span></span>
-   <span data-ttu-id="02246-577">**Système d’exploitation pris en charge**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-577">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-578">**Nom du module**: @% systemroot% \\ system32 \\pwcreator.exe,-151</span><span class="sxs-lookup"><span data-stu-id="02246-578">**Module name**: @%SystemRoot%\\System32\\pwcreator.exe,-151</span></span>

### <a name="windows-update"></a><span data-ttu-id="02246-579">Windows Update</span><span class="sxs-lookup"><span data-stu-id="02246-579">Windows Update</span></span>

-   <span data-ttu-id="02246-580">**Nom canonique**: Microsoft. windowsupdate</span><span class="sxs-lookup"><span data-stu-id="02246-580">**Canonical name**: Microsoft.WindowsUpdate</span></span>
-   <span data-ttu-id="02246-581">**GUID**: {36eef7db-88ad-4E81-AD49-0e313f0c35f8}</span><span class="sxs-lookup"><span data-stu-id="02246-581">**GUID**: {36eef7db-88ad-4e81-ad49-0e313f0c35f8}</span></span>
-   <span data-ttu-id="02246-582">**Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-582">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="02246-583">**Nom du module**: @% systemroot% \\ system32 \\wucltux.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-583">**Module name**: @%SystemRoot%\\system32\\wucltux.dll,-1</span></span>
-   <span data-ttu-id="02246-584">**Pages**</span><span class="sxs-lookup"><span data-stu-id="02246-584">**Pages**</span></span>

    | <span data-ttu-id="02246-585">Nom de la page</span><span class="sxs-lookup"><span data-stu-id="02246-585">Page Name</span></span>         | <span data-ttu-id="02246-586">Opens</span><span class="sxs-lookup"><span data-stu-id="02246-586">Opens</span></span>               |
    |-------------------|---------------------|
    | <span data-ttu-id="02246-587">pageSettings</span><span class="sxs-lookup"><span data-stu-id="02246-587">pageSettings</span></span>      | <span data-ttu-id="02246-588">Modifier les paramètres</span><span class="sxs-lookup"><span data-stu-id="02246-588">Change settings</span></span>     |
    | <span data-ttu-id="02246-589">pageUpdateHistory</span><span class="sxs-lookup"><span data-stu-id="02246-589">pageUpdateHistory</span></span> | <span data-ttu-id="02246-590">Afficher l’historique des mises à jour</span><span class="sxs-lookup"><span data-stu-id="02246-590">View update history</span></span> |

    

     

### <a name="work-folders"></a><span data-ttu-id="02246-591">Dossiers de travail</span><span class="sxs-lookup"><span data-stu-id="02246-591">Work Folders</span></span>

-   <span data-ttu-id="02246-592">**Nom canonique**: Microsoft. WorkFolders</span><span class="sxs-lookup"><span data-stu-id="02246-592">**Canonical name**: Microsoft.WorkFolders</span></span>
-   <span data-ttu-id="02246-593">**GUID**: {ECDB0924-4208-451e-8EE0-373C0956DE16}</span><span class="sxs-lookup"><span data-stu-id="02246-593">**GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}</span></span>
-   <span data-ttu-id="02246-594">**Système d’exploitation pris en charge**: Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02246-594">**Supported OS**: Windows 8.1</span></span>
-   <span data-ttu-id="02246-595">**Nom du module**: @C: \\ Windows \\ system32 \\WorkfoldersControl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="02246-595">**Module name**: @C:\\Windows\\System32\\WorkfoldersControl.dll,-1</span></span>

## <a name="deprecated-control-panel-canonical-names"></a><span data-ttu-id="02246-596">Noms canoniques du panneau de configuration déconseillés</span><span class="sxs-lookup"><span data-stu-id="02246-596">Deprecated Control Panel Canonical Names</span></span>

<span data-ttu-id="02246-597">Les noms canoniques suivants ne sont plus utilisés à la Windows 8.1 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="02246-597">The following are canonical names that are no longer in use as of Windows 8.1 or later.</span></span> <span data-ttu-id="02246-598">Certains ont été complètement supprimés.</span><span class="sxs-lookup"><span data-stu-id="02246-598">Some have been removed altogether.</span></span> <span data-ttu-id="02246-599">D’autres ont été remappés dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="02246-599">Others have been remapped in these situations:</span></span>

-   <span data-ttu-id="02246-600">Un élément du panneau de configuration est renommé.</span><span class="sxs-lookup"><span data-stu-id="02246-600">A Control Panel item is renamed.</span></span> <span data-ttu-id="02246-601">Un nouveau nom canonique est attribué à l’élément renommé, mais conserve le même GUID.</span><span class="sxs-lookup"><span data-stu-id="02246-601">The renamed item is given a new canonical name but keeps the same GUID.</span></span> <span data-ttu-id="02246-602">Dans ce cas, l’ancien nom canonique lance l’élément renommé du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="02246-602">In this case, the old canonical name launches the renamed Control Panel item.</span></span> <span data-ttu-id="02246-603">Sachez que l’élément lancé peut ne pas utiliser la même interface utilisateur que la version antérieure de cet élément.</span><span class="sxs-lookup"><span data-stu-id="02246-603">Be aware that the item that's launched might not use the same UI as that item's older version.</span></span>
-   <span data-ttu-id="02246-604">La fonctionnalité d’un ou de plusieurs éléments du panneau de configuration est déplacée ou consolidée dans un nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="02246-604">The functionality of one or more Control Panel items is moved or consolidated into a new item.</span></span> <span data-ttu-id="02246-605">Dans ce cas, l’ancien nom canonique est mappé au nouvel élément de panneau de configuration le plus approprié.</span><span class="sxs-lookup"><span data-stu-id="02246-605">In this case, the old canonical name maps to the most appropriate new Control Panel item.</span></span>

> [!Note]  
> <span data-ttu-id="02246-606">Des remappages existent pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="02246-606">Remappings exist for backward compatibility.</span></span> <span data-ttu-id="02246-607">Vous ne devez pas utiliser de valeurs déconseillées dans le nouveau code.</span><span class="sxs-lookup"><span data-stu-id="02246-607">You should not use deprecated values in new code.</span></span>

 



| <span data-ttu-id="02246-608">Nom canonique déconseillé</span><span class="sxs-lookup"><span data-stu-id="02246-608">Deprecated canonical name</span></span>                                   | <span data-ttu-id="02246-609">Élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="02246-609">Control Panel Item</span></span>                | <span data-ttu-id="02246-610">GUID</span><span class="sxs-lookup"><span data-stu-id="02246-610">GUID</span></span>                                   | <span data-ttu-id="02246-611">Notes</span><span class="sxs-lookup"><span data-stu-id="02246-611">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02246-612">Microsoft. AddHardware</span><span class="sxs-lookup"><span data-stu-id="02246-612">Microsoft.AddHardware</span></span>                                       | <span data-ttu-id="02246-613">Ajouter un matériel</span><span class="sxs-lookup"><span data-stu-id="02246-613">Add Hardware</span></span>                      | <span data-ttu-id="02246-614">{7A979262-40CE-46ff-AEEE-7884AC3B6136}</span><span class="sxs-lookup"><span data-stu-id="02246-614">{7A979262-40CE-46ff-AEEE-7884AC3B6136}</span></span> | <span data-ttu-id="02246-615">Correspond à [Microsoft. DevicesAndPrinters](#devices-and-printers) à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-615">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="02246-616">Microsoft. AudioDevicesAndSoundThemes</span><span class="sxs-lookup"><span data-stu-id="02246-616">Microsoft.AudioDevicesAndSoundThemes</span></span>                        | <span data-ttu-id="02246-617">Son</span><span class="sxs-lookup"><span data-stu-id="02246-617">Sound</span></span>                             | <span data-ttu-id="02246-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="02246-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span> | <span data-ttu-id="02246-619">Correspond à [Microsoft. Sound](#sound) depuis Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-619">Maps to [Microsoft.Sound](#sound) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="02246-620">Microsoft. BackupAndRestoreCenter/Microsoft. BackupAndRestore</span><span class="sxs-lookup"><span data-stu-id="02246-620">Microsoft.BackupAndRestoreCenter/Microsoft.BackupAndRestore</span></span> | <span data-ttu-id="02246-621">Centre de sauvegarde et de restauration</span><span class="sxs-lookup"><span data-stu-id="02246-621">Backup and Restore Center</span></span>         | <span data-ttu-id="02246-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span><span class="sxs-lookup"><span data-stu-id="02246-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span></span> | <span data-ttu-id="02246-623">Microsoft. BackupAndRestoreCenter est mappé à Microsoft. BackupAndRestore dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-623">Microsoft.BackupAndRestoreCenter maps to Microsoft.BackupAndRestore in Windows 7.</span></span> <span data-ttu-id="02246-624">Les deux sont supprimés à partir de Windows 8 ; Utilisez à la place [Microsoft. FileHistory](#file-history) .</span><span class="sxs-lookup"><span data-stu-id="02246-624">Both are removed as of Windows 8; use [Microsoft.FileHistory](#file-history) instead.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="02246-625">Microsoft. CardSpace</span><span class="sxs-lookup"><span data-stu-id="02246-625">Microsoft.CardSpace</span></span>                                         | <span data-ttu-id="02246-626">Windows CardSpace</span><span class="sxs-lookup"><span data-stu-id="02246-626">Windows CardSpace</span></span>                 | <span data-ttu-id="02246-627">{78CB147A-98EA-4AA6-B0DF-C8681F69341C}</span><span class="sxs-lookup"><span data-stu-id="02246-627">{78CB147A-98EA-4AA6-B0DF-C8681F69341C}</span></span> | <span data-ttu-id="02246-628">Suppression depuis Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02246-628">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="02246-629">Microsoft. DesktopGadgets</span><span class="sxs-lookup"><span data-stu-id="02246-629">Microsoft.DesktopGadgets</span></span>                                    | <span data-ttu-id="02246-630">Gadgets du Bureau</span><span class="sxs-lookup"><span data-stu-id="02246-630">Desktop Gadgets</span></span>                   | <span data-ttu-id="02246-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="02246-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="02246-632">Suppression depuis Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02246-632">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="02246-633">Microsoft. GetProgramsOnline</span><span class="sxs-lookup"><span data-stu-id="02246-633">Microsoft.GetProgramsOnline</span></span>                                 | <span data-ttu-id="02246-634">Place de marché Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="02246-634">Windows Marketplace</span></span>               | <span data-ttu-id="02246-635">{3e7efb4c-faf1-453d-89eb-56026875ef90}</span><span class="sxs-lookup"><span data-stu-id="02246-635">{3e7efb4c-faf1-453d-89eb-56026875ef90}</span></span> | <span data-ttu-id="02246-636">Suppression depuis Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-636">Removed as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="02246-637">Microsoft. InfraredOptions</span><span class="sxs-lookup"><span data-stu-id="02246-637">Microsoft.InfraredOptions</span></span>                                   | <span data-ttu-id="02246-638">Infrarouge</span><span class="sxs-lookup"><span data-stu-id="02246-638">Infrared</span></span>                          | <span data-ttu-id="02246-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="02246-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span> | <span data-ttu-id="02246-640">Correspond à [Microsoft. infrarouge](#infrared) à compter de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-640">Maps to [Microsoft.Infrared](#infrared) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="02246-641">Microsoft. langue</span><span class="sxs-lookup"><span data-stu-id="02246-641">Microsoft.Language</span></span>                                          | <span data-ttu-id="02246-642">Langage</span><span class="sxs-lookup"><span data-stu-id="02246-642">Language</span></span>                          | <span data-ttu-id="02246-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span><span class="sxs-lookup"><span data-stu-id="02246-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span></span> | <span data-ttu-id="02246-644">Supprimé à partir de Windows 10, version 1803</span><span class="sxs-lookup"><span data-stu-id="02246-644">Removed as of Windows 10, version 1803</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="02246-645">Microsoft. LocationAndOtherSensors</span><span class="sxs-lookup"><span data-stu-id="02246-645">Microsoft.LocationAndOtherSensors</span></span>                           | <span data-ttu-id="02246-646">Emplacement et autres capteurs</span><span class="sxs-lookup"><span data-stu-id="02246-646">Location and Other Sensors</span></span>        | <span data-ttu-id="02246-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="02246-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span></span> | <span data-ttu-id="02246-648">Correspond à [Microsoft. LocationSettings](#infrared) à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02246-648">Maps to [Microsoft.LocationSettings](#infrared) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="02246-649">Microsoft. PenAndInputDevices</span><span class="sxs-lookup"><span data-stu-id="02246-649">Microsoft.PenAndInputDevices</span></span>                                | <span data-ttu-id="02246-650">Stylet et périphériques d’entrée</span><span class="sxs-lookup"><span data-stu-id="02246-650">Pen and Input Devices</span></span>             | <span data-ttu-id="02246-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="02246-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span> | <span data-ttu-id="02246-652">Correspond à [Microsoft. PenAndTouch](#pen-and-touch) à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-652">Maps to [Microsoft.PenAndTouch](#pen-and-touch) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="02246-653">Microsoft. PeopleNearMe</span><span class="sxs-lookup"><span data-stu-id="02246-653">Microsoft.PeopleNearMe</span></span>                                      | <span data-ttu-id="02246-654">Voisinage immédiat</span><span class="sxs-lookup"><span data-stu-id="02246-654">People Near Me</span></span>                    | <span data-ttu-id="02246-655">{5224F545-A443-4859-BA23-7B5A95BDC8EF}</span><span class="sxs-lookup"><span data-stu-id="02246-655">{5224F545-A443-4859-BA23-7B5A95BDC8EF}</span></span> | <span data-ttu-id="02246-656">Suppression depuis Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02246-656">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="02246-657">Microsoft. PerformanceInformationAndTools</span><span class="sxs-lookup"><span data-stu-id="02246-657">Microsoft.PerformanceInformationAndTools</span></span>                    | <span data-ttu-id="02246-658">Informations et outils de performance</span><span class="sxs-lookup"><span data-stu-id="02246-658">Performance Information and Tools</span></span> | <span data-ttu-id="02246-659">{78F3955E-3B90-4184-BD14-5397C15F1EFC}</span><span class="sxs-lookup"><span data-stu-id="02246-659">{78F3955E-3B90-4184-BD14-5397C15F1EFC}</span></span> | <span data-ttu-id="02246-660">Suppression à partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="02246-660">Removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="02246-661">Microsoft. PhoneAndModemOptions</span><span class="sxs-lookup"><span data-stu-id="02246-661">Microsoft.PhoneAndModemOptions</span></span>                              | <span data-ttu-id="02246-662">Téléphone et modem</span><span class="sxs-lookup"><span data-stu-id="02246-662">Phone and Modem</span></span>                   | <span data-ttu-id="02246-663">{40419485-C444-4567-851A-2DD7BFA1684D}</span><span class="sxs-lookup"><span data-stu-id="02246-663">{40419485-C444-4567-851A-2DD7BFA1684D}</span></span> | <span data-ttu-id="02246-664">Correspond à [Microsoft. PhoneAndModem](#phone-and-modem) à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-664">Maps to [Microsoft.PhoneAndModem](#phone-and-modem) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="02246-665">Microsoft. Printers</span><span class="sxs-lookup"><span data-stu-id="02246-665">Microsoft.Printers</span></span>                                          | <span data-ttu-id="02246-666">Imprimantes</span><span class="sxs-lookup"><span data-stu-id="02246-666">Printers</span></span>                          | <span data-ttu-id="02246-667">{2227A280-3AEA-1069-A2DE-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="02246-667">{2227A280-3AEA-1069-A2DE-08002B30309D}</span></span> | <span data-ttu-id="02246-668">Correspond à [Microsoft. DevicesAndPrinters](#devices-and-printers) à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-668">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="02246-669">Microsoft. ProblemReportsAndSolutions</span><span class="sxs-lookup"><span data-stu-id="02246-669">Microsoft.ProblemReportsAndSolutions</span></span>                        | <span data-ttu-id="02246-670">Rapports et solutions aux problèmes</span><span class="sxs-lookup"><span data-stu-id="02246-670">Problem Reports and Solutions</span></span>     | <span data-ttu-id="02246-671">{FCFEECAE-EE1B-4849-AE50-685DCF7717EC}</span><span class="sxs-lookup"><span data-stu-id="02246-671">{FCFEECAE-EE1B-4849-AE50-685DCF7717EC}</span></span> | <span data-ttu-id="02246-672">Correspond à [Microsoft. ActionCenter](#action-center) à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-672">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="02246-673">Microsoft. RegionalAndLanguageOptions</span><span class="sxs-lookup"><span data-stu-id="02246-673">Microsoft.RegionalAndLanguageOptions</span></span>                        | <span data-ttu-id="02246-674">Options régionales et linguistiques</span><span class="sxs-lookup"><span data-stu-id="02246-674">Regional and Language Options</span></span>     | <span data-ttu-id="02246-675">{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span><span class="sxs-lookup"><span data-stu-id="02246-675">{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span> | <span data-ttu-id="02246-676">Correspond à [Microsoft. RegionAndLanguage](#region) à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-676">Maps to [Microsoft.RegionAndLanguage](#region) as of Windows 7.</span></span> <span data-ttu-id="02246-677">Notez que depuis Windows 8, la région et la langue ont chacune leur propre élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="02246-677">Note that as of Windows 8, Region and Language were each given their own Control Panel item.</span></span> <span data-ttu-id="02246-678">Microsoft. RegionalAndLanguageOptions et Microsoft. RegionAndLanguage ouvrent actuellement l’élément Region.</span><span class="sxs-lookup"><span data-stu-id="02246-678">Both Microsoft.RegionalAndLanguageOptions and Microsoft.RegionAndLanguage currently open the Region item.</span></span> <span data-ttu-id="02246-679">Vous devez utiliser [Microsoft. Language](#location-settings) pour accéder à l’élément de langue.</span><span class="sxs-lookup"><span data-stu-id="02246-679">You must use [Microsoft.Language](#location-settings) to access the Language item.</span></span> |
| <span data-ttu-id="02246-680">Microsoft. SecurityCenter</span><span class="sxs-lookup"><span data-stu-id="02246-680">Microsoft.SecurityCenter</span></span>                                    | <span data-ttu-id="02246-681">Security Center Windows</span><span class="sxs-lookup"><span data-stu-id="02246-681">Windows Security Center</span></span>           | <span data-ttu-id="02246-682">{087DA31B-0DD3-4537-8E23-64A18591F88B}</span><span class="sxs-lookup"><span data-stu-id="02246-682">{087DA31B-0DD3-4537-8E23-64A18591F88B}</span></span> | <span data-ttu-id="02246-683">Correspond à [Microsoft. ActionCenter](#action-center) à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-683">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="02246-684">Microsoft. SpeechRecognitionOptions</span><span class="sxs-lookup"><span data-stu-id="02246-684">Microsoft.SpeechRecognitionOptions</span></span>                          | <span data-ttu-id="02246-685">Options de reconnaissance vocale</span><span class="sxs-lookup"><span data-stu-id="02246-685">Speech Recognition Options</span></span>        | <span data-ttu-id="02246-686">{58E3C745-D971-4081-9034-86E34B30836A}</span><span class="sxs-lookup"><span data-stu-id="02246-686">{58E3C745-D971-4081-9034-86E34B30836A}</span></span> | <span data-ttu-id="02246-687">Correspond à [Microsoft. SpeechRecognition](#speech-recognition) à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-687">Maps to [Microsoft.SpeechRecognition](#speech-recognition) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="02246-688">Microsoft. TaskbarAndStartMenu</span><span class="sxs-lookup"><span data-stu-id="02246-688">Microsoft.TaskbarAndStartMenu</span></span>                               | <span data-ttu-id="02246-689">Barre des tâches et menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="02246-689">Taskbar and Start Menu</span></span>            | <span data-ttu-id="02246-690">{0DF44EAA-FF21-4412-828E-260A8728E7F1}</span><span class="sxs-lookup"><span data-stu-id="02246-690">{0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span> | <span data-ttu-id="02246-691">Correspond à [Microsoft. Taskbar](#speech-recognition) à compter de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02246-691">Maps to [Microsoft.Taskbar](#speech-recognition) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="02246-692">Microsoft. WelcomeCenter</span><span class="sxs-lookup"><span data-stu-id="02246-692">Microsoft.WelcomeCenter</span></span>                                     | <span data-ttu-id="02246-693">Centre d’accueil</span><span class="sxs-lookup"><span data-stu-id="02246-693">Welcome Center</span></span>                    | <span data-ttu-id="02246-694">{CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1}</span><span class="sxs-lookup"><span data-stu-id="02246-694">{CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1}</span></span> | <span data-ttu-id="02246-695">Correspond à Microsoft. GettingStarted dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-695">Maps to Microsoft.GettingStarted in Windows 7.</span></span> <span data-ttu-id="02246-696">Ouvre la page d’hébergement du panneau de configuration à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02246-696">Launches the Control Panel home page as of Windows 8.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="02246-697">Microsoft. WindowsSidebarProperties</span><span class="sxs-lookup"><span data-stu-id="02246-697">Microsoft.WindowsSidebarProperties</span></span>                          | <span data-ttu-id="02246-698">Propriétés du volet Windows</span><span class="sxs-lookup"><span data-stu-id="02246-698">Windows Sidebar Properties</span></span>        | <span data-ttu-id="02246-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="02246-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="02246-700">Correspond à Microsoft. DesktopGadgets dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02246-700">Maps to Microsoft.DesktopGadgets in Windows 7.</span></span> <span data-ttu-id="02246-701">Suppression depuis Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02246-701">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="02246-702">Microsoft. WindowsSideShow</span><span class="sxs-lookup"><span data-stu-id="02246-702">Microsoft.WindowsSideShow</span></span>                                   | <span data-ttu-id="02246-703">Windows SideShow</span><span class="sxs-lookup"><span data-stu-id="02246-703">Windows SideShow</span></span>                  | <span data-ttu-id="02246-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span><span class="sxs-lookup"><span data-stu-id="02246-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span></span> | <span data-ttu-id="02246-705">Fonctionnalité déconseillée dans Windows 8, supprimée à partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="02246-705">Feature deprecated in Windows 8, removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a><span data-ttu-id="02246-706">Utilisation de noms canoniques dans les stratégie de groupe locaux</span><span class="sxs-lookup"><span data-stu-id="02246-706">Using Canonical Names in Local Group Policy</span></span>

<span data-ttu-id="02246-707">À compter de Windows 7, vous pouvez utiliser des noms canoniques pour restreindre l’accès aux éléments individuels du panneau de configuration par le biais de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="02246-707">As of Windows 7, you can use canonical names to restrict access to individual Control Panel items through group policy.</span></span> <span data-ttu-id="02246-708">Cette même procédure peut être utilisée dans Windows Vista, mais vous devez utiliser le nom du module au lieu du nom canonique.</span><span class="sxs-lookup"><span data-stu-id="02246-708">This same procedure can be used in Windows Vista, but you have to use the module name instead of the canonical name.</span></span>

### <a name="hiding-individual-control-panel-items"></a><span data-ttu-id="02246-709">Masquage d’éléments individuels du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="02246-709">Hiding individual Control Panel items</span></span>

<span data-ttu-id="02246-710">Utilisez cette méthode si vous souhaitez afficher plus d’éléments du panneau de configuration que vous ne souhaitez masquer.</span><span class="sxs-lookup"><span data-stu-id="02246-710">Use this method if you want to show more Control Panel items than you want to hide.</span></span>

1.  <span data-ttu-id="02246-711">Exécutez le fichier Gpedit. msc pour lancer l’éditeur de stratégie de groupe local.</span><span class="sxs-lookup"><span data-stu-id="02246-711">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="02246-712">Vous pouvez également taper « stratégie de groupe » sur le Windows 8.1 écran d’accueil et sélectionner **modifier la stratégie de groupe** dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="02246-712">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="02246-713">Sélectionnez **Configuration utilisateur**  >  **modèles d’administration**  >  **le panneau** de configuration.</span><span class="sxs-lookup"><span data-stu-id="02246-713">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="02246-714">Sélectionnez **Masquer les éléments du panneau de configuration spécifiés**.</span><span class="sxs-lookup"><span data-stu-id="02246-714">Select **Hide specified Control Panel items**.</span></span>
4.  <span data-ttu-id="02246-715">Dans la fenêtre **Masquer les éléments du panneau de configuration spécifiés** qui s’ouvre, cliquez sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="02246-715">In the **Hide Specified Control Panel Items** window that opens, click **Enabled**.</span></span>
5.  <span data-ttu-id="02246-716">Cliquez sur le bouton **Afficher** dans le panneau Options pour afficher la liste des éléments du panneau de configuration non autorisés.</span><span class="sxs-lookup"><span data-stu-id="02246-716">Click the **Show** button in the Options panel to show the list of disallowed Control Panel items.</span></span>
6.  <span data-ttu-id="02246-717">Dans la fenêtre **afficher le contenu** qui s’ouvre, tapez un nom canonique dans la colonne **valeur** .</span><span class="sxs-lookup"><span data-stu-id="02246-717">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="02246-718">Répétez cette opération si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="02246-718">Repeat as necessary.</span></span>
7.  <span data-ttu-id="02246-719">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="02246-719">Click **OK**.</span></span>

### <a name="showing-individual-control-panel-items"></a><span data-ttu-id="02246-720">Montrer des éléments du panneau de configuration individuels</span><span class="sxs-lookup"><span data-stu-id="02246-720">Showing individual Control Panel items</span></span>

<span data-ttu-id="02246-721">Utilisez cette méthode si vous souhaitez masquer davantage d’éléments du panneau de configuration que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="02246-721">Use this method if you want to hide more Control Panel items than you want to show.</span></span>

1.  <span data-ttu-id="02246-722">Exécutez le fichier Gpedit. msc pour lancer l’éditeur de stratégie de groupe local.</span><span class="sxs-lookup"><span data-stu-id="02246-722">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="02246-723">Vous pouvez également taper « stratégie de groupe » sur le Windows 8.1 écran d’accueil et sélectionner **modifier la stratégie de groupe** dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="02246-723">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="02246-724">Sélectionnez **Configuration utilisateur**  >  **modèles d’administration**  >  **le panneau** de configuration.</span><span class="sxs-lookup"><span data-stu-id="02246-724">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="02246-725">Sélectionnez **afficher uniquement les éléments du panneau de configuration spécifiés**.</span><span class="sxs-lookup"><span data-stu-id="02246-725">Select **Show only specified Control Panel items**.</span></span>
4.  <span data-ttu-id="02246-726">Dans la fenêtre **afficher uniquement les éléments du panneau de configuration spécifiés** qui s’ouvre, cliquez sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="02246-726">In the **Show Only Specified Control Panel Items** window that opens, click **Enabled**.</span></span> <span data-ttu-id="02246-727">Cela masque tous les éléments du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="02246-727">This hides everything in the Control Panel.</span></span>
5.  <span data-ttu-id="02246-728">Cliquez sur le bouton **Afficher** dans le panneau Options pour afficher la liste des éléments du panneau de configuration autorisés.</span><span class="sxs-lookup"><span data-stu-id="02246-728">Click the **Show** button in the Options panel to show the list of allowed Control Panel items.</span></span>
6.  <span data-ttu-id="02246-729">Dans la fenêtre **afficher le contenu** qui s’ouvre, tapez un nom canonique dans la colonne **valeur** .</span><span class="sxs-lookup"><span data-stu-id="02246-729">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="02246-730">Répétez cette opération si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="02246-730">Repeat as necessary.</span></span>
7.  <span data-ttu-id="02246-731">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="02246-731">Click **OK**.</span></span>

<span data-ttu-id="02246-732">Si vous souhaitez supprimer toutes les entrées que vous avez ajoutées à la liste afficher ou masquer les éléments du panneau de configuration, revenez à l’écran à l’étape 4 et sélectionnez **non configuré** pour effacer la liste.</span><span class="sxs-lookup"><span data-stu-id="02246-732">If you want to remove all of the entries that you've added to a Show or Hide Control Panel items list, return to the screen in step 4 and select **Not Configured** to clear the list.</span></span> <span data-ttu-id="02246-733">Si vous souhaitez conserver vos entrées tout en interrompant les restrictions, sélectionnez **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="02246-733">If you want to retain your entries but suspend the restrictions, select **Disabled**.</span></span>

## <a name="remarks"></a><span data-ttu-id="02246-734">Notes</span><span class="sxs-lookup"><span data-stu-id="02246-734">Remarks</span></span>

<span data-ttu-id="02246-735">Vous pouvez voir des éléments dans votre panneau de configuration qui ne sont pas répertoriés ici.</span><span class="sxs-lookup"><span data-stu-id="02246-735">You might see items in your Control Panel that are not listed here.</span></span> <span data-ttu-id="02246-736">Ces éléments ne font pas partie de Windows, mais sont ajoutés au moment de l’installation de divers logiciels et matériels, comme Microsoft Office ou une carte vidéo.</span><span class="sxs-lookup"><span data-stu-id="02246-736">Those items are not part of Windows, but instead are added during the installation of various software and hardware, such as Microsoft Office or a video card.</span></span> <span data-ttu-id="02246-737">Les éléments du panneau de configuration non-Windows peuvent ou non avoir un nom canonique.</span><span class="sxs-lookup"><span data-stu-id="02246-737">Non-Windows Control Panel items may or may not have a canonical name.</span></span> <span data-ttu-id="02246-738">Pour rechercher le nom canonique d’un élément du panneau de configuration qui n’est pas répertorié ici, consultez le Registre sous ces chemins d’accès :</span><span class="sxs-lookup"><span data-stu-id="02246-738">To find the canonical name of a Control Panel item not listed here, look in the registry under these paths:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

<span data-ttu-id="02246-739">Pour plus d’informations qui peuvent vous aider à découvrir les CLSID nécessaires, consultez [comment inscrire des éléments du panneau de configuration exécutables](how-to-register-an-executable-control-panel-item-registration-.md) et [comment inscrire des éléments du panneau de configuration de la dll](how-to-register-dll-control-panel-item-registration-.md).</span><span class="sxs-lookup"><span data-stu-id="02246-739">For more information that can help you discover the necessary CLSIDs, see [How to Register Executable Control Panel Items](how-to-register-an-executable-control-panel-item-registration-.md) and [How to Register DLL Control Panel Items](how-to-register-dll-control-panel-item-registration-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02246-740">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02246-740">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02246-741">Exécution des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="02246-741">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="02246-742">**IOpenControlPanel**</span><span class="sxs-lookup"><span data-stu-id="02246-742">**IOpenControlPanel**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



