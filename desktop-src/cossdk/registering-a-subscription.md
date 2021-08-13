---
description: Une fois que vous avez inscrit une classe d’événements dans le catalogue COM+, vous pouvez ajouter des abonnés à la classe d’événements et des abonnements aux abonnés.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Inscription d’un abonnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f152834c805bd905019d2afe0e353c0a962452c32ef144cc3c3d445b59fbbed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547109"
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

 

 



