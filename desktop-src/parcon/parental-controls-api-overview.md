---
description: Vue d’ensemble de l’API des contrôles parentaux
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Vue d’ensemble de l’API des contrôles parentaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2dc1995db834aa206dea1a4f657565ac3e38b35766ca6a83ac495c4f1734af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712579"
---
# <a name="parental-controls-api-overview"></a>Vue d’ensemble de l’API des contrôles parentaux

Les API utilisées pour les contrôles parentaux exposent la stratégie et les paramètres de restrictions intégrés, ainsi que la fonctionnalité de journalisation.

## <a name="settings"></a>Paramètres

Deux API publiques sont fournies :

-   Une API de conformité minimale basée sur COM légère (appelée API de conformité) principalement pour les applications afin de déterminer si la journalisation doit être activée. En outre, des méthodes simples sont fournies pour :
    -   Récupération de l’état des restrictions pour les restrictions Web, limites de temps, restrictions de jeux et restrictions d’application.
    -   Récupération de l’ID du filtre de contenu Web actif.
    -   Déterminer si les éléments de l’interface utilisateur du fournisseur doivent être affichés, de manière cohérente avec le masquage par zone dans le cas d’une jointure à un domaine.
    -   Récupération de l’heure de la dernière modification d’un paramètre pour un utilisateur.
    -   La récupération des téléchargements de fichiers basés sur un navigateur ou un navigateur doit être bloquée pour un utilisateur, ainsi que la possibilité de demander à une URL d’être spécifiquement autorisée par le filtre de contenu Web pour cet utilisateur.
    -   Déterminer si un jeu donné est bloqué pour un utilisateur.
-   Windows L’API WMI (Management Instrumentation) accède à un espace de noms de contrôle parental pour l’accès en lecture et en écriture à tous les paramètres exposés. Le contrôle parental déploie un fournisseur WMI pour gérer les autorisations de lecture/écriture sur le magasin de paramètres sous-jacent, avec la mise en œuvre appropriée des privilèges pour les administrateurs et les utilisateurs contrôlés.

Les éditeurs de logiciels indépendants sont invités à utiliser l’API de conformité et l’API WMI si nécessaire pour contrôler les restrictions appropriées pour la sécurité des enfants en fonction de la fonctionnalité de l’application ou de la solution.

## <a name="logging"></a>Journalisation

-   Windows api de publication et de consommation d’événements standard sont utilisées pour la surveillance de l’activité des contrôles parentaux. le système de suivi et de création de rapports d’événements Windows Vista a amélioré les performances par rapport aux fonctionnalités de Suivi d’v nements pour Windows (ETW) précédentes. Le contrôle parental définit un canal unique pour ses données dans ETW.
-   Les éditeurs de logiciels indépendants sont invités à utiliser l’API de publication d’événements pour enregistrer l’activité des utilisateurs comme spécifié dans la section utilisation des API de contrôle parental.

 

 



