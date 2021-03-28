---
description: L’interface utilisateur de Windows permet aux utilisateurs d’accéder à un large éventail d’objets nécessaires pour exécuter des applications et gérer le système d’exploitation.
title: Guide du développeur de l’interpréteur de commandes
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1be17ca90b7138294be3e1b34fa3fcb4dcb4227a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991149"
---
# <a name="shell-developers-guide"></a>Guide du développeur de l’interpréteur de commandes

L’interface utilisateur de Windows permet aux utilisateurs d’accéder à un large éventail d’objets nécessaires pour exécuter des applications et gérer le système d’exploitation. Les plus nombreux et les plus familiers de ces objets sont les dossiers et les fichiers qui résident sur les lecteurs de disque de l’ordinateur. Il existe également un certain nombre d’objets virtuels qui permettent à l’utilisateur d’effectuer des tâches telles que l’envoi de fichiers à des imprimantes distantes ou l’accès à la corbeille. L’interpréteur de commandes organise ces objets dans un espace de noms hiérarchique et fournit aux utilisateurs et aux applications un moyen cohérent et efficace d’accéder aux objets et de les gérer.

## <a name="in-this-section"></a>Dans cette section

-   [Considérations relatives à la sécurité : Microsoft Windows Shell](sec-shell.md)
-   [Conseils pour l’implémentation des extensions de In-Process](shell-and-managed-code.md)
-   [Versions de l’interpréteur de commandes et des contrôles communs](versions.md)
-   [Implémentation des interfaces d’objets de dossier de base](nse-implement.md)
-   [Implémentation d’un format de fichier personnalisé](customizing-file-types-bumper.md)
-   [Extensibilité de l’interpréteur de commandes (création d’une source de données)](shell-extensibility-bumper.md)
-   [Implémentation des éléments du panneau de configuration](control-panel-applications.md)
-   [Prise en charge des applications Shell](application-support-bumper.md)
-   [Rubriques sur l’interpréteur de commandes hérité](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a>Conventions de document

Le guide des développeurs de Shell suit les conventions de document du kit de développement logiciel (SDK) Windows habituel. Deux conventions en particulier doivent être indiquées :

-   L’exemple de code omet le code de correction des erreurs normal. Ce code a été supprimé uniquement pour rendre le code plus lisible. Vous devez inclure tous les codes de correction des erreurs appropriés dans vos propres applications.
-   Pour afficher des exemples d’entrées de Registre, les noms de clé, de sous-clé et d’entrée, ainsi que les valeurs sont affichés avec une police standard. Les noms d’éléments définis par l’utilisateur ou l’application sont en italique.

 

 



