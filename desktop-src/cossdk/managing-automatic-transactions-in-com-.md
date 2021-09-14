---
description: dans le modèle de programmation COM+, vous pouvez concevoir vos composants pour faire ce qu’ils font le mieux&\# 8212, en activant la logique métier ou en établissant une connexion de base de données&\# 8212 ; et s’appuient sur l’infrastructure de traitement des transactions de Microsoft Windows pour automatiser les transactions.
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: Gestion des transactions automatiques dans COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310993"
---
# <a name="managing-automatic-transactions-in-com"></a>Gestion des transactions automatiques dans COM+

dans le modèle de programmation COM+, vous pouvez concevoir vos composants pour faire ce qu’ils font le mieux (en activant la logique métier ou en établissant une connexion de base de données) et s’appuyer sur l’infrastructure de traitement des transactions de Microsoft Windows pour automatiser les transactions.

## <a name="starting-a-transaction"></a>Démarrage d'une transaction

COM+ commence automatiquement une transaction lorsqu’il rencontre l’une des conditions suivantes :

-   Lorsqu’un client non transactionnel appelle un composant qui requiert une transaction ou nécessite une nouvelle transaction.
-   Lorsqu’un client transactionnel appelle un composant qui requiert une nouvelle transaction.

Si COM+ détermine qu’un objet doit avoir une nouvelle transaction, il commence par commencer la transaction, puis place l’objet dans celui-ci. Le processus comporte les étapes suivantes :

1.  COM+ crée un objet de contexte, définit les attributs d' [activation](com--just-in-time-activation.md) et de [synchronisation](com--synchronization.md) JIT sur obligatoire, puis définit les [indicateurs consistent et Done](consistent-and-done-flags.md) sur true et false, respectivement.
2.  COM+ communique avec le Distributed Transaction Coordinator (DTC) pour commencer une transaction. Le DTC coordonne la transaction physique.
3.  Le DTC génère un identificateur de transaction et le retourne à COM+. L’identificateur de transaction établit une limite de transaction. Tous les objets participant à la transaction partagent le même identificateur.
4.  Lorsque le client crée l’objet, COM+ l’active dans la limite de la transaction.

## <a name="ending-a-transaction"></a>Fin d’une transaction

COM+ met fin à une transaction automatique en la validant ou en l’abandonnant lorsque l’une des conditions suivantes se produit :

-   L’objet racine de la transaction termine son travail et COM+ le libère. Après la désactivation de l’objet racine, la transaction tente de valider.
-   Le client libère l’objet racine. Sans référence, l’objet racine est désactivé et la transaction tente de valider.
-   La transaction dépasse son seuil de délai d’expiration. La transaction est automatiquement abandonnée si elle n’est pas validée dans le délai d’expiration de la transaction, ce qui désactive tous les objets associés à la transaction. Le délai d’expiration de la transaction par défaut est de 60 secondes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Indicateurs cohérents et terminés](consistent-and-done-flags.md)
</dt> <dt>

[Accélération des transactions en avertissant l’objet racine](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[Fin d’une transaction automatique en appelant SetComplete](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 



