---
description: Cet exemple montre comment utiliser des actions personnalisées pour créer des comptes d’utilisateur sur un ordinateur local lors de l’installation d’un composant.
ms.assetid: fc06dd7b-46d7-45a0-85b3-26f808c64f89
title: Utilisation d’une action personnalisée pour créer des comptes d’utilisateur sur un ordinateur local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd3bf002c0fa1d661c6bfebb6d1a18cbc4b0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319606"
---
# <a name="using-a-custom-action-to-create-user-accounts-on-a-local-computer"></a>Utilisation d’une action personnalisée pour créer des comptes d’utilisateur sur un ordinateur local

Cet exemple montre comment utiliser des actions personnalisées pour créer des comptes d’utilisateur sur un ordinateur local lors de l’installation d’un composant. La suppression d’un composant supprime les comptes d’utilisateurs locaux créés par l’action personnalisée. Plusieurs actions personnalisées sont illustrées, notamment des actions personnalisées d' [exécution différée](deferred-execution-custom-actions.md) et des [actions personnalisées de restauration](rollback-custom-actions.md).

L’exemple est conforme aux spécifications suivantes.

-   L’installation de crée des comptes d’utilisateur uniquement si Windows 2000 est en cours d’exécution.
-   L’installation de crée des comptes d’utilisateur uniquement si le composant est en cours d’installation pour s’exécuter localement. Cela empêche la création de comptes d’utilisateur lors de la réparation ou de la réinstallation du composant.
-   Le programme d’installation supprime les comptes lorsque le composant est supprimé.
-   Les informations de compte d’utilisateur sont lues à partir d’une table personnalisée dans la base de données d’installation et ne sont pas codées en dur dans le code d’action personnalisé.
-   Étant donné que la création ou la suppression de comptes d’utilisateur requiert des privilèges élevés, certaines des actions personnalisées doivent être en mesure d’apporter des modifications au système qui nécessitent des privilèges élevés. Ces actions personnalisées doivent être des actions personnalisées différées qui s’exécutent dans le script d’exécution.
-   Chaque compte a une action personnalisée de restauration pour s’assurer que le compte est supprimé lors de la restauration de l’installation du composant. Cela n’inclut pas la restauration d’une suppression de compte lors de la suppression d’un composant.
-   Les actions personnalisées envoient des messages ActionData pour chaque compte créé ou supprimé. Cela n’inclut pas la fourniture de messages de progression pour le ProgressBar.
-   Les actions personnalisées signalent une erreur si un compte ne peut pas être créé.
-   Le mot de passe du compte est obtenu par le biais de l’interaction de l’utilisateur avec l’interface utilisateur, ou dans le cas d’une installation au niveau de l’interface utilisateur de base ou aucun [niveau d’interface utilisateur](user-interface-levels.md), en tant que propriété passée sur la ligne de commande.
-   Les données sensibles sont masquées dans le fichier journal.

L’exemple comprend un composant hypothétique nommé TestAccount. Les sections suivantes supposent que vous avez déjà créé les ressources requises par TestAccount et que vous avez créé les tables de [fonctionnalités](feature-table.md), de [composants](component-table.md), de [fichiers](file-table.md), de [répertoires](directory-table.md)et de [FeatureComponents](featurecomponents-table.md) dans l’exemple de base de données requis pour installer ce composant. Pour plus d’informations, consultez [un exemple d’installation](an-installation-example.md).

Les rubriques suivantes contiennent des informations sur la façon de créer des actions personnalisées requises et de les ajouter à un package d’installation.

-   [Création des actions personnalisées](authoring-the-custom-actions.md)
-   [Ajout d’une table CustomUserAccounts personnalisée](adding-a-custom-customuseraccounts-table.md)
-   [Création de la table CustomAction](authoring-the-customaction-table.md)
-   [Création des tables ActionText et Error](authoring-the-actiontext-and-error-tables.md)
-   [Création de la table InstallExecuteSequence](authoring-the-installexecutesequence-table.md)
-   [Création de l’interface utilisateur pour l’entrée de mot de passe](authoring-the-user-interface-for-password-input.md)
-   [Sécurisation de l’installation](securing-the-installation.md)

 

 



