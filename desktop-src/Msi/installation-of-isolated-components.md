---
description: Windows Le programme d’installation effectue les actions suivantes lors de l’installation d’une application lorsque le package contient des composants isolés. En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Installation de composants isolés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f842f626775dce436abedace96549fd55079c577885aad81492df861cd1a68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634124"
---
# <a name="installation-of-isolated-components"></a>Installation de composants isolés

Windows Le programme d’installation effectue les actions suivantes lors de l’installation d’une application lorsque le package contient des composants isolés. En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.

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

 

 



