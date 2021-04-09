---
title: Guides du développeur de l’infrastructure de ruban Windows
description: Les rubriques contenues dans cette section décrivent des aspects spécifiques de l’infrastructure du ruban Windows.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Ruban Windows, infrastructure
- Ruban, infrastructure
- Ruban Windows, guides pour les développeurs
- Ruban, guides pour les développeurs
- Guide du développeur pour le ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b6e88045efdd31384d99370fdd9bb9cb264598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102156"
---
# <a name="windows-ribbon-framework-developer-guides"></a>Guides du développeur de l’infrastructure de ruban Windows

Les rubriques contenues dans cette section décrivent des aspects spécifiques de l’infrastructure du ruban Windows.

## <a name="basics"></a>Concepts de base

[Création d’une application de ruban](windowsribbon-stepbystep.md)

Pour que l’infrastructure du ruban Windows utilise le fichier de balisage du ruban, le fichier de balisage doit être compilé dans un fichier de ressources au format binaire. Un compilateur de balisage du ruban dédié, le compilateur de commandes d’interface utilisateur (UICC), est inclus dans le kit de développement logiciel (SDK) Microsoft Windows (7,0 ou version ultérieure) à cet effet. En plus de compiler la version binaire du balisage du ruban, UICC génère un fichier d’en-tête de définition d’ID (. h) qui expose tous les éléments de balisage à l’application hôte du ruban et un fichier de ressources (. RC) qui est utilisé pour lier des ressources d’image et de chaîne à l’application hôte au moment de la génération.

[Migration vers l’infrastructure de ruban Windows](ribbon-migration.md)

Une application qui s’appuie sur des menus, des barres d’outils et des boîtes de dialogue traditionnels peut être migrée vers l’interface utilisateur riche, dynamique et basée sur le contexte du système de commandes de l’infrastructure du ruban. Il s’agit d’un moyen simple et efficace de moderniser et de revitaliser l’application tout en améliorant également l’accessibilité, la convivialité et la détectabilité de ses fonctionnalités.

[Fonctionnement des commandes et des contrôles](windowsribbon-commandscontrols.md)

La séparation de la logique de la présentation est la philosophie de conception qui inspire le système de présentation de commande de l’infrastructure du ruban, un système basé sur un modèle de conception où les fonctionnalités et le comportement sont implémentés indépendamment des contrôles qui exposent cette fonctionnalité.

## <a name="user-interface"></a>Interface utilisateur

[Spécification des ressources d’image du ruban](windowsribbon-imageformats.md)

En tant que système de présentation de commande riche, l’infrastructure du ruban est conçue pour prendre en charge les ressources d’image de manière intensive dans l’interface utilisateur du ruban. Toutes les ressources d’image sont déclarées dans le [balisage du ruban](windowsribbon-schema.md) ou interrogées à partir d’une application hôte du ruban.

Pour Windows 8 et versions ultérieures, l’infrastructure du ruban prend en charge les formats graphiques suivants : fichiers BMP (bitmaps) 32 bits et fichiers PNG (Portable Network Graphics) avec transparence.

Pour Windows 7 et les versions antérieures, les ressources d’image doivent être conformes au format graphique BMP standard utilisé dans Windows.

[Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md)

Les contrôles hébergés dans la barre de commandes du ruban sont soumis à des règles de disposition appliquées par l’infrastructure du ruban et basées sur une combinaison de comportements par défaut et de modèles de disposition (à la fois définis par l’infrastructure et personnalisées) comme déclaré dans le balisage du ruban. Ces règles définissent les comportements de disposition adaptative de l’infrastructure du ruban qui influencent la manière dont les contrôles de la barre de commandes s’adaptent aux différentes tailles de ruban au moment de l’exécution.

[Utilisation des galeries](ribbon-controls-galleries.md)

L’infrastructure du ruban offre aux développeurs un modèle robuste et cohérent pour la gestion du contenu dynamique sur divers contrôles basés sur des collections. En adaptant et en reconfigurant l’interface utilisateur du ruban, ces contrôles dynamiques permettent à l’infrastructure de répondre à l’interaction de l’utilisateur dans l’application hôte et le ruban lui-même, et offrent la flexibilité nécessaire pour gérer différents environnements d’exécution.

[Affichage des onglets contextuels](ribbon-contextualtabs.md)

Dans une application de Framework de ruban, un onglet contextuel est un contrôle [onglet](windowsribbon-controls-tab.md) masqué qui est affiché dans la ligne d’onglet lorsqu’un objet dans l’espace de travail d’application, tel qu’une image, est sélectionné ou mis en surbrillance.

[Reconfiguration du ruban avec les modes d’application](ribbon-applicationmodes.md)

L’infrastructure du ruban prend en charge la reconfiguration et l’exposition dynamiques des éléments principaux de l’interface utilisateur du ruban au moment de l’exécution, en fonction de l’état de l’application (également appelé contexte). Déclarés et associés à des éléments spécifiques dans le balisage, les différents États pris en charge par une application sont appelés modes d’application.

[Personnalisation des couleurs du ruban](ribbon-color.md)

L’infrastructure du ruban expose un jeu de propriétés de couleur qui permettent à une application de personnaliser l’apparence des différents éléments de l’interface utilisateur du ruban au moment de l’exécution.

[Affichage du ruban](ribbon-visibility.md)

L’infrastructure du ruban expose un ensemble de propriétés qui permettent à une application de spécifier la manière dont l’interface utilisateur du ruban est affichée au moment de l’exécution.

## <a name="management"></a>Gestion

[Persistance de l’état du ruban](ribbon-statepersistence.md)

Windows Ribon Framework (ruban) offre la possibilité de conserver l’état d’une variété de paramètres utilisateur et de préférences dans les sessions d’application.

[Écoute des événements de ruban](listening-for-ribbon-events.md)

L’infrastructure du ruban utilise l’infrastructure de [suivi d’v nements pour Windows (ETW)](../etw/event-tracing-portal.md) pour permettre aux développeurs d’apprendre comment les utilisateurs interagissent avec le ruban de leur application.

## <a name="markup-compiler"></a>Compilateur de balisage

[Compilation du balisage du ruban](windowsribbon-intentcl.md)

Pour que l’infrastructure du ruban utilise le fichier de [balisage du ruban](windowsribbon-schema.md) , le fichier de balisage doit être compilé dans un fichier de ressources au format binaire. Un compilateur de balisage dédié, le compilateur de commandes d’interface utilisateur (UICC), est inclus dans le kit de développement logiciel (SDK) Microsoft Windows (7,0 ou version ultérieure) à cet effet. En plus de compiler la version binaire du balisage, UICC génère un fichier d’en-tête de définition d’ID (. h) qui expose tous les éléments de balisage à l’application hôte du ruban et un fichier de ressources (. RC) qui est utilisé pour lier des ressources d’image et de chaîne à l’application hôte au moment de la génération.

[Fonctionnement des messages du compilateur de balisage](windowsribbon-compilationerrors.md)

Le compilateur de balisage de l’infrastructure du ruban Windows (ruban), compilateur de commande d’interface utilisateur (UICC.exe), valide la balise du ruban par rapport au schéma du ruban et à un ensemble supplémentaire de règles définies par l’infrastructure du ruban.

 

 