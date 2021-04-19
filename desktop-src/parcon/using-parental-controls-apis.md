---
description: Utilisation des API de contrôle parental
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: Utilisation des API de contrôle parental
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534498"
---
# <a name="using-parental-controls-apis"></a>Utilisation des API de contrôle parental

## <a name="api-selection"></a>Sélection de l’API

Comme indiqué dans la section vue d’ensemble, le développement implique l’utilisation de trois API au maximum :

-   Accès aux paramètres de base : l’API COM de conformité minimale des contrôles parentaux (API de conformité) est définie dans Wpcapi. h pour un accès simple à un sous-ensemble d’États de contrôle parental.
-   Accès en écriture/lecture des paramètres complets : l’utilisation d’un petit sous-ensemble de l’API COM WMI pour l’accès complet n’est requise que si l’ISV doit modifier les paramètres. L’ajout d’un lien d’extensibilité de l’interface utilisateur, le remplacement du filtre de contenu Web ou des ajouts aux listes d’exemptions d’application HTTP à l’ordinateur ou de filtrage d’URL sont principalement les raisons d’utiliser l’API. Comme l’utilisation de l’espace de noms de contrôle parental WMI fournit un accès brut au magasin de paramètres sous-jacent, les éditeurs de logiciels indépendants doivent procéder avec prudence pour interpréter l’état des paramètres individuels qui peuvent en fait avoir des dépendances de passerelle sur d’autres paramètres. Par conséquent, il est recommandé d’utiliser l’API de conformité pour lire l’état de toutes les valeurs exposées par cette API.
-   Journalisation : l’API du système de rapports et de suivi d’événements de Windows Vista (également appelée ETW) pour la publication des événements d’activité dans les journaux de contrôle parental, conjointement avec les descripteurs d’événements et les énumérations de tableau définies dans WpcEvent. h.

Toutes les API peuvent être appelées en tant qu’utilisateur standard. Pour la journalisation, tout utilisateur peut consigner des événements de journal. L’appel de pour extraire ou modifier les paramètres d’un autre utilisateur échoue si l’appelant ne dispose pas de privilèges d’administrateur. En d’autres termes, un utilisateur standard peut uniquement accéder à ses propres paramètres et uniquement pour la lecture.

Les paramètres et l’utilisation de l’API de journalisation sont décrits plus en détail dans les sections suivantes :

-   [Utilisation des API de paramètres de contrôle parental](using-parental-controls-settings-apis.md)
-   [Utilisation des API de journalisation pour les contrôles parentaux](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a>Environnement de développement

Le développement pour les contrôles parentaux requiert l’accès à trois fichiers d’en-tête : WPC. h, WpcApi. h et WpcEvent. h. WPC. h est un collecteur qui inclut les paramètres API de conformité publique et en-têtes d’événement. par conséquent, il suffit d’inclure WPC. h dans le code de l’application.

Les autorisations de lecture/écriture sur l’API WMI sont spécifiées par le fichier Wpcsprov. mof. Ce fichier est installé dans le sous-répertoire WBEM sous le répertoire Windows system32.

Le kit de développement logiciel (SDK) Microsoft Windows contient un exemple de code pour renforcer l’exemple de code présenté ici et fournir des outils de ligne de commande simples pour l’exploration des API ou les tests d’intégration.

 

 



