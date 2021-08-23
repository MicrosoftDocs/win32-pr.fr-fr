---
description: Les auteurs des packages d’installation peuvent spécifier que le programme d’installation copie les fichiers partagés (les dll communément partagés) d’une application dans le dossier de l’application plutôt que dans un emplacement partagé.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Composants isolés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08095e72862a94474b7096950ac5ed3b331e806456e72982ee9d7374ab9511b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013177"
---
# <a name="isolated-components"></a>Composants isolés

Les auteurs des packages d’installation peuvent spécifier que le programme d’installation copie les fichiers partagés (les dll communément partagés) d’une application dans le dossier de l’application plutôt que dans un emplacement partagé. Ce jeu de fichiers (dll) privé est ensuite utilisé uniquement par l’application. L’isolation de l’application avec ses composants partagés de cette manière présente les avantages suivants :

-   L’application utilise toujours les versions des fichiers partagés avec lesquels elle a été déployée.
-   L’installation de l’application ne remplace pas les autres versions des fichiers partagés par d’autres applications.
-   Les installations ultérieures d’autres applications utilisant des versions différentes des fichiers partagés ne peuvent pas remplacer les fichiers utilisés par cette application.

Étant donné que l’implémentation actuelle de COM conserve un seul chemin d’accès complet dans le registre pour chaque paire CLSID/contexte, elle force toutes les applications à utiliser la même version d’une DLL partagée. pour permettre à une application de conserver une copie privée d’un serveur COM, le chargeur du système dans Windows 2000 vérifie la présence d’un. Fichier LOCAL dans le dossier de l’application. Si le chargeur de système détecte un. Fichier LOCAL, il modifie sa logique de recherche pour préférer les dll situées dans le même dossier que l’application.

lorsque Windows Installer exécute l' [action IsolateComponents](isolatecomponents-action.md) , il copie les fichiers du composant (généralement une DLL partagée) spécifiés dans la \_ colonne shared component de la [table IsolatedComponent](isolatedcomponent-table.md) dans le même dossier que le composant (généralement un fichier .exe) spécifié dans la \_ colonne Application du composant. Le programme d’installation crée un fichier dans ce répertoire, avec une longueur de zéro octet, en utilisant le nom de fichier abrégé du fichier de clé pour l’application du composant \_ (en général, le nom est le même que celui de l’application .exe) ajouté à. Localisé. Le programme d’installation utilise l’inscription du composant dans son emplacement partagé et n’écrit pas d’informations d’inscription pour la copie du composant dans l’emplacement privé.

Pour plus d'informations, consultez les pages suivantes :

-   [Installation de composants isolés](installation-of-isolated-components.md)
-   [Réinstallation de composants isolés](reinstallation-of-isolated-components.md)
-   [Suppression de composants isolés](removal-of-isolated-components.md)
-   [Utilisation des composants isolés](using-isolated-components.md)

 

 



