---
description: Les options de restauration permettent aux demandeurs de communiquer des options de restauration personnalisées aux enregistreurs.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Définition des options de restauration VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c814ffb94f25229e7f3e17f592c631f13b6717e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529153"
---
# <a name="setting-vss-restore-options"></a><span data-ttu-id="69e4c-103">Définition des options de restauration VSS</span><span class="sxs-lookup"><span data-stu-id="69e4c-103">Setting VSS Restore Options</span></span>

<span data-ttu-id="69e4c-104">Les options de restauration permettent aux demandeurs de communiquer des options de restauration personnalisées aux enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="69e4c-104">Restore options allow requesters to communicate customized restore options to writers.</span></span>

## <a name="restore-options"></a><span data-ttu-id="69e4c-105">Options de restauration</span><span class="sxs-lookup"><span data-stu-id="69e4c-105">Restore Options</span></span>

<span data-ttu-id="69e4c-106">La standardisation du format des options de restauration permet aux rédacteurs et aux demandeurs de gérer les demandes personnalisées courantes.</span><span class="sxs-lookup"><span data-stu-id="69e4c-106">Standardizing the format of the restore options allow writers and requesters to handle common custom requests.</span></span> <span data-ttu-id="69e4c-107">Les options de restauration sont définies par le demandeur en appelant la méthode [**IVssBackupComponents :: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) jusqu’à une fois par composant sélectionné pour la sauvegarde avant d’appeler la méthode [**IVssBackupComponents ::P Restore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .</span><span class="sxs-lookup"><span data-stu-id="69e4c-107">Restore options are set by the requester by calling the [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method up to once per selected-for-backup component before calling the [**IVssBackupComponents::PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) method.</span></span> <span data-ttu-id="69e4c-108">La chaîne transmise dans le paramètre *wszRestoreOptions* à la méthode **SetRestoreOptions** peut contenir plusieurs valeurs, comme décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="69e4c-108">The string passed in the *wszRestoreOptions* parameter to the **SetRestoreOptions** method can contain multiple values, as described below.</span></span>

## <a name="format"></a><span data-ttu-id="69e4c-109">Format</span><span class="sxs-lookup"><span data-stu-id="69e4c-109">Format</span></span>

<span data-ttu-id="69e4c-110">Le format des options de restauration est une ou plusieurs paires nom/valeur séparées par des virgules, et le nom est éventuellement préfixé avec le nom du sous-composant auquel il s’applique.</span><span class="sxs-lookup"><span data-stu-id="69e4c-110">The format of restore options, is one or more comma-separated name/value pairs, and the name is optionally prefixed with the name of the subcomponent to which it applies.</span></span> <span data-ttu-id="69e4c-111">Les noms des composants et des options ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="69e4c-111">The component names and option names are case-insensitive.</span></span> <span data-ttu-id="69e4c-112">Le respect de la casse des valeurs est déterminé par le writer.</span><span class="sxs-lookup"><span data-stu-id="69e4c-112">The case-sensitivity of the values is determined by the writer.</span></span> <span data-ttu-id="69e4c-113">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="69e4c-113">For example:</span></span>

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

<span data-ttu-id="69e4c-114">Dans cet exemple, « option1 » s’applique uniquement au sous-composant « child1 » et à ses descendants, « option2 » s’applique à tous les composants et à leurs descendants, et « option3 » s’applique uniquement aux sous-composants « enfant2 \\ Grandchild3 » et à ses descendants.</span><span class="sxs-lookup"><span data-stu-id="69e4c-114">In this example, "Option1" only applies to the "Child1" subcomponent and its descendants, "Option2" applies to all components and their descendants, and "Option3" applies only to the "Child2\\Grandchild3" subcomponents and its descendants.</span></span>

<span data-ttu-id="69e4c-115">La méthode [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) peut uniquement être appelée sur des composants sélectionnables pour la sauvegarde, alors que les nœuds descendants ne peuvent pas être sélectionnables pour la sauvegarde, ils peuvent être sélectionnables pour la restauration.</span><span class="sxs-lookup"><span data-stu-id="69e4c-115">The [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method can only be called on components that are selectable for backup, while descendant nodes may not be selectable for backup, they may be selectable for restore.</span></span>

## <a name="common-restore-options"></a><span data-ttu-id="69e4c-116">Options de restauration courantes</span><span class="sxs-lookup"><span data-stu-id="69e4c-116">Common Restore Options</span></span>

<span data-ttu-id="69e4c-117">Ces options de restauration courantes ont été définies pour améliorer l’interopérabilité entre les enregistreurs et les demandeurs.</span><span class="sxs-lookup"><span data-stu-id="69e4c-117">These common restore options have been defined to increase interoperability between writers and requesters.</span></span>

-   <span data-ttu-id="69e4c-118">Manière</span><span class="sxs-lookup"><span data-stu-id="69e4c-118">Authoritative</span></span>

    <span data-ttu-id="69e4c-119">L’option « authoritative » prend en charge plusieurs valeurs « Item », mais une seule valeur « All ».</span><span class="sxs-lookup"><span data-stu-id="69e4c-119">The "Authoritative" option supports multiple "Item" values, but only one "All" value.</span></span>

    <span data-ttu-id="69e4c-120">Ce composant entier fait autorité.</span><span class="sxs-lookup"><span data-stu-id="69e4c-120">This entire component is authoritative.</span></span>

    ``` syntax
    "Authoritative"="All"
    ```

    <span data-ttu-id="69e4c-121">Seul l’élément spécifié fait autorité.</span><span class="sxs-lookup"><span data-stu-id="69e4c-121">Only the specified item is authoritative.</span></span> <span data-ttu-id="69e4c-122">Le format de l’élément nommé est défini par le writer.</span><span class="sxs-lookup"><span data-stu-id="69e4c-122">The format of the named item is defined by the writer.</span></span> <span data-ttu-id="69e4c-123">Les désignations courantes sont « \* » pour indiquer tous les fichiers, « ... » pour indiquer tous les fichiers et sous-répertoires du composant spécifié.</span><span class="sxs-lookup"><span data-stu-id="69e4c-123">Common designations are "\*" to indicate all files, "..." to indicate all files and subdirectories of the specified component.</span></span>

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   <span data-ttu-id="69e4c-124">Restaurer par progression</span><span class="sxs-lookup"><span data-stu-id="69e4c-124">Roll Forward</span></span>

    <span data-ttu-id="69e4c-125">Après la restauration d’une base de données, les rédacteurs restaurent généralement les journaux pour mettre à jour la base de données.</span><span class="sxs-lookup"><span data-stu-id="69e4c-125">After a database is restored, writers usually roll forward through logs to bring the database up to date.</span></span> <span data-ttu-id="69e4c-126">En cas de restaurations incrémentielles ou différentielles, le demandeur utilise la méthode [**IVssBackupComponents :: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) pour contrôler partiellement le comportement de gestion des journaux : cette option de restauration permet un contrôle plus granulaire.</span><span class="sxs-lookup"><span data-stu-id="69e4c-126">In the case of incremental or differential restores, the requester uses the [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) method to partially control the log-handling behavior - this restore option allows more granular control.</span></span>

    <span data-ttu-id="69e4c-127">Ne pas restaurer les journaux.</span><span class="sxs-lookup"><span data-stu-id="69e4c-127">Do not roll through logs.</span></span>

    ``` syntax
    "Roll Forward"="None"
    ```

    <span data-ttu-id="69e4c-128">Parcourez tous les journaux.</span><span class="sxs-lookup"><span data-stu-id="69e4c-128">Roll through all logs.</span></span>

    ``` syntax
    "Roll Forward"="All"
    ```

    <span data-ttu-id="69e4c-129">Restaure les journaux jusqu’au point spécifié.</span><span class="sxs-lookup"><span data-stu-id="69e4c-129">Roll through logs up to specified point.</span></span> <span data-ttu-id="69e4c-130">Le format du point spécifié est défini par le writer.</span><span class="sxs-lookup"><span data-stu-id="69e4c-130">The format of the specified point is defined by the writer.</span></span>

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   <span data-ttu-id="69e4c-131">Nouveau nom du composant</span><span class="sxs-lookup"><span data-stu-id="69e4c-131">New Component Name</span></span>

    <span data-ttu-id="69e4c-132">Un enregistreur peut vouloir restaurer un nouveau nom d’un composant.</span><span class="sxs-lookup"><span data-stu-id="69e4c-132">A writer may want to restore a component to a new name.</span></span> <span data-ttu-id="69e4c-133">Par exemple, la restauration d’une base de données avec un nom différent pour restaurer un élément individuel ; Si vous restaurez le même nom, toutes les données nous recommandons que les rédacteurs acceptent un chemin logique et un nom de composant valides comme valeur.</span><span class="sxs-lookup"><span data-stu-id="69e4c-133">For example, restoring a database to a different name to restore an individual item; restoring to the same name would please all data We recommend that writers accept a valid logical path and component name as this options' value.</span></span> <span data-ttu-id="69e4c-134">Ce sera souvent utilisé avec une [*cible dirigée*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="69e4c-134">This will often be used with a [*directed target*](vssgloss-d.md).</span></span>

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



