---
description: Une fois que vous avez inscrit une classe d’événements dans le catalogue COM+, vous pouvez ajouter des abonnés à la classe d’événements et des abonnements aux abonnés.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Inscription d’un abonnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03d5710fc792cad6282683d51df21d2ede10451
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393175"
---
# <a name="registering-a-subscription"></a>Inscription d’un abonnement

Une fois que vous avez inscrit une classe d’événements dans le catalogue COM+, vous pouvez ajouter des abonnés à la classe d’événements et des abonnements aux abonnés. Les abonnements peuvent s’abonner à une méthode unique ou à toutes les méthodes d’une interface. Pour recevoir des appels sur plus d’une méthode, mais pas sur chaque méthode, d’une interface, vous devez ajouter un abonnement pour chaque méthode à laquelle vous souhaitez recevoir un appel. L’outil d’administration Services de composants peut rechercher dans le catalogue COM+ des classes d’événements inscrites qui prennent en charge les interfaces implémentées par l’abonné et vous offre le choix de s’abonner. Choisissez le serveur de publication qui vous offre les événements souhaités.

Pour ajouter des abonnés au composant abonné, procédez comme suit :

1.  Après avoir créé une application COM+ et installé le composant d’abonné, cliquez avec le bouton droit sur le dossier **abonnements** pour activer l’Assistant Création d’un nouvel abonnement com+.

2.  Choisissez la classe d’événements à partir de laquelle vous souhaitez recevoir des événements.

3.  Entrez un nom pour l’abonnement.

4.  Activez l’abonnement.

5.  Cliquez sur **OK**.

Quand une application de serveur de publication souhaite déclencher un événement, le serveur de publication instancie l’objet de classe d’événements et appelle une méthode sur celui-ci. COM+ recherche tous les abonnés dans le catalogue COM+. Il crée l’objet d’abonné (directement, en file d’attente ou avec un moniker) et passe sur l’appel de méthode initialement effectué par le serveur de publication.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription d’une classe d’événements](registering-an-event-class.md)
</dt> </dl>

 

 



