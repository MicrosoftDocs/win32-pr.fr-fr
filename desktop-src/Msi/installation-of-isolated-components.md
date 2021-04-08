---
description: Windows Installer effectue les actions suivantes lors de l’installation d’une application lorsque le package contient des composants isolés. En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Installation de composants isolés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753765"
---
# <a name="installation-of-isolated-components"></a>Installation de composants isolés

Windows Installer effectue les actions suivantes lors de l’installation d’une application lorsque le package contient des composants isolés. En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.

## <a name="installation"></a>Installation

-   Copiez les fichiers du composant \_ partagé dans le même dossier que le composant \_ application Component uniquement si l' \_ application composant est également en cours d’installation.
-   Créez un fichier de zéro octet avec le nom de fichier abrégé du fichier de clé de l’application de composant \_ . Recherchez ce fichier dans le même dossier que le composant \_ application. Ajoutez l’extension. LOCAL pour ce nom de fichier.
-   Incrémentez le refcount SharedDLL si le bit msidbComponentAttributesSharedDllRefCount est défini dans la colonne attributs de la [table des composants](component-table.md).
-   Inscrire \_ l’application composant en tant que client du composant \_ partagé et enregistrer un chemin d’accès de clé pointant vers l’emplacement partagé du composant \_ partagé.
-   Installez toutes les ressources de l’application de composant \_ comme d’habitude.

Si \_ le composant partagé ou son fichier de clé est déjà installé sur l’ordinateur, ne copiez pas les fichiers dans l’emplacement partagé du composant \_ partagé.

Si \_ le composant partagé ou son fichier de clé n’est pas encore installé sur l’ordinateur :

-   Copiez les fichiers du composant \_ partagé dans l’emplacement partagé.
-   Traite toutes les actions d’installation du composant \_ partagé.
-   Si le composant \_ partagé est un composant com, enregistrez le chemin d’accès com complet afin que la syntaxe \[ $Component \] et \[ \# FileKey \] pointent vers l’emplacement partagé du composant \_ partagé.

 

 



