---
description: Activation de l’activation JIT pour un composant
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Activation de l’activation JIT pour un composant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f61cc5c79270a926bb50e3408766df63f4484c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095430"
---
# <a name="enabling-jit-activation-for-a-component"></a>Activation de l’activation JIT pour un composant

Vous devez configurer un composant qui doit être activé juste-à-temps uniquement lorsqu’il est écrit correctement pour prendre en charge le service d’activation juste-à-temps (JIT) COM+. Si un composant est désactivé entre les appels de méthode, il perd tout état associé. Étant donné le comportement par défaut de l’activation JIT, il est peu probable que cela se produise quand vous ne le pensez pas, mais vous devez être conscient des exigences d’un composant avant de modifier sa configuration et des attentes des clients qui appellent le composant.

> [!Note]  
> Si un composant est configuré pour exiger des transactions, le service d’activation JIT COM+ est activé automatiquement. Vous ne pouvez pas le désactiver dans ce cas. Pour plus d’informations, consultez [Configuration des transactions](configuring-transactions.md).

 

Lorsque vous activez l’activation JIT pour un composant, son attribut de synchronisation est défini sur obligatoire pour ce composant. Dans ce cas, vous ne pouvez pas modifier le paramètre de synchronisation. Pour plus d’informations, consultez [dépendances de synchronisation](synchronization-dependencies.md).

**Pour activer l’activation JIT**

1.  Dans le volet d’informations de l’outil d’administration Services de composants, cliquez avec le bouton droit sur le composant que vous souhaitez configurer, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **activation** .

3.  Pour activer l’activation JIT pour le composant, activez la case à cocher **activer l’activation juste-à-temps** .

4.  Cliquez sur **OK**.

Lorsque vous avez activé l’activation JIT pour un composant, vous avez la possibilité d’activer la fonctionnalité de saisie semi-automatique pour toute méthode exposée par ce composant. Pour plus d’informations, consultez [activation de la saisie semi-automatique pour une méthode](enabling-auto-done-for-a-method.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Activation de la saisie semi-automatique pour une méthode](enabling-auto-done-for-a-method.md)
</dt> <dt>

[Définition du bit terminé](setting-the-done-bit.md)
</dt> </dl>

 

 



