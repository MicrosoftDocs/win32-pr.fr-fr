---
description: Répertorie les différents types de notifications qui peuvent être reçus par une inscription.
ms.assetid: 65db8ba5-193c-439b-8e8c-6cb4a9bd4efd
title: NOTIFICATION_MASK (KtmTypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3650c10f619cf45db34d9172476261838897a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520624"
---
# <a name="notification_mask"></a><span data-ttu-id="c81bb-103">masque de NOTIFICATION \_</span><span class="sxs-lookup"><span data-stu-id="c81bb-103">NOTIFICATION\_MASK</span></span>

<span data-ttu-id="c81bb-104">Répertorie les différents types de notifications qui peuvent être reçus par une inscription.</span><span class="sxs-lookup"><span data-stu-id="c81bb-104">Lists the different types of notifications that can be received by an enlistment.</span></span>

<dl> <dt>

<span data-ttu-id="c81bb-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**\_masque de notification des transactions \_**</span><span class="sxs-lookup"><span data-stu-id="c81bb-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**TRANSACTION\_NOTIFY\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-106">0x3FFFFFFF</span><span class="sxs-lookup"><span data-stu-id="c81bb-106">0x3FFFFFFF</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-107">Masque qui indique tous les bits valides pour une notification de transaction.</span><span class="sxs-lookup"><span data-stu-id="c81bb-107">A mask that indicates all valid bits for a transaction notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**prépréparation de la TRANSACTION \_ Notify \_**</span><span class="sxs-lookup"><span data-stu-id="c81bb-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**TRANSACTION\_NOTIFY\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c81bb-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-110">Cette notification est appelée après qu’un client a appelé [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) et qu’aucun gestionnaire de ressources (RM) ne prend en charge la validation à phase unique ou qu’un gestionnaire de transactions supérieur (TM) appelle [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment).</span><span class="sxs-lookup"><span data-stu-id="c81bb-110">This notification is called after a client calls [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) and either no resource manager (RM) supports single-phase commit or a superior transaction manager (TM) calls [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment).</span></span> <span data-ttu-id="c81bb-111">Cette notification est reçue par le RMs, indiquant qu’elle doit effectuer tout travail susceptible d’entraîner la nécessité de l’inscription d’autres services RMs dans une transaction, par exemple le vidage de son cache.</span><span class="sxs-lookup"><span data-stu-id="c81bb-111">This notification is received by the RMs indicating that they should complete any work that could cause other RMs to need to enlist in a transaction, such as flushing its cache.</span></span> <span data-ttu-id="c81bb-112">Une fois ces opérations terminées, le gestionnaire de tâches doit appeler [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete).</span><span class="sxs-lookup"><span data-stu-id="c81bb-112">After completing these operations the RM must call [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete).</span></span> <span data-ttu-id="c81bb-113">Pour recevoir cette notification, le gestionnaire de transactions doit également prendre en charge la validation de **transaction \_ Notify \_ Prepare** et **transaction \_ Notify \_ Commit**.</span><span class="sxs-lookup"><span data-stu-id="c81bb-113">To receive this notification the RM must also support **TRANSACTION\_NOTIFY\_PREPARE** and **TRANSACTION\_NOTIFY\_COMMIT**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**TRANSACTION \_ Notify \_ Prepare**</span><span class="sxs-lookup"><span data-stu-id="c81bb-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**TRANSACTION\_NOTIFY\_PREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c81bb-115">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-116">Cette notification est appelée une fois le traitement de **\_ \_ prépréparation de la transaction Notify** terminé.</span><span class="sxs-lookup"><span data-stu-id="c81bb-116">This notification is called after the **TRANSACTION\_NOTIFY\_PREPREPARE** processing is complete.</span></span> <span data-ttu-id="c81bb-117">Il signale au gestionnaire de tâches d’effectuer tout le travail associé à cette inscription afin de garantir qu’une opération de validation peut aboutir et qu’une opération d’abandon peut également aboutir.</span><span class="sxs-lookup"><span data-stu-id="c81bb-117">It signals the RM to complete all the work that is associated with this enlistment so that it can guarantee that a commit operation could succeed and an abort operation could also succeed.</span></span> <span data-ttu-id="c81bb-118">En règle générale, la majeure partie du travail d’une transaction est effectuée au cours de la phase de préparation.</span><span class="sxs-lookup"><span data-stu-id="c81bb-118">Typically, the bulk of the work for a transaction is done during the prepare phase.</span></span> <span data-ttu-id="c81bb-119">Pour les services RMs durables, ils doivent enregistrer leur état avant d’appeler la fonction [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) .</span><span class="sxs-lookup"><span data-stu-id="c81bb-119">For durable RMs, they must log their state prior to calling the [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) function.</span></span> <span data-ttu-id="c81bb-120">Il s’agit de la dernière chance pour le RM de demander que la transaction soit restaurée.</span><span class="sxs-lookup"><span data-stu-id="c81bb-120">This is the last chance for the RM to request that the transaction be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**TRANSACTION \_ Notify \_ Commit**</span><span class="sxs-lookup"><span data-stu-id="c81bb-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**TRANSACTION\_NOTIFY\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c81bb-122">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-123">Cette notification signale au RM d’effectuer tout le travail associé à cette inscription.</span><span class="sxs-lookup"><span data-stu-id="c81bb-123">This notification signals the RM to complete all the work that is associated with this enlistment.</span></span> <span data-ttu-id="c81bb-124">En règle générale, le gestionnaire de distribution libère tous les verrous, libère les informations nécessaires à la restauration de la transaction.</span><span class="sxs-lookup"><span data-stu-id="c81bb-124">Typically, the RM releases any locks, releases any information necessary to roll back the transaction.</span></span> <span data-ttu-id="c81bb-125">Le gestionnaire de tâches doit répondre en appelant la fonction [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) une fois ces opérations terminées.</span><span class="sxs-lookup"><span data-stu-id="c81bb-125">The RM must respond by calling the [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) function when it has finished these operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**TRANSACTION \_ Notify \_ Rollback**</span><span class="sxs-lookup"><span data-stu-id="c81bb-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**TRANSACTION\_NOTIFY\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-127">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c81bb-127">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-128">Cette notification signale au RM d’annuler tout le travail qu’il a effectué et associé à la transaction.</span><span class="sxs-lookup"><span data-stu-id="c81bb-128">This notification signals the RM to undo all the work it has done that is associated with the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**prépréparation de la notification de TRANSACTION \_ \_ \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="c81bb-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-130">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c81bb-130">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-131">Cette notification signale au gestionnaire de configuration supérieur qu’une opération de prépréparation a été effectuée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c81bb-131">This notification signals to the superior TM that a pre-prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**TRANSACTION \_ Notify \_ Prepare \_ Complete**</span><span class="sxs-lookup"><span data-stu-id="c81bb-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-133">0x00000020</span><span class="sxs-lookup"><span data-stu-id="c81bb-133">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-134">Cette notification signale au gestionnaire de traduction supérieur qu’une opération de préparation a été effectuée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c81bb-134">This notification signals to the superior TM that a prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**TRANSACTION de \_ notification de \_ validation \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="c81bb-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**TRANSACTION\_NOTIFY\_COMMIT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-136">0x00000040</span><span class="sxs-lookup"><span data-stu-id="c81bb-136">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-137">Cette notification signale au gestionnaire de traduction supérieur qu’une opération de validation a été effectuée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c81bb-137">This notification signals to the superior TM that a commit operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**restauration de la notification de TRANSACTION \_ \_ \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="c81bb-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**TRANSACTION\_NOTIFY\_ROLLBACK\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="c81bb-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-140">Cette notification signale au gestionnaire de traduction supérieur qu’une opération de restauration a été effectuée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c81bb-140">This notification signals to the superior TM that a rollback operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**\_notification de récupération de la transaction \_**</span><span class="sxs-lookup"><span data-stu-id="c81bb-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**TRANSACTION\_NOTIFY\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="c81bb-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-143">Cette notification signale à RMs qu’il doit récupérer son état, car un résultat de transaction doit être remis à son état.</span><span class="sxs-lookup"><span data-stu-id="c81bb-143">This notification signals to RMs that they should recover their state because a transaction outcome must be redelivered.</span></span> <span data-ttu-id="c81bb-144">Par exemple, lorsqu’un RM est récupéré et lorsqu’il reste des transactions incertaines.</span><span class="sxs-lookup"><span data-stu-id="c81bb-144">For example, when an RM is recovered, and when there are transactions left in-doubt.</span></span> <span data-ttu-id="c81bb-145">Cette notification est remise une fois que l’état incertain est résolu.</span><span class="sxs-lookup"><span data-stu-id="c81bb-145">This notification is delivered once the in-doubt state is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**TRANSACTION \_ Notify en \_ une seule \_ phase \_ validation**</span><span class="sxs-lookup"><span data-stu-id="c81bb-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**TRANSACTION\_NOTIFY\_SINGLE\_PHASE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-147">0x00000200</span><span class="sxs-lookup"><span data-stu-id="c81bb-147">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-148">Cette notification indique au gestionnaire de transactions de se terminer et de valider la transaction sans utiliser un protocole de validation en deux phases.</span><span class="sxs-lookup"><span data-stu-id="c81bb-148">This notification signals the RM to complete and commit the transaction without using a two-phase commit protocol.</span></span> <span data-ttu-id="c81bb-149">Si le gestionnaire de comptes de service souhaite utiliser une opération en deux phases, il doit répondre en appelant la fonction [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) .</span><span class="sxs-lookup"><span data-stu-id="c81bb-149">If the RM wants to use a two-phase operation, it must respond by calling the [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**TRANSACTION \_ notifier la \_ validation de délégué \_**</span><span class="sxs-lookup"><span data-stu-id="c81bb-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**TRANSACTION\_NOTIFY\_DELEGATE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-151">0x00000400</span><span class="sxs-lookup"><span data-stu-id="c81bb-151">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-152">KTM signale au gestionnaire de transactions supérieur qu’il doit effectuer une opération de validation.</span><span class="sxs-lookup"><span data-stu-id="c81bb-152">KTM is signaling to the superior TM to perform a commit operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**requête de récupération de la TRANSACTION \_ Notify \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c81bb-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**TRANSACTION\_NOTIFY\_RECOVER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-154">0x00000800</span><span class="sxs-lookup"><span data-stu-id="c81bb-154">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-155">KTM signale au gestionnaire de transactions supérieur qu’il doit interroger l’état d’une transaction incertaine.</span><span class="sxs-lookup"><span data-stu-id="c81bb-155">KTM is signaling to the superior TM to query the status of an in-doubt transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**TRANSACTION \_ notifier \_ \_ prépréparer l’inscription**</span><span class="sxs-lookup"><span data-stu-id="c81bb-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**TRANSACTION\_NOTIFY\_ENLIST\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-157">0x00001000</span><span class="sxs-lookup"><span data-stu-id="c81bb-157">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-158">Cette notification signale au gestionnaire de configuration supérieur que les notifications de prépréparation doivent être fournies dans l’inscription spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c81bb-158">This notification signals to the superior TM that pre-prepare notifications must be delivered on the specified enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**TRANSACTION \_ Notify \_ dernière \_ récupération**</span><span class="sxs-lookup"><span data-stu-id="c81bb-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**TRANSACTION\_NOTIFY\_LAST\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-160">0x00002000</span><span class="sxs-lookup"><span data-stu-id="c81bb-160">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-161">Cette notification indique que l’opération de récupération est terminée pour ce RM.</span><span class="sxs-lookup"><span data-stu-id="c81bb-161">This notification indicates that the recovery operation is complete for this RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**\_notifier \_ incertaine la transaction**</span><span class="sxs-lookup"><span data-stu-id="c81bb-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**TRANSACTION\_NOTIFY\_INDOUBT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-163">0x00004000</span><span class="sxs-lookup"><span data-stu-id="c81bb-163">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-164">La transaction spécifiée est dans un état incertain.</span><span class="sxs-lookup"><span data-stu-id="c81bb-164">The specified transaction is in an in-doubt state.</span></span> <span data-ttu-id="c81bb-165">Le RM reçoit cette notification pendant les opérations de récupération lorsqu’une transaction a été préparée, mais qu’il n’existe pas de gestionnaire de transactions supérieur (TM) disponible.</span><span class="sxs-lookup"><span data-stu-id="c81bb-165">The RM receives this notification during recovery operations when a transaction has been prepared, but there is no superior transaction manager (TM) available.</span></span> <span data-ttu-id="c81bb-166">Par exemple, lorsqu’une transaction implique un gestionnaire de transactions distant et que ce nœud n’est pas disponible, que son nœud n’est pas disponible ou que le service de [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) local n’est pas disponible, l’état de la transaction est incertain.</span><span class="sxs-lookup"><span data-stu-id="c81bb-166">For example, when a transaction involves a remote TM and that node is unavailable, its node is unavailable, or the local [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) service is unavailable, the transaction state is in-doubt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**notification de TRANSACTION \_ \_ TM \_ en ligne**</span><span class="sxs-lookup"><span data-stu-id="c81bb-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**TRANSACTION\_NOTIFY\_TM\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-168">0x02000000</span><span class="sxs-lookup"><span data-stu-id="c81bb-168">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-169">Le gestionnaire de traduction est en ligne et accepte les demandes.</span><span class="sxs-lookup"><span data-stu-id="c81bb-169">The TM is online and accepting requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**résultat de la demande de notification de TRANSACTION \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c81bb-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**TRANSACTION\_NOTIFY\_REQUEST\_OUTCOME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-171">0x20000000</span><span class="sxs-lookup"><span data-stu-id="c81bb-171">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-172">Signale à RMs qu’il y a des informations de résultat disponibles et qu’une demande de ces informations doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="c81bb-172">Signals to RMs that there is outcome information available, and that a request for that information should be made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c81bb-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**TRANSACTION \_ Notify \_ Commit \_ Finalize**</span><span class="sxs-lookup"><span data-stu-id="c81bb-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**TRANSACTION\_NOTIFY\_COMMIT\_FINALIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c81bb-174">0x40000000</span><span class="sxs-lookup"><span data-stu-id="c81bb-174">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="c81bb-175">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c81bb-175">Reserved.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c81bb-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c81bb-176">Requirements</span></span>



| <span data-ttu-id="c81bb-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c81bb-177">Requirement</span></span> | <span data-ttu-id="c81bb-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="c81bb-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c81bb-179">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c81bb-179">Minimum supported client</span></span><br/> | <span data-ttu-id="c81bb-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c81bb-180">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="c81bb-181">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c81bb-181">Minimum supported server</span></span><br/> | <span data-ttu-id="c81bb-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c81bb-182">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="c81bb-183">En-tête</span><span class="sxs-lookup"><span data-stu-id="c81bb-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="c81bb-184"><dt>KtmTypes. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c81bb-184"><dt>KtmTypes.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c81bb-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c81bb-185">See also</span></span>

<dl> <dt>

<span data-ttu-id="c81bb-186">[Coordinateur de transactions distribuées](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c81bb-186">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c81bb-187">Constantes du gestionnaire de transactions du noyau</span><span class="sxs-lookup"><span data-stu-id="c81bb-187">Kernel Transaction Manager Constants</span></span>](kernel-transaction-manager-constants.md)
</dt> <dt>

[<span data-ttu-id="c81bb-188">**CreateEnlistment**</span><span class="sxs-lookup"><span data-stu-id="c81bb-188">**CreateEnlistment**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[<span data-ttu-id="c81bb-189">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="c81bb-189">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[<span data-ttu-id="c81bb-190">**GetNotificationResourceManager**</span><span class="sxs-lookup"><span data-stu-id="c81bb-190">**GetNotificationResourceManager**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[<span data-ttu-id="c81bb-191">**GetNotificationResourceManagerAsync**</span><span class="sxs-lookup"><span data-stu-id="c81bb-191">**GetNotificationResourceManagerAsync**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[<span data-ttu-id="c81bb-192">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="c81bb-192">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[<span data-ttu-id="c81bb-193">**SinglePhaseReject**</span><span class="sxs-lookup"><span data-stu-id="c81bb-193">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[<span data-ttu-id="c81bb-194">**NOTIFICATION de TRANSACTION \_**</span><span class="sxs-lookup"><span data-stu-id="c81bb-194">**TRANSACTION\_NOTIFICATION**</span></span>](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

