---
description: 'La liste suivante indique les ajouts et les modifications apportées à l’interface Service VSS dans Windows Server 2003 avec Service Pack 1 (SP1) :'
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: Nouveautés de VSS dans Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559b51d5b019d9d57aa154c4728ef5c8f4bb19d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485017"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a><span data-ttu-id="edc66-103">Nouveautés de VSS dans Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="edc66-103">What's New in VSS in Windows Server 2003 SP1</span></span>

<span data-ttu-id="edc66-104">La liste suivante indique les ajouts et les modifications apportées à l’interface Service VSS dans Windows Server 2003 avec Service Pack 1 (SP1) :</span><span class="sxs-lookup"><span data-stu-id="edc66-104">The following list indicates additions and changes to the Volume Shadow Copy Service interface in Windows Server 2003 with Service Pack 1 (SP1):</span></span>

## <a name="auto-recovery"></a><span data-ttu-id="edc66-105">Récupération automatique</span><span class="sxs-lookup"><span data-stu-id="edc66-105">Auto-recovery</span></span>

<span data-ttu-id="edc66-106">La [*récupération automatique*](vssgloss-a.md) permet aux rédacteurs de mettre à jour les composants d’un cliché instantané avant que le cliché instantané ne soit définitivement modifié en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="edc66-106">[*Auto-recovery*](vssgloss-a.md) allows writers a time to update components in a shadow copy before the shadow copy is permanently changed to read-only.</span></span> <span data-ttu-id="edc66-107">Par exemple, une base de données peut avoir besoin de restaurer toutes les transactions incomplètes pour tous les clichés instantanés (l’enregistreur de base de données définit l’indicateur de **\_ \_ \_ récupération de sauvegarde CF VSS** pour les composants de base de données).</span><span class="sxs-lookup"><span data-stu-id="edc66-107">For example, a database may need to rollback any incomplete transactions for all shadow copies (the database writer would set the **VSS\_CF\_BACKUP\_RECOVERY** flag for the database components).</span></span> <span data-ttu-id="edc66-108">La récupération automatique lancée par le demandeur autorise à la fois une restauration affinée (par exemple, la restauration d’une table dans une base de données ou un dossier sur un serveur de messagerie) ou la restauration pour prendre en charge l’exploration de données pour effectuer une analyse trop **lente pour un serveur \_ \_ \_ \_** de production La récupération automatique n’est pas compatible avec les clichés instantanés transportables, mais la même fonctionnalité est prise en charge à l’aide de la [récupération rapide à l’aide de volumes de clichés instantanés transportables](fast-recovery-using-transportable-shadow-copied-volumes.md).</span><span class="sxs-lookup"><span data-stu-id="edc66-108">Auto-recovery initiated by the requester allows both fine-grained restore (for example restoring one table in a database or one folder on a mail server), or the rollback to support data mining to perform analysis that would be too slow for a production server (the requester would add **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** to the shadow copy context.) Auto-recovery is not compatible with transportable shadow copies, but the same functionality is supported by using [Fast Recovery Using Transportable Shadow Copied Volumes](fast-recovery-using-transportable-shadow-copied-volumes.md).</span></span>

<span data-ttu-id="edc66-109">Les éléments de programmation suivants ont des modifications pour prendre en charge la récupération automatique :</span><span class="sxs-lookup"><span data-stu-id="edc66-109">The following programming elements have changes to support auto-recovery:</span></span>

<span data-ttu-id="edc66-110">Méthodes de classe</span><span class="sxs-lookup"><span data-stu-id="edc66-110">Class methods</span></span>

-   [<span data-ttu-id="edc66-111">**CVssWriter::GetSnapshotDeviceName**</span><span class="sxs-lookup"><span data-stu-id="edc66-111">**CVssWriter::GetSnapshotDeviceName**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [<span data-ttu-id="edc66-112">**CVssWriter::OnPostSnapshot**</span><span class="sxs-lookup"><span data-stu-id="edc66-112">**CVssWriter::OnPostSnapshot**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

<span data-ttu-id="edc66-113">Énumérations</span><span class="sxs-lookup"><span data-stu-id="edc66-113">Enumerations</span></span>

-   [<span data-ttu-id="edc66-114">**\_indicateurs du composant VSS \_**</span><span class="sxs-lookup"><span data-stu-id="edc66-114">**VSS\_COMPONENT\_FLAGS**</span></span>](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [<span data-ttu-id="edc66-115">**\_attributs de l' \_ instantané du volume VSS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="edc66-115">**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

<span data-ttu-id="edc66-116">Méthodes d’interface</span><span class="sxs-lookup"><span data-stu-id="edc66-116">Interface methods</span></span>

-   [<span data-ttu-id="edc66-117">**IVssProviderCreateSnapshotSet ::P reFinalCommitSnapshots**</span><span class="sxs-lookup"><span data-stu-id="edc66-117">**IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [<span data-ttu-id="edc66-118">**IVssProviderCreateSnapshotSet ::P ostFinalCommitSnapshots**</span><span class="sxs-lookup"><span data-stu-id="edc66-118">**IVssProviderCreateSnapshotSet::PostFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a><span data-ttu-id="edc66-119">Prise en charge complète des clichés instantanés transportables</span><span class="sxs-lookup"><span data-stu-id="edc66-119">Full Support for Transportable Shadow Copies</span></span>

<span data-ttu-id="edc66-120">Les clichés instantanés transportables sont pris en charge dans toutes les éditions de Windows Server 2003 avec SP1.</span><span class="sxs-lookup"><span data-stu-id="edc66-120">Transportable shadow copies are supported in all editions of Windows Server 2003 with SP1.</span></span> <span data-ttu-id="edc66-121">Pour plus d’informations, consultez [importation de volumes clichés instantanés transportables](importing-transportable-shadow-copied-volumes.md).</span><span class="sxs-lookup"><span data-stu-id="edc66-121">For more information, see [Importing Transportable Shadow Copied Volumes](importing-transportable-shadow-copied-volumes.md).</span></span>

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="edc66-122">Récupération rapide à l’aide de volumes de clichés instantanés transportables</span><span class="sxs-lookup"><span data-stu-id="edc66-122">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

[<span data-ttu-id="edc66-123">Récupération rapide à l’aide de volumes de clichés instantanés transportables</span><span class="sxs-lookup"><span data-stu-id="edc66-123">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a><span data-ttu-id="edc66-124">Gestion de la zone de stockage des clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="edc66-124">Shadow copy storage area management</span></span>

[<span data-ttu-id="edc66-125">**IVssSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="edc66-125">**IVssSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



