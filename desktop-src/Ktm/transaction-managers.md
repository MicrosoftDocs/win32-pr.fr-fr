---
description: Un gestionnaire de transactions (TM) est une instance d’un journal. Dans KTM, les objets TM spécifient le journal et certaines fonctionnalités du gestionnaire de transactions. Il y a généralement de nombreux objets TM sur un nœud particulier. Les gestionnaires de ressources (RMs) doivent être associés à un gestionnaire de traduction spécifique.
ms.assetid: 8d43977a-84cf-4109-b7db-f9c94a226c5d
title: Gestionnaires de transactions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ea492a3eb10d95002d4e0a61500e7f1e74e87da21bc90daf680a2899e3fa67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424439"
---
# <a name="transaction-managers"></a>Gestionnaires de transactions

Un gestionnaire de transactions (TM) est une instance d’un journal. Dans KTM, les objets TM spécifient le journal et certaines fonctionnalités du gestionnaire de transactions. Il y a généralement de nombreux objets TM sur un nœud particulier. Les gestionnaires de ressources (RMs) doivent être associés à un gestionnaire de traduction spécifique. Il existe trois types de TMs :

-   Un TM volatile, qui n’a pas de journal.
-   TM standard, qui dispose d’un journal et permet de coordonner les transactions d’un ou de plusieurs services RMs.
-   Gestionnaire de transactions supérieur.

## <a name="volatile-transaction-managers"></a>Gestionnaires de transactions volatiles

Un TM volatile est un TM pour les services RMs en lecture seule ou volatiles. Il n’a pas de journal et ne conserve pas l’état des transactions entre les redémarrages du système.

## <a name="transaction-managers"></a>Gestionnaires de transactions

TMs ont un journal, un ou plusieurs services RMs durables ou volatiles, ou les deux. Le gestionnaire de transactions conserve l’état d’une transaction sur les redémarrages du système jusqu’à ce que les transactions soient terminées. Un modèle présumé d’abandon est utilisé, donc les transactions qui étaient actives mais non préparées lorsque l’objet TM est arrêté sont restaurées. Lorsque vous ouvrez une TM pour la première fois, vous devez récupérer la TM en appelant la fonction [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager) .

## <a name="superior-transaction-managers"></a>Gestionnaires de transactions supérieurs

Un gestionnaire de traduction supérieur est un gestionnaire de traduction pour d’autres TMs. Il coordonne les transactions. Il émet également des notifications de **\_ \_ préparation de la transaction Notify** au gestionnaire de transactions KTM (Kernel Transaction Manager). Le Distributed Transaction Coordinator Microsoft (DTC) est un exemple de gestionnaire de transactions supérieur. Cette capacité est accompagnée d’une responsabilité dans le temps de récupération. Pendant la récupération, le gestionnaire de comptes doit d’abord appeler la fonction [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) pour rouvrir l’inscription. Elle doit également fournir (ou remettre à nouveau) le résultat de la transaction si la transaction a été validée ; Il est libre de fournir un résultat en appelant la fonction [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) ou la fonction [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction) . Cette obligation ne se termine pas tant qu’elle n’a pas reçu d’événement de notification de **validation de transaction \_ Notify \_ \_ complet** ou **transaction \_ Notify \_ \_ Complete** . Si un gestionnaire de transactions supérieur ne parvient pas à effectuer ces opérations au moment de la récupération, le KTM nettoie toutes les transactions qui n’ont pas reçu de résultats à la fin de la phase de récupération. Toutefois, cela peut entraîner des résultats incohérents de transaction.

## <a name="transaction-manager-functions"></a>Fonctions du gestionnaire de transactions

Les fonctions suivantes sont utilisées avec les gestionnaires de transactions.



| Fonction                                                                            | Description                                                                                    |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Crée un nouvel objet de gestionnaire de transactions (TM) et retourne un handle avec l’accès spécifié.  |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Obtient une valeur d’horloge virtuelle à partir d’un gestionnaire de transactions.                                      |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Obtient un identificateur pour le gestionnaire de transactions spécifié.                                   |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Ouvre un gestionnaire de transactions existant.                                                         |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Récupère l’état d’un gestionnaire de transactions à partir de son fichier journal.                                      |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Récupère l’état d’un gestionnaire de transactions à partir de son fichier journal vers la valeur d’horloge virtuelle spécifiée. |



 

 

 



