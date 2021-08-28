---
description: La liste espace disque vous permet de calculer l’espace disque requis pour effectuer les opérations d’installation.
ms.assetid: 6514cbdd-2f23-4ab8-9e34-86d3837503dc
title: À propos de la liste Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6595d3087ac8ac7913d4ce79acdc7607355eaa232342c5a7e2ef597e4fa5f013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887925"
---
# <a name="about-the-disk-space-list"></a>À propos de la liste Disk-Space

La liste espace disque vous permet de calculer l’espace disque requis pour effectuer les opérations d’installation. Après avoir créé une liste d’espace disque et y avoir ajouté des opérations de fichier, vous pouvez interroger la liste pour déterminer les lecteurs cibles spécifiés par les opérations de fichier et l’espace disque requis sur chaque lecteur.

En comparant l’espace nécessaire à l’espace disponible sur les disques cibles, vous pouvez déterminer par programme si un espace suffisant est disponible pour l’installation actuelle.

Vous pouvez ajouter ou supprimer des opérations de fichier dans la liste espace disque et recalculer l’espace disque requis. Cette fonctionnalité vous permet, par exemple, d’écrire un programme qui interagit avec l’utilisateur, ce qui lui permet de choisir les composants qu’il souhaite installer en fonction de l’espace disque requis.

Les fonctions de liste d’espace disque vérifient automatiquement les copies préexistantes des fichiers sur le disque cible. Si une version précédente du fichier est trouvée, les fonctions de liste d’espace disque calculent l’espace supplémentaire requis pour effectuer les opérations de fichier.

Par exemple, si une opération de copie spécifie qu’un fichier de 6000 octets doit être copié sur le lecteur C, et qu’une version de 2000 octets de ce fichier existe déjà sur le lecteur C, les fonctions d’espace disque retourneraient un espace requis de 4000 octets. L’espace supplémentaire est utilisé pour remplacer l’ancienne version du fichier par la version la plus récente.

La liste d’espace disque permet d’arrondir les tailles de fichiers aux limites du cluster de disque.

 

 



