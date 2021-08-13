---
description: cette documentation est la principale source de documents de référence pour Windows Installer.
ms.assetid: dfbcc4b6-08bd-4b8a-b658-7010bd0b099c
title: guide de la Documentation Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad76621cf26e72bf277964609846c32e514b9cb73296bf27593111f84b92d037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625909"
---
# <a name="roadmap-to-windows-installer-documentation"></a>guide de la Documentation Windows Installer

cette documentation est la principale source de documents de référence pour Windows Installer. Il fournit des informations sur les packages d’installation et le service d’installation. Il fournit également une description complète de l’interface de programmation d’applications (API) et des éléments de la base de données du programme d’installation. cette documentation contient également une discussion sur les exemples de base des packages d’installation et de mise à jour dans [Windows Installer exemples](windows-installer-examples.md).

le [guide basé sur les rôles de Windows Installer Documentation](role-based-guide-to-windows-installer-documentation.md) est une alternative fournie aux lecteurs qui préfèrent voir des liens vers des rubriques organisées par rôle professionnel et des scénarios de tâches courantes.

pour plus d’informations sur les groupes de discussion Windows Installer, consultez également la rubrique : [autres Sources d’informations](other-sources-of-windows-installer-information.md)sur les Windows Installer.

pour obtenir la liste des conseils sur l’utilisation de la Windows Installer, consultez [Windows Installer meilleures pratiques](windows-installer-best-practices.md).

La liste suivante décrit chaque section de la documentation du programme d’installation.

