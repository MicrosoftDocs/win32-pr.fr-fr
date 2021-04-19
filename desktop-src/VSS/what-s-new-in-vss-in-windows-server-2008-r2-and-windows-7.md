---
description: Windows Server 2008 R2 et Windows 7 présentent les modifications suivantes apportées au Service VSS.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'Nouveautés : VSS dans Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3677f89517a770a4519369ae11f2eed7e7985414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516666"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a><span data-ttu-id="c963c-103">Nouveautés : VSS dans Windows Server 2008 R2 & Windows 7</span><span class="sxs-lookup"><span data-stu-id="c963c-103">What's New: VSS in Windows Server 2008 R2 & Windows 7</span></span>

<span data-ttu-id="c963c-104">Windows Server 2008 R2 et Windows 7 présentent les modifications suivantes apportées au Service VSS.</span><span class="sxs-lookup"><span data-stu-id="c963c-104">Windows Server 2008 R2 and Windows 7 introduce the following changes to the Volume Shadow Copy Service.</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="c963c-105">Nouvelles interfaces VSS</span><span class="sxs-lookup"><span data-stu-id="c963c-105">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="c963c-106">**IVssBackupComponentsEx3**</span><span class="sxs-lookup"><span data-stu-id="c963c-106">**IVssBackupComponentsEx3**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[<span data-ttu-id="c963c-107">**IVssComponentEx2**</span><span class="sxs-lookup"><span data-stu-id="c963c-107">**IVssComponentEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[<span data-ttu-id="c963c-108">**IVssCreateExpressWriterMetadata**</span><span class="sxs-lookup"><span data-stu-id="c963c-108">**IVssCreateExpressWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[<span data-ttu-id="c963c-109">**IVssExpressWriter**</span><span class="sxs-lookup"><span data-stu-id="c963c-109">**IVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a><span data-ttu-id="c963c-110">Nouvelles classes VSS</span><span class="sxs-lookup"><span data-stu-id="c963c-110">New VSS Classes</span></span>

<dl>

[<span data-ttu-id="c963c-111">**CVssWriterEx2**</span><span class="sxs-lookup"><span data-stu-id="c963c-111">**CVssWriterEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="c963c-112">Nouvelles énumérations VSS</span><span class="sxs-lookup"><span data-stu-id="c963c-112">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="c963c-113">**\_options de récupération VSS \_**</span><span class="sxs-lookup"><span data-stu-id="c963c-113">**VSS\_RECOVERY\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a><span data-ttu-id="c963c-114">Nouvelles fonctions VSS</span><span class="sxs-lookup"><span data-stu-id="c963c-114">New VSS Functions</span></span>

<dl>

[<span data-ttu-id="c963c-115">**CreateVssExpressWriter**</span><span class="sxs-lookup"><span data-stu-id="c963c-115">**CreateVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="c963c-116">Modifications existantes de l’interface VSS</span><span class="sxs-lookup"><span data-stu-id="c963c-116">Existing VSS Interface Modifications</span></span>

<dl>

<span data-ttu-id="c963c-117">Interface [**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)</span><span class="sxs-lookup"><span data-stu-id="c963c-117">[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex) interface</span></span><dl> <span data-ttu-id="c963c-118">Méthode ajoutée : [ **ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span><span class="sxs-lookup"><span data-stu-id="c963c-118">Added method: [**ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span></span>  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="c963c-119">Suivi et journalisation des événements VSS</span><span class="sxs-lookup"><span data-stu-id="c963c-119">VSS Event Tracing and Logging</span></span>

<span data-ttu-id="c963c-120">À compter de Windows Server 2008 R2 et Windows 7, vous pouvez utiliser l’outil VssTrace, l’outil Logman ou l’outil tracelog pour collecter des informations de traçage pour l’infrastructure VSS.</span><span class="sxs-lookup"><span data-stu-id="c963c-120">Beginning with Windows Server 2008 R2 and Windows 7, you can use the VssTrace tool, the Logman tool, or the Tracelog tool to collect tracing information for the VSS infrastructure.</span></span> <span data-ttu-id="c963c-121">Pour plus d’informations, consultez [utilisation des outils de suivi avec VSS](using-tracing-tools-with-vss.md).</span><span class="sxs-lookup"><span data-stu-id="c963c-121">For more information, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="lun-resynchronization"></a><span data-ttu-id="c963c-122">Resynchronisation des LUN</span><span class="sxs-lookup"><span data-stu-id="c963c-122">LUN Resynchronization</span></span>

<span data-ttu-id="c963c-123">Dans Windows Server 2008 R2 et Windows 7, les demandeurs VSS peuvent utiliser une fonctionnalité de fournisseur matériel de clichés instantanés appelée resynchronisation de numéro d’unité logique.</span><span class="sxs-lookup"><span data-stu-id="c963c-123">In Windows Server 2008 R2 and Windows 7, VSS requesters can use a hardware shadow copy provider feature called LUN resynchronization (or "LUN resync").</span></span> <span data-ttu-id="c963c-124">Il s’agit d’un schéma de récupération rapide qui permet à un administrateur d’application de restaurer des données à partir d’un cliché instantané vers le numéro d’unité logique (LUN) d’origine ou vers un nouveau LUN.</span><span class="sxs-lookup"><span data-stu-id="c963c-124">This is a fast-recovery scheme that allows an application administrator to restore data from a shadow copy to the original logical unit number (LUN) or to a new LUN.</span></span> <span data-ttu-id="c963c-125">Le cliché instantané peut être un clone complet ou un cliché instantané différentiel.</span><span class="sxs-lookup"><span data-stu-id="c963c-125">The shadow copy can be a full clone or a differential shadow copy.</span></span> <span data-ttu-id="c963c-126">Dans les deux cas, à la fin de l’opération de resynchronisation, le numéro d’unité logique de destination présente le même contenu que le numéro d’unité logique du cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="c963c-126">In either case, at the end of the resync operation, the destination LUN will have the same contents as the shadow copy LUN.</span></span> <span data-ttu-id="c963c-127">Pendant l’opération de resynchronisation, la baie effectue une copie au niveau du bloc du cliché instantané vers le numéro d’unité logique de destination.</span><span class="sxs-lookup"><span data-stu-id="c963c-127">During the resync operation, the array performs a block-level copy from the shadow copy to the destination LUN.</span></span> <span data-ttu-id="c963c-128">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c963c-128">For more information, see the following:</span></span>

-   [<span data-ttu-id="c963c-129">Resynchronisation des LUN-un scénario de récupération rapide dans le serveur 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c963c-129">LUN Resync - A fast recovery scenario in Server 2008 R2</span></span>](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   <span data-ttu-id="c963c-130">« Utilisation des clichés instantanés » dans [service VSS](/windows-server/storage/file-server/volume-shadow-copy-service)</span><span class="sxs-lookup"><span data-stu-id="c963c-130">"How Shadow Copies Are Used" in [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service)</span></span>
-   [<span data-ttu-id="c963c-131">Pièges courants de resynchronisation des LUN</span><span class="sxs-lookup"><span data-stu-id="c963c-131">Common LUN Resync gotchas</span></span>](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a><span data-ttu-id="c963c-132">Writers Express</span><span class="sxs-lookup"><span data-stu-id="c963c-132">Express Writers</span></span>

<span data-ttu-id="c963c-133">Dans Windows Server 2008 R2 et Windows 7, l’interface VSS Express permet à une application d’enregistrer l’emplacement de ses fichiers de données sans avoir à implémenter un enregistreur VSS.</span><span class="sxs-lookup"><span data-stu-id="c963c-133">In Windows Server 2008 R2 and Windows 7, the VSS express interface allows an application to register the location of its data files without implementing a VSS writer.</span></span> <span data-ttu-id="c963c-134">Pour plus d’informations, consultez [service VSS (VSS) enregistreurs Express](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).</span><span class="sxs-lookup"><span data-stu-id="c963c-134">For more information, see [Volume Shadow Copy Service (VSS) Express Writers](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).</span></span>

## <a name="new-vss-writers"></a><span data-ttu-id="c963c-135">Nouveaux enregistreurs VSS</span><span class="sxs-lookup"><span data-stu-id="c963c-135">New VSS Writers</span></span>

<span data-ttu-id="c963c-136">Windows Server 2008 R2 et Windows 7 présentent les enregistreurs VSS suivants :</span><span class="sxs-lookup"><span data-stu-id="c963c-136">Windows Server 2008 R2 and Windows 7 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="c963c-137">Enregistreur des compteurs de performances</span><span class="sxs-lookup"><span data-stu-id="c963c-137">Performance Counters Writer</span></span>
-   <span data-ttu-id="c963c-138">Rédacteur de Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c963c-138">Task Scheduler Writer</span></span>
-   <span data-ttu-id="c963c-139">Enregistreur du magasin de métadonnées VSS</span><span class="sxs-lookup"><span data-stu-id="c963c-139">VSS Metadata Store Writer</span></span>

<span data-ttu-id="c963c-140">Ces nouveaux enregistreurs sont documentés dans les [enregistreurs VSS](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="c963c-140">These new writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 
