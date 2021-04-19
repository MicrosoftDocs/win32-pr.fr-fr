---
description: Le concept d’un composant est essentiel pour organiser les fichiers dont le writer doit être sauvegardé ou restauré.
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: Composants de métadonnées VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c913262158d59a69de21a6e0d49e31979c1a0cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515249"
---
# <a name="vss-metadata-components"></a>Composants de métadonnées VSS

Le concept d’un [*composant*](vssgloss-c.md)est essentiel pour organiser les fichiers dont le writer doit être sauvegardé ou restauré.

Les composants permettent à un enregistreur d’indiquer à un moteur de sauvegarde comment ses fichiers doivent être organisés, les dépendances entre les fichiers et le type de données que ces fichiers peuvent contenir. Cela permet à un moteur de sauvegarde de décider comment stocker les fichiers pour une efficacité maximale.

En outre, les applications basées sur VSS utilisent des composants comme blocs de construction pour leurs métadonnées et le support pour la communication de rédacteur/demandeur.

Les rédacteurs et les demandeurs stockent des informations sur les composants séparément : dans le document de métadonnées de l’enregistreur et dans le document composants de sauvegarde, respectivement, et les informations diffèrent dans chaque représentation.

Les informations sur les composants dans les documents de métadonnées d’écriture incluent les éléments suivants :

-   Informations d’un seul enregistreur dans chaque document
-   Tous les composants de ce writer, qu’ils puissent être [*inclus explicitement*](vssgloss-e.md) ou doivent être [*implicitement inclus*](vssgloss-i.md) dans une opération de sauvegarde ou de restauration
-   Informations de [*chemin d’accès logique*](vssgloss-l.md) utilisées pour associer un composant sélectionnable pour la sauvegarde à des composants de sauvegarde spécifiques, ce qui permet de former un ensemble de composants
-   Informations sur le [*jeu de fichiers*](vssgloss-f.md) — chemin, spécification de fichier et indicateur de récurrence — géré pour chaque composant

Les documents de métadonnées d’écriture contiennent également des informations de métadonnées au niveau de l’enregistreur, telles que les méthodes de restauration et les mappages d’emplacements de remplacement pour la restauration. Les documents de métadonnées de l’enregistreur sont en lecture seule. L’interface permettant d’examiner ces informations est [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).

Les informations sur les composants dans les documents des composants de sauvegarde incluent les éléments suivants :

-   Uniquement les informations sur les composants inclus explicitement
-   Informations de métadonnées au niveau de l’enregistreur, telles que les mappages d’emplacement de remplacement et la restauration
-   Informations d’état décrivant une opération de sauvegarde ou de restauration

Les documents des composants de sauvegarde ne contiennent pas d’informations sur les [*jeux de fichiers*](vssgloss-f.md)des composants. Les documents des composants de sauvegarde ne sont pas en lecture seule et peuvent être modifiés par le writer. L’interface pour accéder à ces informations est [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).

Le cycle de vie et la relation entre les deux expressions d’un composant peuvent être interprétés comme suit :

-   Les enregistreurs sont responsables des définitions initiales des composants.
-   Un demandeur examine les métadonnées de tous les enregistreurs et leurs composants.
-   À partir des informations sur la sélectivité et le chemin logique des composants, un demandeur détermine quels composants doivent être explicitement inclus, qui peuvent être inclus explicitement, qui définissent des ensembles de composants et qui sont membres de jeux de composants.
-   Un demandeur ajoute les composants qui requièrent une inclusion explicite, et inclut implicitement les sous-composants dans les [*ensembles de composants*](/windows) (dont les informations ne se trouvent pas dans le document sur les composants de sauvegarde).
-   Lors de la gestion des événements, les rédacteurs et les demandeurs peuvent modifier et examiner les informations de composant stockées dans le document composants de sauvegarde pour coordonner leur activité.

Les informations de composant de l’enregistreur et de la version du demandeur sont requises pour exécuter correctement les opérations de sauvegarde et de restauration, et les deux doivent être stockées avec les données sauvegardées :

-   [Types de composants](component-types.md)
-   [Définition des composants par les rédacteurs](definition-of-components-by-writers.md)
-   [Utilisation de composants par le demandeur](use-of-components-by-the-requestor.md)

 

 
