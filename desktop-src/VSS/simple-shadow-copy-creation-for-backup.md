---
description: Plusieurs types de clichés instantanés peuvent être créés par un demandeur.
ms.assetid: a20570ea-e3eb-4d65-b8fa-9a27ce1a3e74
title: Création de clichés instantanés simples pour la sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11e030c0531c96eee40e9cd5bb7cc9366284985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751029"
---
# <a name="simple-shadow-copy-creation-for-backup"></a><span data-ttu-id="a6eeb-103">Création de clichés instantanés simples pour la sauvegarde</span><span class="sxs-lookup"><span data-stu-id="a6eeb-103">Simple Shadow Copy Creation for Backup</span></span>

<span data-ttu-id="a6eeb-104">Plusieurs types de clichés instantanés peuvent être créés par un demandeur.</span><span class="sxs-lookup"><span data-stu-id="a6eeb-104">There are a number of different types of shadow copy a requester can create.</span></span> <span data-ttu-id="a6eeb-105">Toutefois, pour la plupart des applications de sauvegarde, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a6eeb-105">However, for most backup applications, you would do the following:</span></span>

1.  <span data-ttu-id="a6eeb-106">Appelez [**IVssBackupComponents :: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) avec un contexte de sauvegarde Visual SourceSafe \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a6eeb-106">Call [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) with a context of VSS\_CTX\_BACKUP.</span></span>
2.  <span data-ttu-id="a6eeb-107">Appelez [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) pour initialiser la communication avec les enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="a6eeb-107">Call [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) to initialize communication with writers.</span></span>
3.  <span data-ttu-id="a6eeb-108">Appelez [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) pour ajouter des composants de fichiers et de bases de données à la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="a6eeb-108">Call [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to add file and database components to the backup.</span></span>
4.  <span data-ttu-id="a6eeb-109">Appelez [**IVssBackupComponents :: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) pour initialiser le mécanisme de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="a6eeb-109">Call [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) to initialize the shadow copy mechanism.</span></span>
5.  <span data-ttu-id="a6eeb-110">Appelez [**IVssBackupComponents :: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) pour inclure les volumes dans le cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="a6eeb-110">Call [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) to include volumes in the shadow copy.</span></span>
6.  <span data-ttu-id="a6eeb-111">Appelez [**IVssBackupComponents ::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) pour notifier les auteurs des opérations de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="a6eeb-111">Call [**IVssBackupComponents::PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) to notify writers of backup operations.</span></span>

 

 



