---
description: Suivi COM+
ms.assetid: ad3bdeb5-f303-411a-abfb-ccde3f9a86b9
title: Suivi COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069d910f0c559776125342b861e71566fb20f45231f960b1c1dcb18262171926
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029489"
---
# <a name="com-tracking"></a>Suivi COM+

Le service de suivi COM+ vous permet de créer vos propres programmes d’administration et de diagnostic qui assurent le suivi de l’État et des performances des applications COM+ en cours d’exécution. Le suivi COM+ fournit des informations statistiques sur l’utilisation des applications COM+, ainsi que des informations d’État, par exemple si une instance d’application serveur COM+ est suspendue ou a été recyclée. Les outils peuvent utiliser des informations de suivi dans le cadre de la surveillance du diagnostic ou à des fins d’affichage. Par exemple, l’outil d’administration Services de composants utilise le suivi COM+ pour afficher l’état des instances de l’application COM+ dans les dossiers applications COM+ et processus en cours d’exécution.

Le suivi COM+ calcule et met à jour périodiquement un ensemble de métriques couramment utilisées, ce qui rend ces informations disponibles aux programmes qui en ont besoin. Elle est similaire à l’instrumentation COM+ dans le sens où les deux services collectent automatiquement des données à partir d’instances d’application COM+ et mettent ces données à la disposition des consommateurs. Toutefois, il existe des différences importantes entre ces services, à la fois dans la fonctionnalité fournie et dans l’utilisation classique. Le tableau suivant résume ces différences.



| Instrumentation COM+                                                                                                                                                                                                   | Suivi COM+                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Données affinées. Le service d’instrumentation COM+ notifie les abonnés inscrits d’événements discrets individuels (par exemple, méthode appelée, objet détruit) qui se produisent dans une instance d’application COM+.<br/> | Données agrégées. Le suivi COM+ calcule et met régulièrement à jour les métriques couramment utilisées pour l’État et les performances des instances de l’application COM+.<br/> |
| En général, les abonnés aux événements calculent les métriques, à l’aide d’algorithmes et de stratégies ad hoc.<br/>                                                                                                           | Les métriques sont calculées automatiquement par le service de suivi COM+. Tous les consommateurs obtiennent les mêmes données, sans prise en charge des mesures personnalisées.<br/>                |
| Après l’inscription d’un abonnement, le consommateur ne reçoit pas d’informations sur une instance d’application COM+ jusqu’à ce qu’un événement se produise.<br/>                                                                    | Les données de suivi de toutes les instances d’application COM+ peuvent être récupérées à tout moment.<br/>                                                                         |
| Prend uniquement en charge un mécanisme d’abonnement basé sur les événements COM+ pour les consommateurs.<br/>                                                                                                                                     | Prend en charge à la fois un mécanisme d’abonnement basé sur les événements COM+ et l’interrogation d’une interface de serveur local COM.<br/>                                                  |
| Exemples                                                                                                                                                                                                               |                                                                                                                                                                   |
| Notifications lorsqu’une méthode est appelée ou est retournée.<br/>                                                                                                                                                           | Temps de réponse moyen des appels, nombre d’appels de méthode ayant réussi ou échoué au cours d’une période récente, nombre d’objets actuellement dans un appel de méthode.<br/>     |
| Notifications lorsqu’un objet est ajouté ou obtenu à partir du pool d’objets.<br/>                                                                                                                                  | Nombre d’objets dans le pool, nombre total d’objets.<br/>                                                                                                |
| Notifications lors du démarrage, de la suspension ou du recyclage d’une application serveur COM+.<br/>                                                                                                                               | État du processus de l’application serveur COM+ (par exemple, s’il est suspendu ou recyclé).<br/>                                                         |
| Notifications des événements de début, de préparation, d’abandon et de validation de la transaction.<br/>                                                                                                                                      | Aucun équivalent.<br/>                                                                                                                                         |
| Notifications de tentatives d’authentification de la méthode réussie et ayant échoué.<br/>                                                                                                                           | Aucun équivalent.<br/>                                                                                                                                         |



 

