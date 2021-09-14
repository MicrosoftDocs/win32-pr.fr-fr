---
description: Les fonctions suivantes sont utilisées avec les transactions.
ms.assetid: e9704ea8-e67d-4278-b77e-1d4787224d52
title: Fonctions du gestionnaire de transactions du noyau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221bcc13bb1cfb1f8cc67eb4d16f40a27799b921
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094501"
---
# <a name="kernel-transaction-manager-functions"></a>Fonctions du gestionnaire de transactions du noyau

Les fonctions suivantes sont utilisées avec les transactions.



| Fonction                                                            | Description                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Demande que la transaction spécifiée soit validée.                                           |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Demande que la transaction spécifiée soit validée.                                           |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Crée un nouvel objet de transaction.                                                               |
| [**GetTransactionId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionid)                        | Obtient l’ID de la transaction spécifiée.                                                   |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Retourne les informations demandées sur la transaction spécifiée.                              |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Ouvre une transaction existante.                                                                  |
| [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)                        | Indique que le gestionnaire de ressources (RM) a réussi à restaurer une transaction. |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Demande que la transaction spécifiée soit restaurée.                                         |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Demande que la transaction spécifiée soit restaurée. Cette fonction retourne de manière asynchrone.   |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Définit les informations de transaction pour la transaction spécifiée.                                 |



 

Les fonctions suivantes sont utilisées avec les enlistes.



| Fonction                                                                          | Description                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indique qu’un gestionnaire de transactions a terminé la validation d’une transaction qui a été demandée par le gestionnaire de transactions (TM).                                                                                                                                                                                                                                                                        |
| [**CommitEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-commitenlistment)                                      | Valide la transaction pour l’inscription spécifiée.                                                                                                                                                                                                                                                                                                                                |
| [**GetEnlistmentId**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentid)                                        | Obtient l’ID de l’inscription spécifiée.                                                                                                                                                                                                                                                                                                                                         |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Crée une inscription, définit son état initial et ouvre un handle vers l’inscription avec l’accès spécifié.                                                                                                                                                                                                                                                                       |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Récupère une structure opaque de données de récupération à partir de KTM. Les informations de récupération sont stockées dans un journal au nom d’un RM en appelant la fonction [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) . Après une défaillance, le gestionnaire de données peut utiliser la fonction [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) pour récupérer les informations. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Ouvre un objet d’inscription existant et retourne un handle à l’inscription.                                                                                                                                                                                                                                                                                                         |
| [**PrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-prepareenlistment)                                    | Appelé par le gestionnaire de configuration supérieur pour indiquer que son travail avant préparation est terminé.                                                                                                                                                                                                                                                                                                   |
| [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)                              | Appelé par le gestionnaire de configuration supérieur pour indiquer que son travail avant préparation est terminé.                                                                                                                                                                                                                                                                                                   |
| [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment)                                    | Récupère l’état d’une inscription.                                                                                                                                                                                                                                                                                                                                                      |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Demande que l’inscription spécifiée soit convertie en une inscription en lecture seule. Une inscription en lecture seule ne peut pas participer au résultat de la transaction et n’est pas enregistrée de façon durable pour la récupération.                                                                                                                                                                                 |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Restaure la transaction spécifiée associée à une inscription. Cette fonction ne peut pas être appelée pour des enrôlements en lecture seule.                                                                                                                                                                                                                                                |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Définit une structure opaque, définie par l’utilisateur, des données de récupération à partir de KTM. Les informations de récupération sont stockées dans un journal au nom d’un RM en appelant [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation). Après une défaillance, le gestionnaire de données peut utiliser [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) pour récupérer les informations.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indique que le RM refuse une demande en une seule phase. Lorsqu’un TM reçoit cet appel, il Initialise une validation en deux phases et envoie une demande de préparation à tous les services RMs listés.                                                                                                                                                                                                             |



 

Les fonctions suivantes sont utilisées avec les gestionnaires de ressources.



| Fonction                                                                           | Description                                                                                                                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager,**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Crée un nouvel objet RM et l’associe à un gestionnaire de transactions (TM).                                                                                  |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Demande et reçoit une notification pour RM. Cette fonction est utilisée par le registre RM pour recevoir des notifications lorsqu’une transaction change d’État.                 |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Demande et reçoit une notification asynchrone pour un RM. Cette fonction est utilisée par le gestionnaire de transactions pour s’inscrire afin de recevoir des notifications lorsqu’une transaction change d’État. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Ouvre un RM existant.                                                                                                                                            |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Indique que le gestionnaire de transactions a effectué tout le traitement nécessaire pour garantir qu’une opération de validation ou d’abandon réussit pour la transaction spécifiée.           |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Signale que ce gestionnaire de tâches a terminé son travail de prépréparation, afin que d’autres services RMs puissent maintenant commencer à effectuer leurs opérations de préparation.                                                |
| [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager)                           | Récupère l’état d’un gestionnaire de comptes à partir de son fichier journal.                                                                                                                         |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Associe le port de terminaison d’e/s spécifié au RM spécifié. Ce port reçoit toutes les notifications pour le gestionnaire de comptes.                                             |



 

Les fonctions suivantes sont utilisées avec les gestionnaires de transactions.



| Fonction                                                                            | Description                                                                 |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Crée un nouvel objet TM et retourne un handle avec l’accès spécifié.     |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Obtient une valeur d’horloge virtuelle à partir d’une TM.                                    |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Obtient un identificateur pour la TM spécifiée.                                 |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Ouvre une TM existante.                                                       |
| [**OpenTransactionManagerById**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanagerbyid)                    | Ouvre une TM existante.                                                       |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Récupère l’état d’un TM à partir de son fichier journal.                                    |
| [**RenameTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-renametransactionmanager)                        | Renomme une TM.                                                               |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Récupère l’état du gestionnaire de fichiers de son fichier journal à la valeur d’horloge virtuelle spécifiée. |



 

 

 



