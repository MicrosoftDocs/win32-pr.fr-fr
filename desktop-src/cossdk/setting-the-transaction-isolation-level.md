---
description: Vous pouvez définir manuellement le niveau d’isolation de la transaction des composants à l’aide de l’outil d’administration Services de composants, ou vous pouvez configurer par programme le niveau d’isolation des transactions pour un composant à l’aide des interfaces d’administration COM+.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Définition du niveau d’isolation des transactions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b0447af2591c4f4b3e8e76c017157c02908367
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310965"
---
# <a name="setting-the-transaction-isolation-level"></a>Définition du niveau d’isolation des transactions

Vous pouvez définir manuellement le niveau d’isolation de la transaction des composants à l’aide de l’outil d’administration Services de composants, ou vous pouvez configurer par programme le niveau d’isolation des transactions pour un composant à l’aide des [interfaces d’administration com+](com--administration-interfaces.md).

Pour plus d’informations sur les niveaux d’isolation des transactions, consultez [Configuration des niveaux d’isolation des transactions](configuring-transaction-isolation-levels.md).

**Pour définir le niveau d’isolation de la transaction à l’aide de l’outil d’administration Services de composants**

1.  Dans l’arborescence de la console, cliquez avec le bouton droit sur le composant que vous souhaitez configurer, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **transactions** .

3.  Sous **niveau d’isolement** de la transaction, sélectionnez la valeur de votre choix dans la zone de liste déroulante. La valeur par défaut de tous les composants est **sérialisée**.

    > [!Note]  
    > Si l’option **désactivé** ou **non pris en charge** est sélectionnée sous **prise en charge des transactions**, vous ne pouvez pas définir le niveau d’isolation de la transaction.

     

4.  Cliquez sur **OK**.

Vous devez répéter cette procédure pour chaque composant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration des niveaux d’isolation des transactions](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



