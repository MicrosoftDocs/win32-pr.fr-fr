---
description: Une transaction est un objet qui définit une unité logique de travail.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transactions (gestionnaire de transactions du noyau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff77ae0d89f5e334319ea0b7b73c27a4b34b57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534480"
---
# <a name="transactions"></a>Transactions

Une transaction est un objet qui définit une unité logique de travail. La transaction est active tant qu’il existe un handle référençant la transaction et qu’elle est considérée comme active si la transaction n’a pas encore été validée ou restaurée. Si une transaction est créée et que tous ses descripteurs ont été fermés avant qu’une validation ou une restauration ne se produise, la transaction est restaurée.

Prenons le cas d’un client transactionnel en mode utilisateur qui crée une transaction pour l’étendue de ses opérations, puis effectue des mises à jour sur un ou plusieurs gestionnaires de ressources. Il se produit ce qui suit :

1.  Le client appelle la fonction [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) pour créer la transaction et reçoit un descripteur de cette transaction comme valeur de retour.

    La transaction peut être ouverte ou héritée par n’importe quel nombre de processus ; chaque processus est donc impliqué dans la transaction. L’échec de l’un de ces processus entraîne l’abandon de la transaction.

    Cette transaction n’est peut-être pas encore persistante. Seules les transactions ayant atteint l’état préparé doivent être récupérées sur les défaillances du système si la transaction utilise la journalisation présumée-abandonner.

2.  Le client doit transmettre une transaction au gestionnaire des ressources de manière explicite.
3.  Le client effectue toutes ses opérations transactionnelles avec un ou plusieurs services RMs, tels que les systèmes de fichiers traités.
4.  Le client appelle la fonction [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) .
5.  Le gestionnaire des ressources reçoit les notifications de KTM pour préparer et valider ses données.

## <a name="transactions-and-threads"></a>Transactions et threads

Les transactions ne sont pas les mêmes que les threads. Plusieurs threads ou processus peuvent faire partie d’une transaction unique. À l’inverse, un thread peut faire partie de plusieurs transactions différentes à différents moments.

## <a name="transaction-functions"></a>Fonctions de transaction

Les fonctions suivantes sont utilisées avec les transactions.



| Fonction                                                            | Description                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Demande que la transaction spécifiée soit validée.                                         |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Demande que la transaction spécifiée soit validée.                                         |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Crée un nouvel objet de transaction.                                                             |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Retourne les informations demandées sur la transaction spécifiée.                            |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Ouvre une transaction existante.                                                                |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Demande que la transaction spécifiée soit restaurée.                                       |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Demande que la transaction spécifiée soit restaurée. Cette fonction retourne de manière asynchrone. |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Définit les informations de transaction pour la transaction spécifiée.                               |



 

 

 



