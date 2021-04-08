---
description: Cet exemple montre comment créer un package Windows Installer simple qui installe une application.
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: Exemple d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864493"
---
# <a name="an-installation-example"></a>Exemple d’installation

Cet exemple montre comment créer un package Windows Installer simple qui installe une application. L’exemple installe le bloc-notes, un éditeur de texte inclus avec Windows et plusieurs fichiers texte qui décrivent les événements et les admissions à l’aide du parc rouge imaginaire.

L’exemple présente les spécifications suivantes :

-   L’application est fournie aux utilisateurs sous la forme d’un package de Windows Installer qui installe automatiquement tous les fichiers, raccourcis et informations de registre requis.
-   Le package d’installation peut présenter à l’utilisateur un assistant d’interface utilisateur lors de l’installation afin de collecter les informations de l’utilisateur.
-   Pendant l’installation, les utilisateurs ont la possibilité de sélectionner des fonctionnalités individuelles à installer pour s’exécuter-localement, d’exécuter à partir de la source ou de ne pas être installées.
-   L’une des fonctionnalités peut être présentée aux utilisateurs sous la forme d’une fonctionnalité d’installation à la demande.
-   Le même package désinstalle l’application et supprime tous les fichiers d’application et les informations de registre de l’ordinateur de l’utilisateur.
-   Le package est prêt à recevoir une mise à niveau majeure qui comprend la modification de son code de produit.

Pour reproduire l’exemple, vous avez besoin d’un outil logiciel apte à créer et à modifier une base de données Windows Installer vide. Plusieurs outils de création de packages sont disponibles auprès des éditeurs de logiciels indépendants. Un éditeur de base de données Windows Installer appelé Orca est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Pour compléter l’exemple, procédez comme suit :

[Planification de l’installation](planning-the-installation.md)

[Importation d’une base de données vide](importing-a-blank-database.md)

[Spécification de la structure de répertoires](specifying-directory-structure.md)

[Spécification des composants](specifying-components.md)

[Spécification des fichiers et des attributs de fichier](specifying-files-and-file-attributes.md)

[Spécification du média source](specifying-source-media.md)

[Spécification des fonctionnalités](specifying-features.md)

[Spécification des relations Feature-Component](specifying-feature-component-relationships.md)

[Ajout d’informations de Registre](adding-registry-information.md)

[Spécification de raccourcis](specifying-shortcuts.md)

[Spécification des propriétés](specifying-properties.md)

[Importation du InstallExecuteSequence](importing-the-installexecutesequence.md)

[Importation du InstallUISequence](importing-the-installuisequence.md)

[Importation du AdminExecuteSequence](importing-the-adminexecutesequence.md)

[Importation du AdminUISequence](importing-the-adminuisequence.md)

[Importation du AdvtExecuteSequence](importing-the-advtexecutesequence.md)

[Ajout d’informations de résumé](adding-summary-information.md)

[Importation de l’interface utilisateur](importing-the-user-interface.md)

[Validation d’une base de données d’installation](validating-an-installation-database.md)

 

 



