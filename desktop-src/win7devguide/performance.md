---
title: performances (Guide du développeur Windows 7)
description: Windows 7 maximise l’efficacité et l’évolutivité de l’énergie matérielle tout en conservant des performances élevées.
ms.assetid: db48aa8f-749e-4a56-8a91-ac9b81d6e8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752f66e80265bf7d6b3ea26e7baabdc6550ce921
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231018"
---
# <a name="performance-windows-7-developer-guide"></a>performances (Guide du développeur Windows 7)

Windows 7 maximise l’efficacité et l’évolutivité de l’énergie matérielle tout en conservant des performances élevées. L’efficacité énergétique est améliorée grâce à une activité en arrière-plan réduite et une nouvelle prise en charge du déclencheur à partir de services système. Windows 7 offre également des améliorations dans le noyau Windows qui permettent aux applications et aux services de s’adapter efficacement entre les plateformes. les performances de nombreuses fonctionnalités et api sont améliorées dans Windows 7 par rapport à Windows Vista. Par exemple, les performances du pilote sur les serveurs sont optimisées par les nouvelles API de topologie en mode utilisateur et en mode noyau. Le rendu graphique est beaucoup plus lisse et plus rapide. Les performances d’accessibilité sont également beaucoup plus rapides qu’auparavant.

## <a name="building-power-efficient-applications"></a>Génération d’applications Power-Efficient

La création d’applications économes en énergie qui tirent parti des dernières technologies de gestion de l’alimentation est un défi majeur auquel les développeurs sont confrontés aujourd’hui. En règle générale, les fabricants de processeurs et de périphériques sont en mesure de mesurer et d’évaluer leurs dernières offres. Toutefois, une seule application peut facilement empêcher la dernière génération de matériel de réaliser son potentiel d’efficacité énergétique. Par exemple, une application unique qui augmente la résolution de la minuterie de la plateforme peut réduire la durée de vie de la batterie de 10%.

Le fonctionnement étendu sur batterie et l’utilisation de technologies économes en énergie sont des exigences essentielles pour les développeurs actuels. Windows 7 réduit considérablement le nombre d’activités exécutées par le système d’exploitation et qui empêchent l’utilisation de modes d’économie d’énergie. Il prend également en charge le déclencheur-démarrage des services système pour permettre aux processeurs de devenir inactifs plus souvent et de rester inactifs, ce qui réduit la consommation d’énergie. en outre, les Windows 7 tirent parti du dernier matériel économe en énergie, y compris les cartes réseau, les dispositifs de stockage et les cartes graphiques.

Windows 7 fournit l’infrastructure et les outils qui permettent aux développeurs de déterminer facilement l’impact énergétique de leurs applications. Un ensemble de rappels d’événements permet aux applications de réduire leur activité lorsque le système est alimenté par batterie et s’adapte automatiquement lorsque le système est alimenté en *secteur* . pour les applications qui impliquent un processus ou un service en arrière-plan, Windows 7 propose une nouvelle infrastructure qui permet d’activer automatiquement les tâches en arrière-plan, le cas échéant, afin d’optimiser l’efficacité énergétique. (consultez [WHDC Performance Central](https://www.microsoft.com/whdc/system/sysperf/default.mspx) and [Power Management in Windows 7 Overview](https://www.climatesaverscomputing.org/wordpress/wp-content/uploads/2011/06/Power_Management_in_Windows_7_Overview.pdf).)

## <a name="service-control-manager"></a>Gestionnaire de contrôle des services

le gestionnaire de contrôle Windows des 7Service a été étendu de façon à ce qu’un service puisse être démarré et arrêté automatiquement lorsqu’un événement système spécifique, ou un déclencheur, se produit sur le système. Les fonctionnalités de démarrage du déclencheur éliminent la nécessité de démarrer automatiquement les services au démarrage de l’ordinateur, puis d’interroger ou d’attendre qu’un événement se produise, par exemple l’arrivée d’un appareil. Les événements de déclencheur courants pour les services sont les suivants :

-   Arrivée de l’interface de la classe de l’appareil : démarrez un service uniquement lorsqu’un certain type d’appareil est présent ou attaché sur le système.
-   jonction de domaine : démarrez un service uniquement si le système est joint à un domaine Windows.
-   Modification de la stratégie de groupe : démarrez un service automatiquement lorsque les stratégies de groupe sont actualisées sur le système.
-   Arrivée de l’adresse IP : démarrez un service uniquement lorsque le système est connecté au réseau.

les développeurs de logiciels peuvent utiliser les types de déclencheurs prédéfinis pour Windows 7 et les options de configuration pour activer la fonctionnalité de démarrage du déclencheur. le Windows 7SCM expose un nouvel ensemble d’api qui permet à un service de s’inscrire à des événements de déclencheur personnalisés spécifiques. (Voir [Gestionnaire de contrôle des services](../services/service-control-manager.md).)

## <a name="windows-troubleshooting-platform"></a>Plateforme de résolution des problèmes Windows

Windows 7 offre une plateforme de dépannage complète et extensible qui utilise un mécanisme basé sur PowerShell pour dépanner et résoudre les problèmes. Les principaux composants de la plateforme de résolution des problèmes incluent un package de résolution des problèmes, un moteur de dépannage et un assistant de dépannage. Le Pack de résolution des problèmes est un ensemble de scripts PowerShell et de métadonnées pertinentes. Le moteur de résolution des problèmes lance un Runtime PowerShell pour exécuter un pack de résolution des problèmes et expose un ensemble d’interfaces pour contrôler l’exécution du Pack de résolution des problèmes.

L’Assistant résolution des problèmes fournit une expérience cohérente entre les packs de résolution des problèmes et communique avec le moteur de résolution des problèmes pour dépanner et résoudre les problèmes spécifiés dans un pack de résolution des problèmes. L’exécution d’un pack de résolution des problèmes peut également être contrôlée via un ensemble de *applets* PowerShell.

la plateforme de résolution des problèmes s’intègre parfaitement au centre de solutions Windows 7PC, ce qui permet à d’autres applications d’exécuter des diagnostics de la même manière dans le cadre de leur régime de gestion des ordinateurs. la plateforme de résolution des problèmes est configurable par les professionnels de l’informatique par le biais de *stratégie de groupe* pour une utilisation dans l’entreprise, et un Windows de résolution des problèmes Shared Computer Toolkit qui permet aux développeurs de créer des packs de résolution des problèmes est également disponible. (voir [Windows plateforme de résolution des problèmes](/previous-versions/windows/desktop/wintt/windows-troubleshooting-toolkit-portal).)

![interface utilisateur de la plateforme de dépannage](images/windows7-devguide-troubleshoot.jpg)

la plateforme de résolution des problèmes s’intègre parfaitement au centre de solutions Windows 7PC

 

 
