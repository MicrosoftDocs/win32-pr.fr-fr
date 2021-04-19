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
# <a name="notification_mask"></a>masque de NOTIFICATION \_

Répertorie les différents types de notifications qui peuvent être reçus par une inscription.

<dl> <dt>

<span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**\_masque de notification des transactions \_**
</dt> <dd> <dl> <dt>

0x3FFFFFFF
</dt> <dt>



Masque qui indique tous les bits valides pour une notification de transaction.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**prépréparation de la TRANSACTION \_ Notify \_**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Cette notification est appelée après qu’un client a appelé [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) et qu’aucun gestionnaire de ressources (RM) ne prend en charge la validation à phase unique ou qu’un gestionnaire de transactions supérieur (TM) appelle [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment). Cette notification est reçue par le RMs, indiquant qu’elle doit effectuer tout travail susceptible d’entraîner la nécessité de l’inscription d’autres services RMs dans une transaction, par exemple le vidage de son cache. Une fois ces opérations terminées, le gestionnaire de tâches doit appeler [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete). Pour recevoir cette notification, le gestionnaire de transactions doit également prendre en charge la validation de **transaction \_ Notify \_ Prepare** et **transaction \_ Notify \_ Commit**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**TRANSACTION \_ Notify \_ Prepare**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Cette notification est appelée une fois le traitement de **\_ \_ prépréparation de la transaction Notify** terminé. Il signale au gestionnaire de tâches d’effectuer tout le travail associé à cette inscription afin de garantir qu’une opération de validation peut aboutir et qu’une opération d’abandon peut également aboutir. En règle générale, la majeure partie du travail d’une transaction est effectuée au cours de la phase de préparation. Pour les services RMs durables, ils doivent enregistrer leur état avant d’appeler la fonction [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) . Il s’agit de la dernière chance pour le RM de demander que la transaction soit restaurée.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**TRANSACTION \_ Notify \_ Commit**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Cette notification signale au RM d’effectuer tout le travail associé à cette inscription. En règle générale, le gestionnaire de distribution libère tous les verrous, libère les informations nécessaires à la restauration de la transaction. Le gestionnaire de tâches doit répondre en appelant la fonction [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) une fois ces opérations terminées.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**TRANSACTION \_ Notify \_ Rollback**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Cette notification signale au RM d’annuler tout le travail qu’il a effectué et associé à la transaction.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**prépréparation de la notification de TRANSACTION \_ \_ \_ terminée**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Cette notification signale au gestionnaire de configuration supérieur qu’une opération de prépréparation a été effectuée avec succès.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**TRANSACTION \_ Notify \_ Prepare \_ Complete**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Cette notification signale au gestionnaire de traduction supérieur qu’une opération de préparation a été effectuée avec succès.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**TRANSACTION de \_ notification de \_ validation \_ terminée**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Cette notification signale au gestionnaire de traduction supérieur qu’une opération de validation a été effectuée avec succès.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**restauration de la notification de TRANSACTION \_ \_ \_ terminée**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Cette notification signale au gestionnaire de traduction supérieur qu’une opération de restauration a été effectuée avec succès.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**\_notification de récupération de la transaction \_**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Cette notification signale à RMs qu’il doit récupérer son état, car un résultat de transaction doit être remis à son état. Par exemple, lorsqu’un RM est récupéré et lorsqu’il reste des transactions incertaines. Cette notification est remise une fois que l’état incertain est résolu.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**TRANSACTION \_ Notify en \_ une seule \_ phase \_ validation**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Cette notification indique au gestionnaire de transactions de se terminer et de valider la transaction sans utiliser un protocole de validation en deux phases. Si le gestionnaire de comptes de service souhaite utiliser une opération en deux phases, il doit répondre en appelant la fonction [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) .


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**TRANSACTION \_ notifier la \_ validation de délégué \_**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



KTM signale au gestionnaire de transactions supérieur qu’il doit effectuer une opération de validation.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**requête de récupération de la TRANSACTION \_ Notify \_ \_**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



KTM signale au gestionnaire de transactions supérieur qu’il doit interroger l’état d’une transaction incertaine.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**TRANSACTION \_ notifier \_ \_ prépréparer l’inscription**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Cette notification signale au gestionnaire de configuration supérieur que les notifications de prépréparation doivent être fournies dans l’inscription spécifiée.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**TRANSACTION \_ Notify \_ dernière \_ récupération**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Cette notification indique que l’opération de récupération est terminée pour ce RM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**\_notifier \_ incertaine la transaction**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



La transaction spécifiée est dans un état incertain. Le RM reçoit cette notification pendant les opérations de récupération lorsqu’une transaction a été préparée, mais qu’il n’existe pas de gestionnaire de transactions supérieur (TM) disponible. Par exemple, lorsqu’une transaction implique un gestionnaire de transactions distant et que ce nœud n’est pas disponible, que son nœud n’est pas disponible ou que le service de [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) local n’est pas disponible, l’état de la transaction est incertain.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**notification de TRANSACTION \_ \_ TM \_ en ligne**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Le gestionnaire de traduction est en ligne et accepte les demandes.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**résultat de la demande de notification de TRANSACTION \_ \_ \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Signale à RMs qu’il y a des informations de résultat disponibles et qu’une demande de ces informations doit être effectuée.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**TRANSACTION \_ Notify \_ Commit \_ Finalize**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Réservé.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                            |
| En-tête<br/>                   | <dl> <dt>KtmTypes. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Coordinateur de transactions distribuées](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> <dt>

[Constantes du gestionnaire de transactions du noyau](kernel-transaction-manager-constants.md)
</dt> <dt>

[**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[**NOTIFICATION de TRANSACTION \_**](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

