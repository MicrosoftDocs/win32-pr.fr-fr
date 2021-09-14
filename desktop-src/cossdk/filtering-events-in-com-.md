---
description: 'Les événements COM+ offrent deux moyens de contrôler les événements qui atteignent les abonnés : le filtrage du serveur de publication et le filtrage des paramètres.'
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: Filtrage des événements dans COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291799"
---
# <a name="filtering-events-in-com"></a>Filtrage des événements dans COM+

Les événements COM+ offrent deux moyens de contrôler les événements qui atteignent les abonnés : le filtrage du serveur de *publication* et le *filtrage des paramètres*.

## <a name="publisher-filtering"></a>Publisher Filtration

Publisher filtrage contrôle l’ordre et le déclenchement d’une méthode d’événement par un objet de [classe d’événements](the-com--event-class-object.md) . le filtrage Publisher permet au serveur de publication de déterminer les abonnés qui reçoivent un événement particulier.

Un exemple d’utilisation efficace du filtrage de l’éditeur est celui d’une bourse. La plupart des abonnés veulent savoir quand une nouvelle action est ajoutée. Toutefois, un grand nombre de ces mêmes abonnés peuvent ne pas souhaiter savoir à quel moment chaque cours d’action change. le filtrage Publisher fournit la granularité requise pour remettre efficacement les événements aux abonnés qui souhaitent ces informations.

Lorsqu’une méthode est appelée sur l’objet de classe d’événements instancié, elle collecte tous les filtres d’éditeur sur cette méthode. Le filtre force l’objet d’événement à déclencher la méthode d’événement sur un abonné spécifique. Le filtre détermine les abonnements à activer et leur ordre de déclenchement. Par exemple, le filtre peut lire la liste des abonnements et créer la commande en fonction de certains critères d’application, puis appeler les abonnés dans cet ordre.

pour obtenir des instructions détaillées sur la création d’un filtre de serveur de publication, consultez [création d’un filtre de Publisher](creating-a-publisher-filter.md).

## <a name="parameter-filtering"></a>Filtrage des paramètres

Contrairement au filtrage de l’éditeur, le service d’événements COM+ fournit un filtrage facultatif des paramètres de l’abonné pour chaque abonnement et chaque appel de méthode d’événement. Le filtrage des paramètres évalue la propriété de l’abonnement de l’abonnement par rapport aux paramètres de la méthode d’événement. Ce type de filtrage est utilisé sur la base de la méthode par abonnement et fournit un niveau de filtrage des abonnés au niveau de la source de l’événement. La chaîne des critères de filtre reconnaît les opérateurs relationnels pour la vérification de l’égalité (=, = =, !, ! =, ~, ~ =,  <>), les parenthèses imbriquées et les mots clés logiques **and**, **or** ou **not**.

Le filtrage des paramètres se produit après tout filtrage de l’éditeur et lorsque l’objet d’événement standard est déclenché pour un abonnement donné. Si le filtrage de l’éditeur est utilisé, le filtrage des paramètres se produit uniquement lorsque le filtre de l’éditeur appelle [**IFiringControl :: FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription). Pour cette raison, le filtrage de l’éditeur et le filtrage des paramètres peuvent se composer ensemble, mais le filtrage de l’éditeur est prioritaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Publication et diffusion d’événements dans COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Abonnements](subscriptions.md)
</dt> <dt>

[Objet de classe d’événements COM+](the-com--event-class-object.md)
</dt> <dt>

[Utilisation d’événements COM+ avec des composants en file d’attente COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



