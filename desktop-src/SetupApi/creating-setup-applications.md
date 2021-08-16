---
description: Après avoir créé un fichier INF, vous allez généralement écrire le code source de votre application d’installation. Vous appelez les fonctions d’installation à partir de votre application d’installation pour effectuer de nombreuses opérations d’installation.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Création d’applications d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e77f920a024a4414690baad7684af90a30ee4ca3c9f96a2c6f61b1b84430c072
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887436"
---
# <a name="creating-setup-applications"></a>Création d’applications d’installation

Après avoir créé un fichier INF, vous allez généralement écrire le code source de votre application d’installation. Vous appelez les fonctions d’installation à partir de votre application d’installation pour effectuer de nombreuses opérations d’installation.

Les étapes suivantes décrivent une façon d’utiliser les fonctions de configuration pour créer une application d’installation. Vous pouvez utiliser cet exemple comme point de départ ou développer votre propre algorithme d’installation.

**Initialisation**

-   [Ouvrez le fichier INF et, le cas échéant, ajoutez d’autres fichiers INF.](opening-the-inf-file.md)
-   [Extrayez les informations de fichier à partir du fichier INF.](extracting-file-information-from-the-inf-file.md)
-   [Rassemblez les informations d’installation de l’utilisateur.](gathering-setup-information-from-the-user.md)
-   [Créez une file d’attente.](creating-a-queue-and-queuing-file-operations.md)

**Fichiers d’installation**

-   [Validez la file d’attente, en spécifiant une routine de rappel.](committing-the-queue.md)
-   [Mettre à jour les informations du Registre.](updating-registry-information.md)

**Nettoyage**

-   [Fermez la file d’attente de fichiers et le fichier INF.](closing-the-file-queue-and-inf-file.md)
-   [Libérez toutes les autres ressources système et mettez fin au programme.](releasing-other-system-resources.md)

 

 



