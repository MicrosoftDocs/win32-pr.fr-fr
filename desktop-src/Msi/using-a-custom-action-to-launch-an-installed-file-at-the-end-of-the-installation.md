---
description: L’exemple suivant montre comment lancer un fichier HTML à la fin d’une installation.
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: Utilisation d’une action personnalisée pour lancer un fichier installé à la fin de l’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c039d58830ce6a01f76a0946bced474e5091b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009589"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a>Utilisation d’une action personnalisée pour lancer un fichier installé à la fin de l’installation

L’exemple suivant montre comment lancer un fichier HTML à la fin d’une installation. Le programme d’installation installe le composant qui contient le fichier, puis publie un événement de contrôle à la fin de l’installation pour exécuter une action personnalisée qui ouvre le fichier. Cette approche peut être utilisée pour lancer un didacticiel d’aide à la fin de la première installation d’une application.

L’exemple doit respecter les spécifications suivantes.

-   Le programme d’installation exécute l’action personnalisée uniquement si le niveau d' [*interface utilisateur complet*](f-gly.md) est utilisé pour installer une application.
-   Le programme d’installation exécute l’action personnalisée uniquement si le composant qui contient le fichier HTML est installé pour s’exécuter localement sur l’ordinateur.
-   L’action personnalisée s’exécute uniquement lors de la première installation de l’application.
-   L’installation n’échoue pas si l’action personnalisée échoue.

L’exemple comprend un composant hypothétique nommé Tutorial qui contrôle au moins une ressource, un fichier nommé tutorial.htm. L’identificateur de ce fichier dans la colonne fichier de la table file est Tutorial. La discussion suivante suppose que vous avez déjà créé les ressources requises par le didacticiel et que vous avez effectué toutes les entrées nécessaires dans les tables [Feature](feature-table.md), [Component](component-table.md), [file](file-table.md), [Directory](directory-table.md)et [FeatureComponents](featurecomponents-table.md) pour installer ce composant. Pour plus d’informations, consultez [un exemple d’installation](an-installation-example.md).

Les rubriques suivantes contiennent des informations sur la façon de créer des actions personnalisées requises et de les ajouter à un package d’installation.

-   [Création de l’action personnalisée de lancement](authoring-the-launch-custom-action.md)
-   [Ajout d’un lancement aux tables CustomAction et binaires](adding-launch-to-the-customaction-and-binary-tables.md)
-   [Ajout d’un événement de contrôle à la fin de l’installation pour exécuter le lancement](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



