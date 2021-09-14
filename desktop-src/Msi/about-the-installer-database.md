---
description: la base de données Windows Installer se compose de nombreuses tables liées entre elles qui forment une base de données relationnelle des informations nécessaires à l’installation d’un groupe d’applications.
ms.assetid: 3352dd8f-c082-4c4b-98be-5823c8b28f07
title: À propos de la base de données du programme d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f0ee2cc326f85d964ac3d845b97751a48fbb91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092937"
---
# <a name="about-the-installer-database"></a>À propos de la base de données du programme d’installation

la base de données Windows Installer se compose de nombreuses tables liées entre elles qui forment une base de données relationnelle des informations nécessaires à l’installation d’un groupe d’applications. Étant donné que la base de données est relationnelle, les tables sont liées par les données dans les valeurs de clé primaire et étrangère. Cela constitue une méthode efficace pour modifier le processus d’installation et signifie que les utilisateurs peuvent personnaliser plus facilement une application ou un groupe d’applications de grande taille. Les tables de base de données reflètent la disposition générale du groupe entier d’applications, notamment :

-   Fonctionnalités disponibles
-   Composants
-   Relation entre les fonctionnalités et les composants
-   Paramètres du Registre nécessaires
-   Interface utilisateur pour l’application

Pour créer une base de données d’installation, vous devez remplir les tables avec toutes les informations relatives aux applications et au processus d’installation. La création manuelle de toutes ces tables devient une tâche importante, même pour une installation de taille modérée. par conséquent, certains outils tiers sont disponibles pour faciliter la création de la base de données du programme d’installation. Les sections suivantes décrivent les groupes de tables de base de données associées.

[Groupe de tables principales](core-tables-group.md)

[Groupe de tables de fichiers](file-tables-group.md)

[Groupe de tables de Registre](registry-tables-group.md)

[Groupe de tables système](system-tables-group.md)

[Groupe de tables de localisateur](locator-tables-group.md)

[Groupe de tables d’informations sur les programmes](program-information-tables-group.md)

[Groupe de tables de procédure d’installation](installation-procedure-tables-group.md)

[Légende du diagramme des relations d’entités](entity-relationship-diagram-legend.md)

[Fichiers d’archive de texte](text-archive-files.md)

Pour obtenir la liste complète de toutes les tables d’une base de données d’installation, consultez [tables de base de données](database-tables.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



