---
description: Windows Installer effectue les actions suivantes lors de la réinstallation d’une application lorsque le package contient des composants isolés. En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Réinstallation de composants isolés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad1c7fb53eb09e96882209f7738e95be9b4a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864829"
---
# <a name="reinstallation-of-isolated-components"></a>Réinstallation de composants isolés

Windows Installer effectue les actions suivantes lors de la réinstallation d’une application lorsque le package contient des composants isolés. En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.

## <a name="reinstallation"></a>La réinstallation

-   Réinstallez les fichiers du composant \_ partagés dans le même dossier que le composant \_ application Component uniquement si l' \_ application composant est également en cours de réinstallation.
-   N’incrémentez pas la liste des clients du composant \_ partagé et n’incrémentez pas le nombre de SharedDLL.
-   Recréez le fichier de zéro octet avec le nom de fichier abrégé du fichier de clé de l’application de composant \_ . Ce fichier doit se trouver dans le même dossier que \_ le composant application et avoir l’extension. Localisé.
-   Réinstallez toutes les ressources de l' \_ application de composant comme d’habitude.

Si le refcount SharedDLL pour le composant \_ partagé est supérieur à 1, ou si d’autres produits sont conservés dans la liste des clients du composant \_ partagé :

-   Ne réinstallez aucun fichier à l’emplacement partagé du composant \_ partagé.

Si le refcount SharedDLL pour le composant \_ partagé est égal à 1, ou s’il n’existe aucun autre client restant du composant \_ partagé :

-   Réinstallez les fichiers du composant \_ partagés dans l’emplacement partagé à l’aide des règles de contrôle de [version des fichiers](file-versioning-rules.md).
-   Traiter toutes les actions de réinstallation pour le composant \_ partagé.
-   Si le composant \_ partagé est un composant com, enregistrez le chemin d’accès com complet afin que la syntaxe du programme d’installation \[ $Component \] et \[ \# FileKey \] pointer vers l’emplacement partagé du composant \_ partagé.

 

 



