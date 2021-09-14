---
description: Un composant COM configuré est généralement activé dans son propre contexte. autrement dit, COM+ référence les informations du catalogue de composants pour fournir tous les services configurés.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Application de l’activation dans le contexte par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41599f71dc37c37c1a9a574d274ca2858835e2df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291807"
---
# <a name="enforcing-activation-in-the-default-context"></a>Application de l’activation dans le contexte par défaut

Un composant COM configuré est généralement activé dans son propre contexte. autrement dit, COM+ référence les informations du catalogue du composant pour fournir tous les services configurés. Toutefois, vous pouvez choisir d’activer un composant configuré dans le contexte par défaut. Un composant COM de base (un composant inscrit qui n’a pas d’informations de catalogue COM+) est généralement activé dans le contexte par défaut.

L’activation d’un composant COM dans le contexte par défaut offre trois principaux avantages en matière de performances, comme suit :

-   Vous enregistrez des ressources système en limitant le nombre de contextes créés.
-   Vous augmentez les performances en limitant le nombre d’appels entre les contextes. Étant donné que les appels entre les contextes nécessitent un marshaling, il est beaucoup plus rapide pour un objet COM activé dans le contexte par défaut d’effectuer des appels à d’autres objets dans le contexte par défaut. Dans ce cas, les performances (des appels dans le même contexte) sont similaires à celles de l’appel d’une sous-routine.
-   Vous pouvez importer des applications COM plus anciennes dans COM+ et les exécuter sans problème. Par exemple, plusieurs applications COM plus anciennes peuvent être implémentées en supposant qu’elles étaient autorisées à passer des références d’objet au sein d’un cloisonnement sans marshaler les références. Ces applications COM ne fonctionnent pas lorsqu’elles sont importées dans COM+, car les références d’objet sont passées entre les limites de contexte. Toutefois, vous pouvez faire en sorte que ce type d’application COM s’exécute lors de l’importation si vous utilisez l’outil d’administration Services de composants pour marquer toutes les classes de l’application comme **devant être activées dans le contexte par défaut**.

Le principal inconvénient de l’activation d’un composant configuré dans le contexte par défaut est que COM+ ne fournit aucun des services configurés du composant. Il existe un compromis entre les performances améliorées et la possibilité d’utiliser les services COM+.

Par exemple, supposons qu’un composant COM ne nécessite pas de services COM+ (tels que les [transactions](com--transactions.md), [l’activation juste-à-temps](com--just-in-time-activation.md), les [événements](com--events.md), les [composants mis en file d’attente](com--queued-components.md), la [synchronisation](com--synchronization.md)ou le [regroupement d’objets](com--object-pooling.md)) et que le composant effectue un certain nombre d’appels à d’autres composants COM qui peuvent être activés dans le contexte par défaut. Dans ce cas, il serait judicieux d’activer le composant appelant dans le contexte par défaut.

Si le composant COM requiert des services COM+, il ne peut pas être marqué comme **devant être activé dans le contexte par défaut**. En outre, il n’existe aucun gain de performances réel si un objet COM activé dans le contexte par défaut effectue un certain nombre d’appels à des objets dans d’autres contextes. (Pour plus d’informations, consultez [contextes](com--contexts.md).)

**Pour appliquer l’activation dans le contexte par défaut**

1.  Dans le volet d’informations de l’outil d’administration Services de composants, cliquez avec le bouton droit sur le composant (situé dans le dossier **composants** de toute application com+ sélectionnée) que vous souhaitez activer dans le contexte par défaut, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **activation** .

3.  Activez la case à cocher **doit être activé dans le contexte par défaut**.

4.  Cliquez sur **OK**.

> [!Note]  
> Lorsque vous exécutez un composant configuré dans le contexte par défaut, COM+ n’active aucun des services configurés pour ce composant. Ces services sont à nouveau disponibles lorsque vous désactivez la case à cocher **doit être activé dans le contexte par défaut** et que vous exécutez ensuite le composant configuré dans son propre contexte.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts d’activation juste-à-temps de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Application de l’activation dans le contexte de l’appelant](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



