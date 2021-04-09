---
description: Transactions et activation JIT COM+
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Transactions et activation JIT COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281691ebc9c8d5c654ea6ff0c3035d7e285f62c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861550"
---
# <a name="transactions-and-com-jit-activation"></a>Transactions et activation JIT COM+

L’activation JIT COM+ est étroitement liée aux transactions automatiques. Quand vous configurez un composant pour qu’il nécessite une transaction ou nécessite une nouvelle transaction, l’activation JIT est automatiquement activée. Les deux fonctionnalités fonctionnent naturellement conjointement. Les composants transactionnels activés par le JIT partagent les caractéristiques suivantes :

-   Abandon. Vous ne pouvez pas conserver l’État qui violerait l’isolation des transactions, ni conserver l’État qui serait perdu lors de la désactivation d’un objet.

-   Utilisation rapide. Le modèle d’utilisation canonique d’un objet effectuant un travail dans une transaction automatique consiste à effectuer une petite unité de travail, voter et quitter.

    > [!Note]  
    > La façon dont vous votez dans les transactions COM+ et l’état de signal pour l’activation juste-à-temps est également étroitement liée. Pour plus d’informations, consultez [définition du bit terminé](setting-the-done-bit.md).

     

-   Utilisation répétée. Lorsque le travail transactionnel est correctement divisé, les clients utilisent les mêmes objets pour effectuer des fragments de travail atomique.

-   Désactivé lors de la validation ou de l’abandon. Dans COM+, tous les objets de la limite de transaction sont désactivés lorsque la transaction est validée ou abandonnée.

Conjointement avec les composants transactionnels COM+, l’activation JIT fait office d’amélioration importante des performances en gardant le canal ouvert en tant que clients qui contiennent des références à long terme aux objets transactionnels. Pour d’autres améliorations, vous pouvez choisir de regrouper les objets transactionnels afin de réutiliser les ressources qu’ils contiennent, d’accélérer la réactivation des objets et de gérer de près la façon dont vous utilisez les ressources mémoire pour les objets donnés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts d’activation juste-à-temps de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Activation de l’activation JIT pour un composant](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Mise en pool d’objets et activation JIT COM+](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



