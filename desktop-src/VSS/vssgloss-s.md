---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5979d30f0b88762a2d022a89063ee44bd91a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514617"
---
# <a name="s-volume-shadow-copy-service"></a><span data-ttu-id="ce69f-103">S (Service VSS)</span><span class="sxs-lookup"><span data-stu-id="ce69f-103">S (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="ce69f-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="ce69f-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="ce69f-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**sélectivité pour la sauvegarde**</span><span class="sxs-lookup"><span data-stu-id="ce69f-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selectability for backup**</span></span>
</dt> <dd>

<span data-ttu-id="ce69f-106">Un composant est dit sélectionnable pour la sauvegarde si son inclusion explicite dans une opération de sauvegarde est facultative.</span><span class="sxs-lookup"><span data-stu-id="ce69f-106">A component is said to be selectable for backup if its explicit inclusion in a backup operation is optional.</span></span> <span data-ttu-id="ce69f-107">La sélection de la sauvegarde est activée si la valeur du membre **bSelectable** de la structure [**VSS \_ COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) est **true**.</span><span class="sxs-lookup"><span data-stu-id="ce69f-107">Selectability for backup is enabled if the value of the **bSelectable** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="ce69f-108">Il n’existe pas de valeur par défaut pour la sélection d’un composant pour la sauvegarde ; un enregistreur doit toujours définir cette valeur explicitement.</span><span class="sxs-lookup"><span data-stu-id="ce69f-108">There is no default value for a component's selectability for backup; a writer must always set this value explicitly.</span></span>

<span data-ttu-id="ce69f-109">Les enregistreurs utilisent également la sélectivité pour la restauration afin d’organiser la participation de leurs composants aux opérations de restauration.</span><span class="sxs-lookup"><span data-stu-id="ce69f-109">Writers also use selectability for restore to organize their component's participation in restore operations.</span></span>