Bien que le suivi COM+ soit plus limité en termes d’étendue des données et de flexibilité pour le calcul des mesures, les mesures qu’il fournit doivent être suffisantes pour un large éventail de programmes d’administration et de diagnostic. Dans la mesure du possible, le suivi COM+ peut simplifier la conception de ces programmes. En outre, l’utilisation du suivi COM+ dans les systèmes de production peut avoir un impact nettement inférieur sur les performances, ce qui le rend plus approprié pour les outils de surveillance en temps réel.

## <a name="how-com-tracking-collects-data"></a>Comment le suivi COM+ collecte des données

Lors du démarrage d’un processus d’application serveur COM+, COM+ enregistre le processus auprès du *serveur de suivi*, un composant de l’application système. Les composants des applications et des services de la bibliothèque COM+ sans les contextes de composants (SWC) prennent également en charge le suivi. Lorsqu’un composant de bibliothèque ou un contexte SWC est créé dans un processus, COM+ inscrit le processus auprès du serveur de suivi s’il n’a pas déjà été inscrit.

COM+ met à jour les statistiques d’un processus suivi lorsque certains événements se produisent dans le processus, tels que la création d’un objet ou l’achèvement d’un appel de méthode. Les données mises à jour sont régulièrement envoyées au serveur de suivi, auquel cas elles deviennent disponibles pour les consommateurs. Le serveur de suivi est également chargé de calculer certaines des métriques utilisées par les fonctionnalités de surveillance du recyclage et des blocages des applications COM+. Ces données sont également disponibles pour les consommateurs.

Les données de suivi sont organisées en fonction du processus qui a généré les données. Les données au niveau des applications ou des composants COM+ individuels dans le processus sont également disponibles pour les consommateurs qui ont besoin de ces informations.

## <a name="events-versus-polling"></a>Événements et interrogation

Le suivi COM+ prend en charge deux mécanismes permettant à un consommateur d’obtenir des données de suivi à partir du serveur Tracker, d’un mécanisme d’abonnement basé sur les événements COM+ et d’une interface de serveur local COM.

Les programmes qui doivent être régulièrement avertis avec des données de suivi mises à jour peuvent inscrire un abonnement pour l’interface d’événement [**IComTrackingInfoEvents**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfoevents) . Environ toutes les trois secondes, le serveur de suivi appelle la méthode [**IComTrackingInfoEvents :: OnNewTrackingInfo**](/windows/desktop/api/ComSvcs/nf-comsvcs-icomtrackinginfoevents-onnewtrackinginfo) de chaque abonné, en envoyant les données de suivi les plus récentes sous la forme d’un objet de collection. Cet objet implémente l’interface [**IComTrackingInfoCollection**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfocollection) , et les abonnés peuvent parcourir cette collection pour trouver les données qui les intéressent.

Pour diverses raisons, il peut être plus judicieux pour un programme d’interroger le serveur de suivi des données. Par exemple, un outil de surveillance peut nécessiter des mises à jour nettement moins fréquentes qu’un programme qui affiche l’État dans une interface utilisateur. En outre, un programme ne peut utiliser qu’une petite partie des données de suivi disponibles pour le système (par exemple, un outil peut uniquement surveiller les performances des instances d’une seule application COM+). Le modèle d’abonnement envoie à chaque abonné les données de suivi de toutes les applications COM+ dans chaque notification, et il est de la responsabilité de l’abonné de rechercher les données dont il a besoin. Enfin, les événements COM+ constituent un mécanisme de notification d’événements le mieux adapté. Les services de remise de messages fiables ne sont pas fournis, et il n’existe aucun moyen pour un abonné de détecter que le serveur de suivi n’a pas réussi à lui envoyer une notification.

Un programme qui a besoin d’un contrôle accru sur sa récupération des données de suivi peut utiliser l’interface [**IGetAppTrackerData**](/windows/desktop/api/ComSvcs/nn-comsvcs-igetapptrackerdata) du serveur tracker.

 

 




