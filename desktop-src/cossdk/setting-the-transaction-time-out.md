---
description: Vous pouvez définir manuellement le délai d’expiration pour les transactions à l’aide de l’outil d’administration Services de composants, ou vous pouvez configurer par programme le délai d’expiration à l’aide des interfaces d’administration COM+.
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: Définition de la Time-Out de transaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c770796cc3236f59e4a40e3d647e0a4bfafeb2cc8e06dbd9e248bcb1538867c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029409"
---
# <a name="setting-the-transaction-time-out"></a>Définition de la Time-Out de transaction

Vous pouvez définir manuellement le délai d’expiration pour les transactions à l’aide de l’outil d’administration Services de composants, ou vous pouvez configurer par programme le délai d’expiration à l’aide des [interfaces d’administration com+](com--administration-interfaces.md). Le délai d’attente peut être configuré au niveau de l’ordinateur local et également pour les composants individuels.

**Pour définir le délai d’expiration de la transaction pour l’ordinateur local à l’aide de l’outil d’administration Services de composants**

1.  Dans l’arborescence de la console, cliquez avec le bouton droit sur l’ordinateur local que vous souhaitez configurer, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés de l’ordinateur, cliquez sur l’onglet **options** .

3.  Sous **délai d’expiration** de la transaction, entrez le délai d’expiration de la transaction en secondes. Le délai d’attente par défaut est de 60 secondes.

4.  Cliquez sur **OK**.

**Pour définir le délai d’expiration de la transaction pour un composant à l’aide de l’outil d’administration Services de composants**

1.  Dans l’arborescence de la console, cliquez avec le bouton droit sur le composant que vous souhaitez configurer, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **transactions** .

3.  Activez la case à cocher **remplacer la valeur du délai d’expiration de la transaction globale**.

    > [!Note]  
    > Vous ne pouvez pas activer la case à cocher pour remplacer la valeur du délai d’attente de la transaction globale si la **prise en charge** de la transaction est définie sur **désactivé**, **non pris en charge** ou **pris en charge**.

     

4.  Sous **délai d’expiration** de la transaction, entrez le délai d’expiration de la transaction en secondes. Le délai d’attente par défaut est de 0 seconde, ce qui signifie que le composant ne provoquera jamais l’expiration du délai d’attente de la transaction.

5.  Cliquez sur **OK**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des transactions automatiques dans COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



