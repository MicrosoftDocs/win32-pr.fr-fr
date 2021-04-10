---
description: Ajoutez un enregistrement à la table CustomAction pour l’action personnalisée Launch.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Ajout d’un lancement aux tables CustomAction et binaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115390"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a>Ajout d’un lancement aux tables CustomAction et binaires

Ajoutez un enregistrement à la [table CustomAction](customaction-table.md) pour l’action personnalisée Launch. Entrez le nom de l’action personnalisée dans la colonne action de la table CustomAction. Entrez le type numérique total pour Launch, 65, dans la colonne type de la table d’action personnalisée. La colonne source de la table CustomAction spécifie une clé dans l’enregistrement de la [table binaire](binary-table.md) qui contient les données binaires de la dll. Entrez Tutorial.dll dans la colonne source de la table CustomAction. Le point d’entrée spécifié dans le champ cible de la table CustomAction doit correspondre à celui exporté à partir de la DLL. Entrez LaunchTutorial dans la colonne cible de la table CustomAction.

[Table CustomAction](customaction-table.md)



| Action | Type | Source       | Cible         |
|--------|------|--------------|----------------|
| Lancer | 65   | Tutorial.dll | LaunchTutorial |



 

Ajoutez la Tutorial.dll que vous avez créée à partir de Tutorial. cpp en tant que flux binaire à la table binaire.

[Table binaire](binary-table.md)



| Nom         | Données                          |
|--------------|-------------------------------|
| Tutorial.dll | {*données binaires ajoutées pour la dll*} |



 

Continuez à [Ajouter un événement de contrôle à la fin de l’installation pour exécuter le lancement](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).

 

 



