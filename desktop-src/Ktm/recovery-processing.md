---
description: Après tout type de défaillance qui interrompt le traitement normal des transactions, KTM et chaque gestionnaire de ressources doivent effectuer des opérations de récupération. La récupération est le processus par lequel les participants à la transaction parviennent à une vue cohérente de chaque État des transactions.
ms.assetid: 5bc9a155-6ba4-41f8-8e12-e87f48d83940
title: Traitement de la récupération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8e74d4f8bff3e56af03b017522212e7a02e232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536361"
---
# <a name="recovery-processing"></a>Traitement de la récupération

Après tout type de défaillance qui interrompt le traitement normal des transactions, KTM et chaque gestionnaire de ressources doivent effectuer des opérations de *récupération* . La récupération est le processus par lequel les participants à la transaction parviennent à une vue cohérente de l’état de chaque transaction.

Les gestionnaires de ressources peuvent être *incertains* du résultat d’une transaction, ce qui signifie qu’au moment de la défaillance, ils avaient reçu une \_ notification de préparation de la transaction Notify \_ , avait préparé un stockage durable, mais n’avait pas reçu (ou reçu, mais n’a pas enregistré) un résultat final pour la transaction. De même, KTM peut être indécis quant à une transaction si elle avait été préparée, mais qu’elle n’a pas reçu (ou reçu, mais n’a pas consigné) un résultat. Au moment de la récupération, tous les résultats qui ont été envoyés mais non reconnus doivent être renvoyés. Par exemple, si un gestionnaire de ressources a reçu une notification de validation de validation de TRANSACTION \_ et a \_ appelé la fonction [**COMMITCOMPLETE**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) , le RM peut toujours recevoir une notification de validation de transaction en double \_ \_ au moment de la récupération.

Pour qu’une transaction soit correctement Récupérée après une défaillance du système ou du gestionnaire de ressources, chaque gestionnaire de ressources doit effectuer les opérations suivantes chaque fois qu’il est démarré :

1.  Appelez la fonction [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) pour rouvrir son handle Resource Manager à l’aide de son nom unique et persistant. Cela indique que le gestionnaire de ressources est en cours d’exécution et qu’il est disponible pour effectuer la récupération. Si aucune inscription n’existe pour la récupération, l’appel à **OpenResourceManager** peut échouer. Appelez [**CreateResourceManager,**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) pour recréer l’objet RM.
2.  Appelez [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager). Le gestionnaire de ressources recevra un événement de notification de [**\_ \_ récupération**](notification-mask.md) de la transaction pour chaque inscription pour laquelle il doit effectuer des opérations de récupération, puis une transaction \_ notifier la \_ dernière \_ récupération. L’événement de notification contient un identificateur global unique pour la transaction et l’inscription.
3.  Appelez la fonction [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) pour rouvrir chaque handle d’inscription pour lequel le gestionnaire de ressources a reçu une notification de récupération de la transaction \_ Notify \_ .
4.  Pour chaque inscription ouverte par [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment), appelez [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment). Cela entraîne la \_ \_ \_ \_ remise à la livraison de la notification de notification incertaine de la transaction Notify Commit ou de transaction Notify.
5.  Si le gestionnaire de transactions a reçu une notification de validation de TRANSACTION \_ \_ , le gestionnaire de transactions peut terminer la transaction en appelant [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete).

    Si le gestionnaire de transactions a reçu une notification de non- \_ \_ incertitude, le gestionnaire de transactions doit attendre l’arrivée de la notification de résultat.

6.  Pour toutes les transactions qui ne reçoivent pas de notification de récupération de la transaction par le gestionnaire de transactions \_ \_ , mais qui ont reçu précédemment une \_ \_ notification de préparation de la transaction pour, le gestionnaire de transactions doit traiter la transaction comme si elle était restaurée.

> [!Note]
>
> Les gestionnaires de ressources sont autorisés à s’inscrire dans ou à créer de nouvelles transactions lorsqu’ils sont en cours de récupération.

 

KTM utilise un modèle de transaction d' *abandon présumé* . Le scénario suivant illustre ce comportement. Supposons que KTM et un gestionnaire de ressources existent sur le même ordinateur. Supposons que KTM émet une notification de préparation pour une transaction, mais que le système se bloque avant que KTM journalise la préparation de la notification. Supposons en outre que Resource Manager reçoit et journalise la notification de préparation juste avant l’incident du système. Une fois le système restauré, KTM n’a aucune connaissance de la transaction, car il n’a jamais enregistré la phase de préparation. Le gestionnaire de ressources a connaissance de la transaction, car il a reçu, traité et journalisé la notification de préparation. Lorsque KTM émet ses notifications de récupération, Resource Manager n’inclut pas de notification de récupération pour la transaction en question. Avec le modèle d’abandon présumé, le gestionnaire de ressources considère dans ce cas que la transaction préparée est abandonnée lorsqu’elle ne reçoit pas de notifications pour effectuer la récupération sur cette transaction.

 

 