-   [à propos de Windows Installer](about-windows-installer.md) fournit une vue d’ensemble des fonctionnalités et des avantages du programme d’installation, tels que la publication, l’installation à la demande, la résilience, la personnalisation et la gestion des composants. Cette section présente les concepts des composants et fonctionnalités du programme d’installation, qui sont essentiels pour comprendre comment le programme d’installation organise une installation. Il aborde également plusieurs sujets de haut niveau sur l’installation, tels que la stratégie système, les règles de contrôle de version des fichiers et l’installation de la restauration.
-   [l’utilisation de Windows Installer](using-windows-installer.md) présente diverses rubriques, telles qu’une méthode standard pour organiser une application en composants que le programme d’installation peut installer ou supprimer sur l’ordinateur d’un utilisateur. Comment télécharger un package d’installation à partir du World Wide Web ; et l’utilisation d’images sources compressées.
-   les informations contenues dans les sections [nouveautés dans Windows Installer](what-s-new-in-windows-installer.md) peuvent être utilisées pour identifier les nouvelles fonctionnalités qui ne sont pas prises en charge par les versions antérieures de Windows Installer.
-   [signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md) décrit comment les signatures numériques peuvent être utilisées avec les packages, les transformations, les correctifs, les modules de fusion et les fichiers cab externes.
-   les [assemblys](assemblies.md) expliquent comment utiliser Windows Installer pour installer et gérer les assemblys Win32 et le temps d’exécution du langage courant.
-   L' [interface utilisateur](user-interface.md) fournit des informations sur les fonctionnalités de l’interface utilisateur du programme d’installation. Bien que le programme d’installation ne fournisse pas d’interface utilisateur, l’auteur d’un package peut conserver toutes les données et la logique requises pour exécuter une interface utilisateur interne ou externe entièrement interactive dans la base de données d’installation. La section de référence décrit les éléments de l’interface utilisateur qui sont dépendants des tables de base de données, y compris les boîtes de dialogue, les contrôles et les événements de contrôle.
-   [Actions standard](standard-actions.md) présente les actions standard utilisées par le programme d’installation dans les tables de séquence pour effectuer une installation. Ces informations sont principalement destinées aux développeurs de packages.
-   [Actions personnalisées](custom-actions.md) décrit comment créer des fonctionnalités supplémentaires dans le programme d’installation. Les actions personnalisées permettent à l’auteur d’un package d’installation d’étendre les fonctionnalités des actions standard en incluant des fichiers exécutables, des bibliothèques de liens dynamiques et des scripts. Ces informations sont destinées aux développeurs de packages qui doivent effectuer des fonctions d’installation introuvables ailleurs dans le programme d’installation.
-   [Propriétés](properties.md) fournit des informations sur les propriétés utilisées par le programme d’installation au cours d’une installation. Les sections about et Using offrent une vue d’ensemble de ces variables globales et chaque propriété est décrite dans la section de référence.
-   Le [flux d’informations de synthèse](summary-information-stream.md) documente les propriétés d’informations de résumé utilisées par le programme d’installation. Ces informations présentent un intérêt pour tous les développeurs.
-   L' [application de correctifs et de mises à niveau](patching-and-upgrades.md) traite de l’utilisation du programme d’installation pour effectuer des mises à jour de fichiers, des correctifs logiciels, des mises à jour mineures, des mises à niveau de produits et des correctifs.
-   [Transformations](transforms.md) explique comment modifier ou personnaliser une base de données d’installation à l’aide d’une transformation de base de données et comment générer, sécuriser et appliquer des transformations.
-   La [validation du package](package-validation.md) traite de l’utilisation des évaluateurs de cohérence internes (ICEs) pour tester la cohérence interne des packages d’installation en cours de développement.
-   Les [modules de fusion](merge-modules.md) présentent une norme pour la conception des modules de fusion. Cette norme doit être suivie par les développeurs qui créent leurs propres modules de fusion, ainsi que par les développeurs qui envisagent d’utiliser le programme d’installation pour distribuer du code partagé à leurs applications.
-   [Windows Installer sur les systèmes d’exploitation 64 bits](windows-installer-on-64-bit-operating-systems.md) explique comment utiliser Windows Installer pour installer et gérer les composants du programme d’installation conçus pour s’exécuter sur des systèmes d’exploitation 64 bits.
-   [Windows Installer exemples](windows-installer-examples.md) contient un exemple pas à pas de création d’un package d’installation avec une interface utilisateur interne dans [un exemple d’installation](an-installation-example.md). Pour obtenir un exemple de création d’une mise à niveau majeure pour un package existant, consultez [un exemple de mise à niveau](an-upgrade-example.md). Pour savoir comment une transformation de personnalisation désactive les fonctionnalités et ajoute de nouvelles ressources, consultez [un exemple de transformation de personnalisation](a-customization-transform-example.md). Pour obtenir un exemple de création d’un package de correctifs qui applique une petite mise à jour à un package d’installation existant, consultez [un exemple de mise à jour corrective de petite taille](a-small-update-patching-example.md). Pour savoir comment localiser un package d’installation existant, consultez [un exemple de localisation](a-localization-example.md).
-   l' [interface d’automatisation](automation-interface.md) fournit des informations aux développeurs qui souhaitent utiliser l’interface automation de Windows Installer.
-   Les [fonctions du programme d’installation](installer-functions.md) décrivent les appels de fonction à l’API du programme d’installation. Il s’agit des fonctions que d’autres applications appellent pour accéder aux services du programme d’installation afin d’installer, de gérer ou de supprimer des applications. Les sections utilisation incluent des discussions sur la manière de demander des fonctionnalités, d’initier des installations et de réinstaller des composants manquants par programmation. La section de référence est la documentation de référence principale pour les fonctions du service d’installation.
-   La [base de données](installer-database.md) d’installation discute de la base de données d’installation. Le programme d’installation conserve toute la logique et les données nécessaires pour une installation dans une base de données relationnelle située dans un fichier de .msi. La section à propos de fournit une vue d’ensemble des diagrammes de schéma pour les principaux groupes fonctionnels de tables de la base de données. La section utilisation traite de l’utilisation des tables les plus importantes. Ces sections contiennent des informations qui sont essentielles pour les développeurs qui créent des packages d’installation ou écrivent des outils de création de package. La section de référence contient des documents de référence complets pour chaque table de base de données. Cette section contient également la référence principale de chacune des fonctions de base de données. Les fonctions de base de données sont utilisées en interne par le programme d’installation pour accéder à la base de données et présentent principalement un intérêt pour les développeurs d’outils de création de packages d’installation.

 

 



