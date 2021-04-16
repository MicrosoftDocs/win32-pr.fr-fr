---
description: Les demandeurs contrôlent les fonctionnalités d’un cliché instantané en définissant son contexte. Ce contexte indique si le cliché instantané doit survivre à l’opération en cours, ainsi que le degré de coordination du fournisseur ou du writer.
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: Configurations du contexte de cliché instantané
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb41d0e2604dcf92d27f490175cdcbafd49822c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528696"
---
# <a name="shadow-copy-context-configurations"></a><span data-ttu-id="4dbc6-104">Configurations du contexte de cliché instantané</span><span class="sxs-lookup"><span data-stu-id="4dbc6-104">Shadow Copy Context Configurations</span></span>

<span data-ttu-id="4dbc6-105">Les demandeurs contrôlent les fonctionnalités d’un cliché instantané en définissant son contexte.</span><span class="sxs-lookup"><span data-stu-id="4dbc6-105">Requesters control a shadow copy's features by setting its context.</span></span> <span data-ttu-id="4dbc6-106">Ce contexte indique si le cliché instantané doit survivre à l’opération en cours, ainsi que le degré de coordination du fournisseur ou du writer.</span><span class="sxs-lookup"><span data-stu-id="4dbc6-106">This context indicates whether the shadow copy will survive the current operation, and the degree of writer/provider coordination.</span></span>

## <a name="persistence-and-shadow-copy-context"></a><span data-ttu-id="4dbc6-107">Persistance et contexte de cliché instantané</span><span class="sxs-lookup"><span data-stu-id="4dbc6-107">Persistence and Shadow Copy Context</span></span>

