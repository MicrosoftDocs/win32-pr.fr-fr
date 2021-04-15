---
title: Finalisation et annulation d’un travail
description: Pour effectuer une tâche de transfert, appelez la méthode méthode ibackgroundcopyjob Complete.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- BITS du travail de transfert, annulation
- annulation d’un travail BITS
- transférer les BITS du travail, terminer
- achèvement d’un travail BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb5cd6a33cf8cefa8749a1802c922dc80518722
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462075"
---
# <a name="completing-and-canceling-a-job"></a><span data-ttu-id="e7d26-107">Finalisation et annulation d’un travail</span><span class="sxs-lookup"><span data-stu-id="e7d26-107">Completing and Canceling a Job</span></span>

<span data-ttu-id="e7d26-108">Pour effectuer une tâche de transfert, appelez la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="e7d26-108">To complete a transfer job, call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="e7d26-109">Pour les travaux de téléchargement, vous pouvez appeler la méthode **Complete** avant que tous les fichiers du travail aient été transférés (avant que l’état du travail soit \_ État du travail BG \_ \_ transféré).</span><span class="sxs-lookup"><span data-stu-id="e7d26-109">For download jobs, you can call the **Complete** method before all files in the job have been transferred (before the job's state is BG\_JOB\_STATE\_TRANSFERRED).</span></span> <span data-ttu-id="e7d26-110">Seuls les fichiers qui ont été transférés avec succès vers le client avant l’appel de la méthode **Complete** sont à la disposition de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e7d26-110">Only those files that BITS successfully transferred to the client before you called the **Complete** method are available to the user.</span></span>

<span data-ttu-id="e7d26-111">Pour les tâches de chargement, appelez la méthode [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) uniquement si l’état du travail est \_ État du travail BG \_ \_ transféré.</span><span class="sxs-lookup"><span data-stu-id="e7d26-111">For upload jobs, call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method only if the job's state is BG\_JOB\_STATE\_TRANSFERRED.</span></span> <span data-ttu-id="e7d26-112">Pour déterminer quand l’état du travail est transfert de l’état de la tâche BG \_ \_ \_ , [interrogez](polling-for-the-status-of-the-job.md) la propriété de l’état du travail ou inscrivez-vous pour recevoir la \_ notification d’événements de transfert de travail BG Notify \_ \_ . [](registering-a-com-callback.md)</span><span class="sxs-lookup"><span data-stu-id="e7d26-112">To determine when the job's state is BG\_JOB\_STATE\_TRANSFERRED, [poll](polling-for-the-status-of-the-job.md) the job's state property or register to receive BG\_NOTIFY\_JOB\_TRANSFERRED [event notification](registering-a-com-callback.md).</span></span>

<span data-ttu-id="e7d26-113">Pour annuler une tâche de transfert, appelez la méthode [**méthode ibackgroundcopyjob :: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="e7d26-113">To cancel a transfer job, call the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span> <span data-ttu-id="e7d26-114">La méthode **Cancel** supprime le travail de la file d’attente de transfert et supprime les fichiers temporaires du client.</span><span class="sxs-lookup"><span data-stu-id="e7d26-114">The **Cancel** method removes the job from the transfer queue and removes the temporary files from the client.</span></span> <span data-ttu-id="e7d26-115">En général, vous appelez cette méthode si vous ne parvenez pas à résoudre une erreur associée au travail.</span><span class="sxs-lookup"><span data-stu-id="e7d26-115">Typically, you call this method if you are unable to resolve an error associated with the job.</span></span>

<span data-ttu-id="e7d26-116">La méthode [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) annule un chargement si le chargement n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="e7d26-116">The [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method cancels an upload if the upload is not complete.</span></span> <span data-ttu-id="e7d26-117">Si le téléchargement est terminé et que le travail est de type réponse du type \_ de travail BG \_ \_ \_ , la méthode annule la réponse.</span><span class="sxs-lookup"><span data-stu-id="e7d26-117">If the upload is complete, and the job is of type BG\_JOB\_TYPE\_UPLOAD\_REPLY, the method cancels the reply.</span></span>

<span data-ttu-id="e7d26-118">Si vous n’appelez pas la méthode [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou la méthode [**méthode ibackgroundcopyjob :: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) dans un délai de 90 jours (par défaut [paramètre jobinactivitytimeout](group-policies.md) stratégie de groupe), le service annule le travail.</span><span class="sxs-lookup"><span data-stu-id="e7d26-118">If you do not call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method within 90 days (default [JobInactivityTimeout](group-policies.md) Group Policy), the service cancels the job.</span></span> <span data-ttu-id="e7d26-119">Si le service annule le travail, les fichiers téléchargés et le fichier de réponse ne sont pas disponibles pour le client ; l’annulation du travail n’affecte pas les fichiers qui ont été téléchargés avec succès.</span><span class="sxs-lookup"><span data-stu-id="e7d26-119">If the service cancels the job, the downloaded files and the reply file are not available to the client; job cancellation does not affect files that have been successfully uploaded.</span></span> <span data-ttu-id="e7d26-120">Vous devez toujours appeler la méthode **Complete** ou **Cancel** et ne pas compter sur la stratégie paramètre jobinactivitytimeout pour nettoyer vos travaux.</span><span class="sxs-lookup"><span data-stu-id="e7d26-120">You should always call the **Complete** or the **Cancel** method and not rely on the JobInactivityTimeout policy to cleanup your jobs.</span></span> <span data-ttu-id="e7d26-121">Les travaux laissés dans la file d’attente peuvent empêcher les utilisateurs de créer d’autres travaux si la limite de stratégie MaxJobsPerUser ou MaxJobsPerMachine est atteinte.</span><span class="sxs-lookup"><span data-stu-id="e7d26-121">Jobs left in the queue may prevent users from creating other jobs if the MaxJobsPerUser or MaxJobsPerMachine policy limit is reached.</span></span>

 

 




