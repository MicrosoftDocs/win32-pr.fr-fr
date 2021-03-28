---
description: L’interface utilisateur de Windows permet aux utilisateurs d’accéder à un large éventail d’objets nécessaires pour exécuter des applications et gérer le système d’exploitation.
title: Shell Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973323"
---
# <a name="windows-shell"></a>Shell Windows

L’interface utilisateur de Windows permet aux utilisateurs d’accéder à un large éventail d’objets nécessaires pour exécuter des applications et gérer le système d’exploitation. Les plus nombreux et les plus familiers de ces objets sont les dossiers et les fichiers qui résident sur les lecteurs de disque de l’ordinateur. Il existe également un certain nombre d’objets virtuels qui permettent à l’utilisateur d’effectuer des tâches telles que l’envoi de fichiers à des imprimantes distantes ou l’accès à la corbeille. L’interpréteur de commandes organise ces objets dans un espace de noms hiérarchique et fournit aux utilisateurs et aux applications un moyen cohérent et efficace d’accéder aux objets et de les gérer.

## <a name="shell-development-scenarios"></a>Scénarios de développement de Shell

Les scénarios de développement suivants sont liés au développement d’applications :

-   Extension de l’interpréteur de commandes, qui consiste à créer une source de données (plutôt que de consommer le modèle de données Shell)
-   Implémentation d’un sous-ensemble des tâches de la source de données Shell
-   Prise en charge des bibliothèques et des affichages d’éléments dans l’Explorateur Windows
-   Utilisation de la boîte de dialogue fichier commun
-   Implémentation des éléments du panneau de configuration
-   Gestion des notifications

Les scénarios de développement suivants sont liés à la propriété de format de fichier :

-   Implémentation d’un sous-ensemble des tâches de la source de données Shell
-   Implémentation d’un gestionnaire
-   Prise en charge de Desktop Search

Les scénarios de développement suivants sont liés à la propriété du stockage des données :

-   Prise en charge de Desktop Search et OpenSearch
-   Implémentation d’un sous-ensemble des tâches de la source de données Shell (dossiers virtuels)
-   Bibliothèques de prise en charge dans l’Explorateur Windows

Le scénario de développement suivant est associé à la prise en charge des appareils :

-   Exécution automatique et lecture automatique

## <a name="windows-shell-sdk-documentation"></a>Documentation du kit de développement logiciel (SDK) Windows Shell

Cette documentation est divisée en trois sections principales :

-   Le [Guide du développeur de l’interpréteur](intro.md) de commandes fournit des informations conceptuelles sur le fonctionnement de l’interpréteur de commandes et sur l’utilisation de l’API de l’interpréteur de commandes dans votre application.
-   La section informations de référence sur le [Shell](shell-reference-bumper.md) documente les éléments de programmation qui composent les différentes API de Shell.
-   Les [exemples de Shell](samples-entry.md) fournissent des liens vers des exemples de code connexes.

Le tableau suivant présente la section Référence de l’interpréteur de commandes. Sauf indication contraire, tous les éléments de programmation sont documentés dans le C++ non managé.



| Section                                                               | Description                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Classes de Shell](classes.md)                                          | Cette section décrit la sélection des classes de shell Windows.                                                                 |
| [Interfaces Shell](interfaces.md)                                    | Cette section décrit les interfaces COM (Component Object Model) du shell Windows.                                    |
| [Fonctions Shell](functions.md)                                      | Cette section décrit les fonctions de l’interpréteur de commandes Windows.                                                                  |
| [Fonctions de rappel de l’interpréteur de commandes](callbacks.md)                             | Cette section décrit les modèles des fonctions de rappel de l’interpréteur de commandes Windows.                                               |
| [Constantes, énumérations et indicateurs de Shell](consts-enums-flags.md)    | Cette section décrit les constantes, énumérations et indicateurs de l’interpréteur de commandes Windows utilisés dans les API de l’interpréteur de commandes.                  |
| [Fonctions utilitaires légères de l’interpréteur de commandes](shlwapi.md)                    | Cette section décrit les fonctions de l’utilitaire léger Windows Shell fournies dans Shlwapi.dll.                      |
| [Macros de Shell](macros.md)                                            | Cette section décrit les macros de l’utilitaire Windows Shell.                                                             |
| [Messages et notifications de l’interpréteur de commandes](messages.md)                      | Cette section décrit les messages et les notifications envoyés par les éléments de l’interpréteur de commandes Windows.                         |
| [Objets Shell pour l’écriture de scripts et Microsoft Visual Basic](objects.md) | Cette section décrit les objets Windows implémentés par le Shell pour une utilisation dans les scripts et les Visual Basic Microsoft. |
| [Objets Shell pour C++](objects-cpp.md)                              | Cette section décrit les objets Windows C++ implémentés par l’interpréteur de commandes.                                             |
| [Schémas de Shell](schemas.md)                                          | Cette section décrit les schémas de manifeste de bibliothèque, de propriété et de transfert utilisés par le shell Windows.                   |
| [Structures de Shell](structures.md)                                    | Cette section décrit les structures de shell Windows utilisées dans les API de l’interpréteur de commandes.                                          |



 

 

 



