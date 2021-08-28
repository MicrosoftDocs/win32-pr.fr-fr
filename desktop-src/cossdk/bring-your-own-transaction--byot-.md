---
description: Transférer votre propre transaction (BYOT)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Transférer votre propre transaction (BYOT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b6177471d1c56956bba5fafd4f728a6295b29afcc6873495ddb690d2e59c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308662"
---
# <a name="bring-your-own-transaction-byot"></a>Transférer votre propre transaction (BYOT)

BYOT permet la création d’un composant avec ou pour hériter d’une transaction externe. Autrement dit, un composant qui n’a pas encore de transaction associée peut acquérir une transaction. Actuellement, les transactions MTS sont automatiques ; le fait qu’une instance de composant réside dans une transaction est déterminé au moment de la création. Les attributs transactionnels d’un composant et son créateur déterminent la transaction associée à une instance donnée. Dans tous les cas, MTS contrôle les durées de vie des transactions. COM+ l’étend pour permettre la définition d’une transaction DTC ou TIP préexistante arbitraire en tant que propriété de transaction du contexte d’un nouveau composant. Cela permet aux composants configurés d’être associés à des transactions dont les durées de vie sont contrôlées par une analyse de TP, un OTS ou un SGBD.

> [!Note]  
> Les transactions BYOT doivent être utilisées avec précaution. Dans certaines situations, elles peuvent entraîner la répartition d’une transaction sur plusieurs domaines de synchronisation, c’est-à-dire qu’ils autorisent le parallélisme avec une transaction, provoquant une condition de blocage. Les transactions automatiques, plutôt que les transactions BYOT, sont le modèle de programmation par défaut pour les rédacteurs de composants métier.

 

Les interfaces des transactions BYOT incluent l’interface [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) et l’interface [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) . L’interface **ICreateWithTransactionEx** crée un objet qui est inscrit dans une transaction manuelle. L’interface **ICreateWithTipTransactionEx** crée un objet qui est inscrit dans une transaction manuelle à l’aide du TIP (transaction Internet Protocol).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Héritage de transactions manuelles](inheriting-manual-transactions.md)
</dt> </dl>

 

 



