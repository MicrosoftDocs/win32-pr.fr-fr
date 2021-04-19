---
description: .
ms.assetid: 872c2a33-327e-41a8-81db-905c46673f13
title: Meilleures pratiques pour les performances d’activation/de désactivation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda45cb1ec7fb66b8afdcdebab7c92bdb071a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526965"
---
# <a name="best-practices-for-onoff-performance"></a>Meilleures pratiques pour les performances d’activation/de désactivation

## <a name="platform"></a>Plateforme

**Clients-** Windows Vista \| Windows 7  
**Serveurs-** Windows Server 2008 \| Windows server 2008 R2  

## <a name="description"></a>Description

Les États d’alimentation du système (ou S-États), tels que définis dans la spécification ACPI (Advanced Computer Power Interface), sont appelés de manière commune les États activés/désactivés dans la mesure où la transition d’État S la plus courante est l’activation et la désactivation d’un ordinateur. Les différentes transitions d’état activé/désactivé sur un système exécutant Windows Vista ou Windows 7 sont les mêmes démarrage, veille (ACPI S3), mise en veille prolongée (ACPI S4) et arrêt.

Une bonne performance au cours de ces transitions d’activation/de désactivation permet non seulement d’améliorer la qualité perçue d’un ordinateur, mais également d’affecter considérablement les modèles d’utilisation des ordinateurs quotidiens et la fiabilité du système. Les clients peuvent devenir frustrés par des systèmes dont le démarrage ou l’arrêt de l’ordinateur prend trop de temps. Les systèmes mobiles qui ont des transitions de veille et de veille prolongée peuvent inutilement épuiser la durée de vie de la batterie. Les durées d’arrêt plus longues peuvent également nuire à la fiabilité des systèmes mobiles. Par exemple, ils augmentent le risque d’une coupure d’alimentation inattendue.

Les extensions système telles que les pilotes, les applications et les services peuvent avoir un impact significatif sur les temps de transition activés/désactivés. Cette section décrit quelques-unes des meilleures pratiques que les développeurs d’applications et de services peuvent suivre pour éviter les retards lors du démarrage, de la mise en veille et de l’arrêt, et pour garantir une expérience utilisateur réactive après le démarrage et après reprise. Pour plus d’informations sur l’identification des problèmes de performances d’activation/de désactivation à l’aide de Windows performance Toolkit et pour mettre en œuvre les recommandations ci-dessous pour votre application ou service, reportez-vous aux livres blancs de la section « Liens vers d’autres ressources ».

## <a name="best-practices"></a>Bonnes pratiques

-   Utilisez Windows performance Toolkit pour mesurer les performances pendant toutes les transitions activées/désactivées.
-   Effectuez des tests de manière contrôlée et effectuez des comparaisons par rapport à une ligne de base valide :
    -   Obtenir une mesure de ligne de base sur un système avec le moins d’extensions système possible
    -   Ajouter des applications et des services l’un après l’autre
    -   Tester les régressions inacceptables dans les temps de transition activé/désactivé
-   Évitez d’utiliser du code managé pour les applications sur le chemin de démarrage critique.
-   Assurez-vous que toutes les applications répondent rapidement aux notifications d’arrêt ( \_ messages WM QUERYENDSESSION et WM \_ ENDSESSION).
-   Réduisez les retards dans le chemin d’arrêt des services et des applications en minimisant l’activité du processeur, du disque et du réseau en réponse aux notifications d’arrêt.
-   Évitez les retards dans le traitement de la notification de suspension ( \_ message WM POWERBROADCAST).
-   Répondez rapidement aux événements et réduisez l’utilisation du processeur, du disque et du réseau après la reprise.
-   Réduire la consommation des ressources d’application après le démarrage.
-   Ne démarrez pas les applications à partir de la clé RunOnce à chaque démarrage.
-   Convertissez tous les services non essentiels en démarrage à la demande ou déclenchez le démarrage pour rendre les ressources système disponibles au démarrage.
-   Évitez d’utiliser des groupes d’ordre de chargement pour exprimer des dépendances de service.
-   Assurez-vous que tous les services en cours d’exécution signalent cet État le plus rapidement possible au démarrage pour éviter de bloquer le gestionnaire de contrôle des services.
-   Évitez d’utiliser du code managé pour les services sur le chemin d’accès de démarrage.
-   N’autorisez pas les services à accepter de recevoir des notifications de pré-arrêt et d’arrêt (codes de contrôle de préarrêt et de contrôle de service du contrôle de service \_ \_ \_ \_ ) sauf si cela est absolument requis.
-   Assurez-vous que tous les services qui ont choisi de recevoir des notifications d’arrêt répondent rapidement au SCM.
-   Vérifiez que les services ne s’abonnent pas à la réception de notifications d’interruption, sauf si cela est absolument requis.
-   Assurez-vous que tous les services répondent rapidement pour reprendre les événements et réduire le temps d’utilisation du processeur, du disque et du réseau après la reprise.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   -   [Guide de solutions pour les transitions de Windows on/off](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Analyse des performances de transition on/off de Windows Vista](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Analyse des performances Windows](https://msdn.microsoft.com/performance/default.aspx)
-   [Documentation Windows performance Toolkit sur MSDN](/previous-versions/windows/desktop/xperf/windows-performance-analyzer--wpa-)
-   [Forum sur l’analyse des performances Windows](https://social.msdn.microsoft.com/Forums/wptk_v4/threads/)
-   [Suivi d’v nements pour Windows sur MSDN](../etw/event-tracing-portal.md)

 

 
