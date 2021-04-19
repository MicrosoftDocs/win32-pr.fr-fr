---
title: Utilisation de BITS
description: Utilisation de BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- Service de transfert intelligent en arrière-plan (BITS)
- Service de transfert intelligent en arrière-plan, tâches
- BITS de transfert de fichiers
- Utilisation de bits bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5158e183ef7e7c142a481f1d89e329a9b04f422b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106518031"
---
# <a name="using-bits"></a><span data-ttu-id="d5d13-107">Utilisation de BITS</span><span class="sxs-lookup"><span data-stu-id="d5d13-107">Using BITS</span></span>

<span data-ttu-id="d5d13-108">Les étapes suivantes montrent comment effectuer un transfert de fichiers à l’aide des  [interfaces](bits-interfaces.md)service de transfert intelligent en arrière-plan (bits).</span><span class="sxs-lookup"><span data-stu-id="d5d13-108">The following steps show how to perform a file transfer using the Background Intelligent Transfer Service (BITS)  [interfaces](bits-interfaces.md).</span></span>

<span data-ttu-id="d5d13-109">**Pour effectuer un transfert de fichiers**</span><span class="sxs-lookup"><span data-stu-id="d5d13-109">**To perform a file transfer**</span></span>

1.  [<span data-ttu-id="d5d13-110">Se connecter au service BITS</span><span class="sxs-lookup"><span data-stu-id="d5d13-110">Connect to the BITS service</span></span>](connecting-to-the-bits-service.md)
2.  [<span data-ttu-id="d5d13-111">Créer une tâche de transfert</span><span class="sxs-lookup"><span data-stu-id="d5d13-111">Create a transfer job</span></span>](creating-a-job.md)
3.  [<span data-ttu-id="d5d13-112">Ajouter des fichiers au travail</span><span class="sxs-lookup"><span data-stu-id="d5d13-112">Add files to the job</span></span>](adding-files-to-a-job.md)
4.  [<span data-ttu-id="d5d13-113">Démarrage du travail</span><span class="sxs-lookup"><span data-stu-id="d5d13-113">Start the job</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [<span data-ttu-id="d5d13-114">Déterminer si BITS a transféré les fichiers avec succès</span><span class="sxs-lookup"><span data-stu-id="d5d13-114">Determine if BITS successfully transferred the files</span></span>](determining-the-status-of-a-job.md)
6.  [<span data-ttu-id="d5d13-115">Terminer la tâche</span><span class="sxs-lookup"><span data-stu-id="d5d13-115">Complete the job</span></span>](completing-and-canceling-a-job.md)

<span data-ttu-id="d5d13-116">Les étapes précédentes montrent comment transférer des fichiers à l’aide des valeurs de propriété par défaut pour un travail.</span><span class="sxs-lookup"><span data-stu-id="d5d13-116">The previous steps show how to transfer files using the default property values for a job.</span></span> <span data-ttu-id="d5d13-117">Vous pouvez modifier le comportement par défaut en modifiant une ou plusieurs des valeurs de propriété du travail.</span><span class="sxs-lookup"><span data-stu-id="d5d13-117">You can change the default behavior by changing one or more of the job's property values.</span></span> <span data-ttu-id="d5d13-118">Par exemple, vous pouvez modifier la priorité de traitement du travail par rapport à d’autres travaux de la file d’attente, spécifier votre propre paramètre de proxy et vous inscrire pour recevoir une notification d’événement lorsque le service BITS a transféré les fichiers.</span><span class="sxs-lookup"><span data-stu-id="d5d13-118">For example, you can change the priority that the job is processed relative to other jobs in the queue, specify your own proxy setting, and register to receive event notification when BITS has transferred the files.</span></span> <span data-ttu-id="d5d13-119">Pour plus d’informations, consultez [définition et récupération des propriétés d’un travail](setting-and-retrieving-the-properties-of-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="d5d13-119">For more information, see [Setting and Retrieving the Properties of a Job](setting-and-retrieving-the-properties-of-a-job.md).</span></span>

<span data-ttu-id="d5d13-120">Windows PowerShell fournit un mécanisme simple pour gérer de nombreuses tâches BITS.</span><span class="sxs-lookup"><span data-stu-id="d5d13-120">Windows PowerShell provides a simple mechanism to manage many BITS tasks.</span></span> <span data-ttu-id="d5d13-121">Cette section contient les rubriques suivantes qui montrent comment utiliser les applets de commande Windows PowerShell avec BITS :</span><span class="sxs-lookup"><span data-stu-id="d5d13-121">This section contains the following topics that show how to use Windows PowerShell cmdlets with BITS:</span></span>

-   [<span data-ttu-id="d5d13-122">Utilisation de Windows PowerShell pour créer des tâches de transfert BITS</span><span class="sxs-lookup"><span data-stu-id="d5d13-122">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [<span data-ttu-id="d5d13-123">Utilisation des applets de commande Windows PowerShell WinRM pour gérer les tâches de transfert BITS</span><span class="sxs-lookup"><span data-stu-id="d5d13-123">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [<span data-ttu-id="d5d13-124">Utilisation des applets de commande WMI Windows PowerShell pour gérer BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="d5d13-124">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> <span data-ttu-id="d5d13-125">À compter de Windows 10, version 1607, vous pouvez également exécuter des applets de commande PowerShell et utiliser BITSAdmin ou d’autres applications qui utilisent les [interfaces](bits-interfaces.md) bits à partir d’une ligne de commande à distance PowerShell connectée à un autre ordinateur (physique ou virtuel).</span><span class="sxs-lookup"><span data-stu-id="d5d13-125">Starting with Windows 10, version 1607, you can also run PowerShell Cmdlets and use BITSAdmin or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="d5d13-126">Cette fonctionnalité n’est pas disponible lors de l’utilisation d’une ligne de commande [PowerShell direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) sur un ordinateur virtuel sur la même machine physique, et elle n’est pas disponible lors de l’utilisation des applets de commande WinRM.</span><span class="sxs-lookup"><span data-stu-id="d5d13-126">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>
>
> <span data-ttu-id="d5d13-127">Un travail BITS créé à partir d’une session PowerShell distante s’exécute dans le contexte du compte d’utilisateur de cette session et ne progresse que lorsqu’il y a au moins une session de connexion locale active ou une session PowerShell distante associée à ce compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5d13-127">A BITS Job created from a Remote PowerShell session will run under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="d5d13-128">Pour plus d’informations, consultez [pour gérer les sessions à distance PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="d5d13-128">For more information, see [To manage PowerShell Remote sessions](using-windows-powershell-to-create-bits-transfer-jobs.md).</span></span>

 

<span data-ttu-id="d5d13-129">Cette section contient également les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5d13-129">This section also contains the following topics:</span></span>

-   [<span data-ttu-id="d5d13-130">Meilleures pratiques lors de l’utilisation de BITS</span><span class="sxs-lookup"><span data-stu-id="d5d13-130">Best Practices When Using BITS</span></span>](best-practices-when-using-bits.md)
-   [<span data-ttu-id="d5d13-131">Énumération des travaux dans la file d’attente de transfert</span><span class="sxs-lookup"><span data-stu-id="d5d13-131">Enumerating jobs in the transfer queue</span></span>](enumerating-jobs-in-the-transfer-queue.md)
-   [<span data-ttu-id="d5d13-132">Énumération de fichiers dans un travail</span><span class="sxs-lookup"><span data-stu-id="d5d13-132">Enumerating files in a job</span></span>](enumerating-files-in-a-job.md)
-   [<span data-ttu-id="d5d13-133">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="d5d13-133">Handling errors</span></span>](handling-errors.md)
-   [<span data-ttu-id="d5d13-134">Récupérer la réponse d’une tâche de chargement-réponse</span><span class="sxs-lookup"><span data-stu-id="d5d13-134">Retrieve the reply from an upload-reply job</span></span>](retrieving-the-reply-from-an-upload-reply-job.md)

<span data-ttu-id="d5d13-135">Pour obtenir un exemple de code qui utilise les interfaces BITS, consultez [exemples et outils bits](bits-samples-and-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d5d13-135">For sample code that uses the BITS interfaces, see [BITS Samples and Tools](bits-samples-and-tools.md).</span></span>

 

 