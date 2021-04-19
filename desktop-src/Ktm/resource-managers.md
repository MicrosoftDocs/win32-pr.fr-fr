---
description: Gestionnaires de ressources
ms.assetid: c717b731-cf0b-45cb-bbff-695410fcf6ce
title: Gestionnaires de ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2ea9b1cd834daf3bfbca49bf37d3f2c0956344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527858"
---
# <a name="resource-managers"></a>Gestionnaires de ressources

Un gestionnaire de ressources utilise le journal du gestionnaire de transactions pour suivre l’état de la transaction. L’action du gestionnaire de ressources lors du traitement d’une transaction est la suivante :

-   Le client transmet explicitement une transaction au gestionnaire de transactions.
-   Le gestionnaire de transactions inscrit dans la transaction à l’aide de [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment).
-   L’utilisateur peut ensuite procéder à toute opération.
-   Lorsque l’utilisateur appelle CommitTransaction, KTM envoie une \_ notification de préparation de transaction au gestionnaire de transactions. À ce stade, le gestionnaire de transactions vide sur le disque toutes les modifications nécessaires pour valider la transaction, mais peut échouer. Si ces opérations réussissent, le RM signale qu’il a terminé l’opération de préparation en appelant [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete). Si ces opérations échouent, le gestionnaire de tâches répond en appelant [**RollBackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).
-   Le gestionnaire des ressources reçoit une notification de préparation.
-   Le gestionnaire de ressources vide toutes les données associées à la transaction dans son fichier journal des services de journalisation commun.
-   Le gestionnaire des ressources appelle la fonction [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) et attend de recevoir le résultat de la transaction du KTM.
-   Selon le résultat de la transaction, le gestionnaire des ressources reçoit un événement de notification de validation ou de restauration. Si le gestionnaire de ressources reçoit une notification de validation, il rend les modifications permanentes et informe le KTM en appelant la fonction [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) . Si le gestionnaire de ressources reçoit une notification de restauration, il ignore toutes les modifications et revient à l’État qui existait avant l’une des modifications traitées et informe le KTM en appelant [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete).

## <a name="resource-manager-functions"></a>Fonctions Gestionnaire des ressources

Les fonctions suivantes sont utilisées avec les gestionnaires de ressources.



| Fonction                                                                           | Description                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager,**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Crée un nouvel objet Resource Manager (RM) et l’associe à un gestionnaire de transactions (TM).                                                                               |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Demande et reçoit une notification pour un gestionnaire de ressources (RM). Cette fonction est utilisée par le registre RM pour recevoir des notifications lorsqu’une transaction change d’État.            |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Demande et reçoit une notification asynchrone pour un gestionnaire de ressources (RM). Cette fonction est utilisée par le registre RM pour recevoir des notifications lorsqu’une transaction change d’État. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Ouvre un gestionnaire de ressources existant (RM).                                                                                                                                         |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Indique que le gestionnaire de ressources a terminé le traitement nécessaire pour garantir la réussite d’une opération de validation ou d’abandon pour la transaction spécifiée.        |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Signale que ce gestionnaire de ressources a terminé son travail de prépréparation, afin que d’autres gestionnaires de ressources puissent maintenant commencer leurs opérations de préparation.                                    |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Associe le port de terminaison d’e/s spécifié au gestionnaire de ressources spécifié (RM). Ce port reçoit toutes les notifications pour le gestionnaire de comptes.                                          |



 

 

 