<span data-ttu-id="4dbc6-108">Un cliché instantané peut être [*persistant*](vssgloss-p.md), c’est-à-dire que le cliché instantané n’est pas supprimé à la suite de l’arrêt d’une opération de sauvegarde ou de la libération d’un objet [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .</span><span class="sxs-lookup"><span data-stu-id="4dbc6-108">A shadow copy may be [*persistent*](vssgloss-p.md)—that is, the shadow copy is not deleted following the termination of a backup operation or the release of an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object.</span></span>

<span data-ttu-id="4dbc6-109">Les clichés instantanés persistants requièrent des contextes de [**\_ \_ \_ contexte de capture instantanée**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) VSS du **\_ client VSS CTX \_ \_ accessible**, de la restauration de l' **\_ \_ application \_ Visual SourceSafe** ou de **VSS \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="4dbc6-109">Persistent shadow copies require [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) contexts of **VSS\_CTX\_CLIENT\_ACCESSIBLE**, **VSS\_CTX\_APP\_ROLLBACK**, or **VSS\_CTX\_NAS\_ROLLBACK**.</span></span> <span data-ttu-id="4dbc6-110">Les clichés instantanés persistants ne peuvent être créés que pour les volumes NTFS.</span><span class="sxs-lookup"><span data-stu-id="4dbc6-110">Persistent shadow copies can be made only for NTFS volumes.</span></span>

<span data-ttu-id="4dbc6-111">Les clichés instantanés non persistants sont créés avec des contextes de sauvegarde **VSS \_ CTX \_** ou une **\_ sauvegarde de \_ \_ partage \_ de fichiers CTX VSS**.</span><span class="sxs-lookup"><span data-stu-id="4dbc6-111">Nonpersistent shadow copies are created with contexts of **VSS\_CTX\_BACKUP** or **VSS\_CTX\_FILE\_SHARE\_BACKUP**.</span></span> <span data-ttu-id="4dbc6-112">Les clichés instantanés non persistants peuvent être effectués pour les volumes NTFS et non-NTFS.</span><span class="sxs-lookup"><span data-stu-id="4dbc6-112">Nonpersistent shadow copies can be made for NTFS and non-NTFS volumes.</span></span>

## <a name="writer-participation-and-shadow-copies"></a><span data-ttu-id="4dbc6-113">Participation aux rédacteurs et clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="4dbc6-113">Writer Participation and Shadow Copies</span></span>

<span data-ttu-id="4dbc6-114">Un contexte de cliché instantané peut être classé comme impliquant des enregistreurs ou ne pas impliquer d’enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="4dbc6-114">A shadow copy context can be classified as either involving writers or not involving writers.</span></span>

<span data-ttu-id="4dbc6-115">Les contextes de clichés instantanés qui impliquent des Writers dans leur création sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="4dbc6-115">Shadow copy contexts that involve writers in their creation include:</span></span>

-   <span data-ttu-id="4dbc6-116">**restauration de l’application Visual SourceSafe \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4dbc6-116">**VSS\_CTX\_APP\_ROLLBACK**</span></span>
-   <span data-ttu-id="4dbc6-117">**\_sauvegarde VSS CTX \_**</span><span class="sxs-lookup"><span data-stu-id="4dbc6-117">**VSS\_CTX\_BACKUP**</span></span>
-   <span data-ttu-id="4dbc6-118">**\_ \_ \_ rédacteurs accessibles par le client CTX VSS \_**</span><span class="sxs-lookup"><span data-stu-id="4dbc6-118">**VSS\_CTX\_CLIENT\_ACCESSIBLE\_WRITERS**</span></span>

<span data-ttu-id="4dbc6-119">Ceux qui n’impliquent pas de Writers dans leur création sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="4dbc6-119">Those that do not involve writers in their creation include:</span></span>

-   <span data-ttu-id="4dbc6-120">**\_client CTX \_ VSS \_ accessible**</span><span class="sxs-lookup"><span data-stu-id="4dbc6-120">**VSS\_CTX\_CLIENT\_ACCESSIBLE**</span></span>
-   <span data-ttu-id="4dbc6-121">**\_sauvegarde du \_ partage de fichiers CTX \_ VSS \_**</span><span class="sxs-lookup"><span data-stu-id="4dbc6-121">**VSS\_CTX\_FILE\_SHARE\_BACKUP**</span></span>
-   <span data-ttu-id="4dbc6-122">**\_restauration du \_ NAS \_ CTX VSS**</span><span class="sxs-lookup"><span data-stu-id="4dbc6-122">**VSS\_CTX\_NAS\_ROLLBACK**</span></span>

<span data-ttu-id="4dbc6-123">Un contexte peut être utilisé avec les deux types de clichés instantanés, mais il ne peut pas être utilisé pour créer un cliché instantané :</span><span class="sxs-lookup"><span data-stu-id="4dbc6-123">One context can be used with both types of shadow copies, but cannot be used in creating a shadow copy:</span></span>

-   <span data-ttu-id="4dbc6-124">**VSS \_ CTX \_ tout**</span><span class="sxs-lookup"><span data-stu-id="4dbc6-124">**VSS\_CTX\_ALL**</span></span>

<span data-ttu-id="4dbc6-125">La création d’un cliché instantané avec un contexte de l’utilisation de **VSS \_ CTX \_ All** (à l’aide de [**IVssBackupComponents :: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) et [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4dbc6-125">Creating a shadow copy with a context of **VSS\_CTX\_ALL** (using [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) and [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) is not supported.</span></span>

<span data-ttu-id="4dbc6-126">Les opérations qui prennent en charge un contexte de l' **\_ \_ ensemble de la VSS CTX** sont les opérations d’administration [**IVssBackupComponents :: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents ::D Eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents :: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)et [**IVssBackupComponents :: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).</span><span class="sxs-lookup"><span data-stu-id="4dbc6-126">Operations that support a context of **VSS\_CTX\_ALL** are the administrative operations [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::DeleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset), and [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).</span></span>

## <a name="obtaining-shadow-copy-information"></a><span data-ttu-id="4dbc6-127">Obtention d’informations sur les clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="4dbc6-127">Obtaining Shadow Copy Information</span></span>

<span data-ttu-id="4dbc6-128">Si un demandeur connaît le GUID d’identification d’un cliché instantané (son **\_ ID VSS**), il peut obtenir des informations sur le contexte d’un cliché instantané spécifique (identifié par **son \_ ID VSS**) en décompactant la structure de l' [**\_ \_ instantané VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) renvoyée par un appel à [**IVssBackupComponents :: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span><span class="sxs-lookup"><span data-stu-id="4dbc6-128">If a requester knows the identifying GUID of a shadow copy (its **VSS\_ID**), it can obtain information about the context of a specific shadow copy (identified by its **VSS\_ID**) by unpacking the [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure returned by a call to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="4dbc6-129">Pour obtenir des informations de contexte sur tous les clichés instantanés d’un système, un demandeur examine le membre **\_ lSnapshotAttributes** du membre **obj. Snap** de la structure de l' [**\_ objet VSS \_ prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (qui est une structure de l' [**\_ instantané \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) obtenue à l’aide de [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) pour effectuer une itération au sein de la liste des objets retournés par un appel à [**IVssBackupComponents :: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="4dbc6-129">To obtain context information about all shadow copies on a system, a requester examines the **m\_lSnapshotAttributes** member of the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) structure obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

 

 



