---
description: Vous pouvez écrire une application qui peut réagir aux événements à tout moment.
ms.assetid: 475dca47-b1e5-4362-ab00-9ab9383e92f9
ms.tgt_platform: multiple
title: Réception d’événements à tout moment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5559068e1e108c6f4185c31f8858a9e4169c50c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318869"
---
# <a name="receiving-events-at-all-times"></a>Réception d’événements à tout moment

Vous pouvez écrire une application qui peut réagir aux événements à tout moment. Par exemple, un administrateur peut vouloir recevoir un message électronique lorsque des mesures de performances spécifiques baissent sur les serveurs réseau. Dans ce cas, votre application doit être exécutée à tout moment. Toutefois, l’exécution d’une application en continu n’est pas une utilisation efficace des ressources système. Au lieu de cela, WMI vous permet de créer un consommateur d’événements permanent. Les consommateurs d’événements permanents doivent répondre à des exigences de sécurité particulières. Pour plus d’informations, consultez [sécurisation des événements WMI](securing-wmi-events.md).

Un consommateur d’événements permanent reçoit des événements jusqu’à ce que son inscription soit explicitement annulée.

Un consommateur d’événements permanent est une combinaison des classes WMI, des filtres et des objets COM qui résident sur votre système :

-   Objet COM appelé consommateur physique. WMI fournit plusieurs consommateurs permanents standard. Par exemple, le consommateur d’événements active script [exécute un script lorsqu’un événement se produit](running-a-script-based-on-an-event.md).
-   Nouvelle classe de consommateur permanente.
-   Une instance de la classe de consommateur permanente appelée consommateur logique.
-   Filtre qui contient la requête pour les événements.
-   Liaison entre le consommateur et le filtre.

Les propriétés d’un consommateur d’événements logiques spécifient les actions à effectuer lors de la notification d’un événement, mais ne définissent pas les requêtes d’événement auxquelles elles sont associées. Lorsqu’il est signalé, WMI charge automatiquement l’objet COM qui représente le consommateur d’événements permanent dans la mémoire active. En général, cela se produit au démarrage ou en réponse à un événement de déclenchement. Une fois activé, le consommateur d’événements permanent agit comme un consommateur d’événements normal, mais reste jusqu’à ce qu’il soit spécifiquement déchargé par le système d’exploitation.

Vous pouvez écrire votre propre consommateur d’événements permanent ou utiliser les [classes de consommateur standard](standard-consumer-classes.md)préinstallées WMI, telles que [**ActiveScriptEventConsumer**](activescripteventconsumer.md). Pour plus d’informations, consultez [classes de consommateur standard](standard-consumer-classes.md), [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md)et [surveillance des événements](monitoring-events.md).

La procédure suivante décrit comment créer votre propre consommateur d’événements permanent.

**Pour créer votre propre consommateur d’événements permanent**

1.  Déterminez le type d’événement que vous souhaitez recevoir.

    WMI prend en charge les événements intrinsèques et extrinsèques. Un événement intrinsèque est un événement prédéfini par WMI, alors qu’un événement extrinsèque est un événement défini par un fournisseur tiers. Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).

2.  [Implémentez un consommateur physique](implementing-a-physical-consumer.md).

    La principale différence entre une application de gestion et un [*consommateur physique*](gloss-p.md) est qu’un utilisateur charge et décharge une application de gestion, alors que WMI charge et décharge un consommateur physique. La majeure partie de votre code doit être dans le consommateur physique.

    > [!Note]  
    > Cette étape est tout d’abord décrite dans la procédure pour faciliter l’explication. En termes de codage, vous devez en fait créer le consommateur physique en dernier. De cette façon, vous pouvez disposer vos paramètres et votre logique pour votre fournisseur d’événements permanent avant de commencer le codage long. Toutefois, il n’existe aucune restriction pour l’écriture du consommateur physique en premier.

     

3.  [Créez une classe de consommateur décrivant le consommateur physique](creating-a-new-permanent-event-consumer-class.md).

    Comme n’importe quelle classe, la classe Consumer décrit les paramètres généraux d’un consommateur d’événements permanent à WMI.

4.  [Créez une instance de la classe de consommateur](creating-a-logical-consumer.md).

    Comme toute autre classe WMI, vous devez créer une instance de la classe de consommateur si vous souhaitez implémenter la classe. Une instance d’une classe de consommateur est également appelée [*consommateur logique*](gloss-l.md). Le consommateur logique représente le consommateur physique de WMI.

5.  [Créez un filtre d’événements](creating-an-event-filter.md).

    Les requêtes d’événement qui activent les consommateurs d’événements permanents sont appelées [*filtres d’événements*](gloss-e.md). Un filtre d’événement unique peut être associé à plusieurs consommateurs d’événements logiques. En outre, plusieurs filtres d’événements peuvent être associés à un seul consommateur d’événements logiques. Le filtre est une instance de [**\_ \_ EventFilter**](--eventfilter.md).

    Un événement de journal NT est généré en cas d’échec de la requête d’un consommateur d’événements permanent. La source de l’événement est WinMgmt, l’ID d’événement est 10 et le type d’événement est Error.

6.  [Liez le filtre d’événement au consommateur logique](binding-an-event-filter-with-a-logical-consumer.md).

    En liant le filtre d’événement au consommateur logique, vous indiquez à WMI le filtre d’événement qui appartient à ce consommateur logique. Les consommateurs d’événements logiques et les filtres d’événements sont liés par une instance de classe d’association de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md). Lors de la réception d’un événement qui correspond à une requête d’événement décrite dans un filtre d’événements, WMI recherche le consommateur d’événements logiques associé en examinant l’instance de la classe d’association. Une fois l’instance de consommateur d’événements logique localisée, WMI utilise une instance de la classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) pour rechercher et exécuter le consommateur d’événements physique associé à cette instance.

7.  [Écriture d’un fournisseur de consommateur d’événements](writing-an-event-consumer-provider.md).

    Le fournisseur de consommateur d’événements est un objet COM qui localise le consommateur physique pour WMI.

 

 