<span data-ttu-id="ce69f-110">Voir aussi *composant sélectionnable*, *sélectivité pour la restauration*, [*inclusion de composant explicite*](vssgloss-e.md), [*inclusion de composant implicite*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="ce69f-110">See also *selectable component*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce69f-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**sélectivité pour la restauration**</span><span class="sxs-lookup"><span data-stu-id="ce69f-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selectability for restore**</span></span>
</dt> <dd>

<span data-ttu-id="ce69f-112">Un composant est dit sélectionnable pour la restauration s’il peut être sauvegardé implicitement en tant que partie d’un jeu de composants, puis restauré séparément par la suite sans le reste du jeu de composants.</span><span class="sxs-lookup"><span data-stu-id="ce69f-112">A component is said to be selectable for restore if it can be implicitly backed up as part of a component set, and then later individually restored without the rest of the component set.</span></span> <span data-ttu-id="ce69f-113">La sélection de la restauration est activée si la valeur du membre **bSelectableForRestore** de la structure [**VSS \_ COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) est **true**.</span><span class="sxs-lookup"><span data-stu-id="ce69f-113">Selectability for restore is enabled if the value of the **bSelectableForRestore** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="ce69f-114">Par défaut, la sélection d’un composant pour la restauration est **false**.</span><span class="sxs-lookup"><span data-stu-id="ce69f-114">By default, a component's selectability for restore is **false**.</span></span> <span data-ttu-id="ce69f-115">La sélectivité pour la restauration n’a de sens que lorsqu’un composant n’a pas été ajouté au document de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="ce69f-115">Selectability for restore has meaning only when a component has not been added to the backup document.</span></span>

<span data-ttu-id="ce69f-116">Voir aussi *composant sélectionnable*, *sélectivité pour la sauvegarde*, [*inclusion de composant explicite*](vssgloss-e.md), [*inclusion de composant implicite*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="ce69f-116">See also *selectable component*, *selectability for backup*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce69f-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**composant sélectionnable**</span><span class="sxs-lookup"><span data-stu-id="ce69f-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**selectable component**</span></span>
</dt> <dd>

<span data-ttu-id="ce69f-118">Un composant est dit sélectionnable si son inclusion explicite dans une opération de sauvegarde ou de restauration est facultative.</span><span class="sxs-lookup"><span data-stu-id="ce69f-118">A component is said to be selectable if its explicit inclusion in a backup or restore operation is optional.</span></span>

<span data-ttu-id="ce69f-119">La sélection de la sauvegarde et de la sélectivité pour la restauration est indépendante les unes des autres. un composant peut être sélectionnable pour les deux opérations, pour la restauration et non pour la sauvegarde, ou pour la sauvegarde et non pour la restauration.</span><span class="sxs-lookup"><span data-stu-id="ce69f-119">Selectability for backup and selectability for restore are independent of each other—a component may be selectable for both operations, for restore and not backup, or for backup and not restore.</span></span>

<span data-ttu-id="ce69f-120">Les enregistreurs utilisent également la sélectivité pour organiser leurs composants en groupes :</span><span class="sxs-lookup"><span data-stu-id="ce69f-120">Writers also use selectability to organize their components into groups:</span></span>

-   <span data-ttu-id="ce69f-121">Les composants non sélectionnables sans ancêtres sélectionnables dans leurs chemins logiques doivent toujours être explicitement inclus si un enregistreur doit être sauvegardé ou restauré.</span><span class="sxs-lookup"><span data-stu-id="ce69f-121">Nonselectable components with no selectable ancestors in their logical paths must always be explicitly included if a writer is to be backed up or restored.</span></span>
-   <span data-ttu-id="ce69f-122">Les composants non sélectionnables avec des ancêtres sélectionnables seront inclus dans une sauvegarde ou une restauration uniquement si au moins un ancêtre sélectionnable est inclus.</span><span class="sxs-lookup"><span data-stu-id="ce69f-122">Nonselectable components with selectable ancestors will only be included in a backup or restore if at least one selectable ancestor is included.</span></span>
-   <span data-ttu-id="ce69f-123">Les composants sélectionnables sans ancêtres sélectionnables ne peuvent être inclus que dans une opération de sauvegarde ou de restauration.</span><span class="sxs-lookup"><span data-stu-id="ce69f-123">Selectable components without selectable ancestors can only be included in a backup or restore operation explicitly.</span></span>
-   <span data-ttu-id="ce69f-124">Les composants sélectionnables avec des ancêtres sélectionnables peuvent être explicitement inclus dans une opération de sauvegarde ou de restauration, ou peuvent être implicitement inclus si l’un de leurs ancêtres sélectionnables est inclus.</span><span class="sxs-lookup"><span data-stu-id="ce69f-124">Selectable components with selectable ancestors can be explicitly included in a backup or restore operation, or can be implicitly included if one of their selectable ancestors is included.</span></span>

<span data-ttu-id="ce69f-125">Voir aussi [*composants*](vssgloss-c.md), *sélection pour la sauvegarde*, *sélectivité pour la restauration*, [*inclusion de composant explicite*](vssgloss-e.md), [*inclusion de composant implicite*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="ce69f-125">See also [*components*](vssgloss-c.md), *selectability for backup*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce69f-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**cliché instantané**</span><span class="sxs-lookup"><span data-stu-id="ce69f-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="ce69f-127">Réplica à un point dans le temps en lecture seule du contenu d’un volume d’origine.</span><span class="sxs-lookup"><span data-stu-id="ce69f-127">A read-only point-in-time replica of an original volume's contents.</span></span> <span data-ttu-id="ce69f-128">Chaque cliché instantané est indexé par un GUID persistant.</span><span class="sxs-lookup"><span data-stu-id="ce69f-128">Each shadow copy is keyed by a persistent GUID.</span></span> <span data-ttu-id="ce69f-129">Également appelé cliché instantané du volume.</span><span class="sxs-lookup"><span data-stu-id="ce69f-129">Also called a volume shadow copy.</span></span> <span data-ttu-id="ce69f-130">Voir aussi *jeu de clichés instantanés*.</span><span class="sxs-lookup"><span data-stu-id="ce69f-130">See also *shadow copy set*.</span></span>

</dd> <dt>

<span data-ttu-id="ce69f-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**clichés instantanés pour dossiers partagés**</span><span class="sxs-lookup"><span data-stu-id="ce69f-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Shadow Copies for Shared Folders**</span></span>
</dt> <dd>

<span data-ttu-id="ce69f-132">Fonctionnalité de Windows qui crée des copies de sauvegarde en ligne légères de volumes à l’aide de VSS.</span><span class="sxs-lookup"><span data-stu-id="ce69f-132">A feature of Windows that creates lightweight, online backup copies of volumes using VSS.</span></span> <span data-ttu-id="ce69f-133">Les clients peuvent accéder à ces sauvegardes via le shell Windows pour voir les anciennes versions des fichiers et annuler des erreurs sans nécessiter une restauration complète.</span><span class="sxs-lookup"><span data-stu-id="ce69f-133">Clients can access these backups through the Windows shell to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="ce69f-134">Voir aussi cliché [*instantané accessible*](vssgloss-c.md)par le client.</span><span class="sxs-lookup"><span data-stu-id="ce69f-134">See also [*client accessible shadow copy*](vssgloss-c.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce69f-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**jeu de clichés instantanés**</span><span class="sxs-lookup"><span data-stu-id="ce69f-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**shadow copy set**</span></span>
</dt> <dd>

<span data-ttu-id="ce69f-136">Collection de clichés instantanés de volume créés en même temps et identifiées par un ID de jeu de clichés instantanés commun (valeur GUID persistant).</span><span class="sxs-lookup"><span data-stu-id="ce69f-136">A collection of volume shadow copies created at the same time and identified by a common shadow copy set ID (a persistent GUID) value.</span></span> <span data-ttu-id="ce69f-137">Il s’agit du mécanisme utilisé pour permettre la gestion d’une opération de cliché instantané sur plusieurs volumes.</span><span class="sxs-lookup"><span data-stu-id="ce69f-137">This is the mechanism used to allow a shadow copy operation to be managed across volumes.</span></span> <span data-ttu-id="ce69f-138">Voir aussi cliché *instantané*.</span><span class="sxs-lookup"><span data-stu-id="ce69f-138">See also *shadow copy*.</span></span>

</dd> <dt>

<span data-ttu-id="ce69f-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**fournisseur de logiciels**</span><span class="sxs-lookup"><span data-stu-id="ce69f-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="ce69f-140">Fournisseur qui intercepte les demandes d’e/s au niveau du logiciel entre le système de fichiers et le gestionnaire de volume.</span><span class="sxs-lookup"><span data-stu-id="ce69f-140">A provider that intercepts I/O requests at the software level between the file system and the volume manager.</span></span> <span data-ttu-id="ce69f-141">Voir aussi [*fournisseur de matériel*](vssgloss-h.md), [*fournisseur*](vssgloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="ce69f-141">See also [*hardware provider*](vssgloss-h.md), [*provider*](vssgloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce69f-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**sous-composant**</span><span class="sxs-lookup"><span data-stu-id="ce69f-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**subcomponent**</span></span>
</dt> <dd>

<span data-ttu-id="ce69f-143">Tout composant qui possède un chemin d’accès logique contenant un élément sélectionnable (pour la sauvegarde ou la restauration) du composant parent.</span><span class="sxs-lookup"><span data-stu-id="ce69f-143">Any component that has a logical path containing a selectable (for either backup or restore) parent component.</span></span> <span data-ttu-id="ce69f-144">Les sous-composants doivent avoir un chemin d’accès logique au format {nom du composant \_ } {nom du sous- \\ composant \_ }.</span><span class="sxs-lookup"><span data-stu-id="ce69f-144">Subcomponents must have a logical path of the form {component\_name}\\{subcomponent\_name}.</span></span> <span data-ttu-id="ce69f-145">Si l’ancêtre d’un sous-composant (pour la sauvegarde ou la restauration) est explicitement inclus dans une sauvegarde ou une restauration, le sous-composant est implicitement inclus dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="ce69f-145">If a subcomponent's selectable (for either backup or restore) ancestor is explicitly included in a backup or restore, then the subcomponent is implicitly included in the operation.</span></span> <span data-ttu-id="ce69f-146">Les sous-composants inclus implicitement n’ont pas leurs données incluses dans le document des composants de sauvegarde, qu’ils soient sélectionnables (pour la restauration ou la sauvegarde) ou non.</span><span class="sxs-lookup"><span data-stu-id="ce69f-146">Implicitly included subcomponents do not have their data included in the Backup Components Document—regardless of whether they are selectable (for either restore or backup) or not.</span></span> <span data-ttu-id="ce69f-147">Voir aussi [*composant*](vssgloss-c.md), [*chemin logique*](vssgloss-l.md).</span><span class="sxs-lookup"><span data-stu-id="ce69f-147">See also [*component*](vssgloss-c.md), [*logical path*](vssgloss-l.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce69f-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**clichés instantanés en surface**</span><span class="sxs-lookup"><span data-stu-id="ce69f-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**surfaced shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="ce69f-149">Volume de clichés instantanés visible pour l’espace de noms du gestionnaire de montage d’un système, ce qui signifie que **FindFirstVolume** et **FindNextVolume** peuvent le trouver et que les notifications d’arrivée et de départ du volume sont générées.</span><span class="sxs-lookup"><span data-stu-id="ce69f-149">A shadow copied volume visible to a system's Mount Manager namespace—meaning **FindFirstVolume** and **FindNextVolume** can find it and that volume arrival and departure notifications are generated.</span></span> <span data-ttu-id="ce69f-150">Tous les clichés instantanés exposés sont également des clichés instantanés en surface.</span><span class="sxs-lookup"><span data-stu-id="ce69f-150">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="ce69f-151">Toutefois, un cliché instantané superficiel n’a pas besoin d’être exposé.</span><span class="sxs-lookup"><span data-stu-id="ce69f-151">However, a surfaced shadow copy need not be exposed.</span></span> <span data-ttu-id="ce69f-152">Si un cliché instantané est transportable, il ne peut pas être exposé.</span><span class="sxs-lookup"><span data-stu-id="ce69f-152">If a shadow copy is transportable, it cannot be surfaced.</span></span> <span data-ttu-id="ce69f-153">Voir aussi cliché [*instantané exposé*](vssgloss-e.md), cliché [*instantané transportable*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="ce69f-153">See also [*exposed shadow copy*](vssgloss-e.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce69f-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**Protection des fichiers système**</span><span class="sxs-lookup"><span data-stu-id="ce69f-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**System File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="ce69f-155">Voir [*protection des fichiers Windows*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="ce69f-155">See [*Windows File Protection*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce69f-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**applications au niveau système**</span><span class="sxs-lookup"><span data-stu-id="ce69f-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**system-level applications**</span></span>
</dt> <dd>

<span data-ttu-id="ce69f-157">Indique le point auquel le service VSS notifie un enregistreur d’un gel.</span><span class="sxs-lookup"><span data-stu-id="ce69f-157">Indicates the point at which VSS notifies a writer of a freeze.</span></span> <span data-ttu-id="ce69f-158">Les enregistreurs qui sont initialisés en tant qu’applications au niveau du système sont avertis après que les rédacteurs ont été initialisés en tant qu’applications de niveau frontal ou en tant qu’applications de niveau principal.</span><span class="sxs-lookup"><span data-stu-id="ce69f-158">Writers that are initialized as system-level applications are notified after writers initialized either as front-end level applications or as back-end level applications.</span></span> <span data-ttu-id="ce69f-159">Consultez également [*niveau application*](vssgloss-a.md), [*applications de niveau*](vssgloss-b.md)principal, [*applications de niveau frontal*](vssgloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="ce69f-159">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*front-end level applications*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce69f-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**fournisseur système**</span><span class="sxs-lookup"><span data-stu-id="ce69f-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**system provider**</span></span>
</dt> <dd>

<span data-ttu-id="ce69f-161">Fournisseur préinstallé par défaut fourni dans le cadre de Windows.</span><span class="sxs-lookup"><span data-stu-id="ce69f-161">The default preinstalled provider provided as part of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ce69f-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Dossier du volume système**</span><span class="sxs-lookup"><span data-stu-id="ce69f-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**System Volume Folder**</span></span>
</dt> <dd>

<span data-ttu-id="ce69f-163">Répertoire partagé qui stocke les copies partagées des fichiers publics d’un domaine, c’est-à-dire les fichiers répliqués sur tous les contrôleurs de domaine du domaine.</span><span class="sxs-lookup"><span data-stu-id="ce69f-163">A shared directory that stores the shared copies of a domain's public files—that is, those files that are replicated among all domain controllers in the domain.</span></span>

</dd> </dl>

 

 



