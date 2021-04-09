---
description: Pour plus d’informations sur le diagramme suivant, consultez la légende diagramme de relation d’entité.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Groupe de tables principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a5cc87e80c60505025825353272699db574bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952892"
---
# <a name="core-tables-group"></a>Groupe de tables principales

Pour plus d’informations sur le diagramme suivant, consultez la [légende diagramme de relation d’entité](entity-relationship-diagram-legend.md).

![Groupe de tables principales](images/core.png)

Le groupe principal se compose de tables décrivant les fonctionnalités et les composants fondamentaux de l’application et du package d’installation. Par conséquent, les développeurs de packages d’installation doivent réfléchir à la façon de remplir ces tables en premier, car l’organisation d’une grande partie de la base de données est visible à partir du contenu de ce groupe.

-   Le [tableau de fonctionnalités](feature-table.md) répertorie toutes les fonctionnalités appartenant à l’application.
-   La [table de condition](condition-table.md) contient les expressions conditionnelles qui déterminent si une fonctionnalité particulière sera installée ou non.
-   Le [tableau FeatureComponents](featurecomponents-table.md) décrit les composants qui appartiennent à chaque fonctionnalité.
-   La [table](component-table.md) des composants répertorie tous les composants appartenant à l’installation.
-   Le [tableau répertoire](directory-table.md) répertorie les répertoires nécessaires au cours de l’installation. Étant donné que chaque composant doit être associé à un et un seul annuaire, la table des composants est étroitement liée à cette table et possède une clé externe pour la table de répertoires.
-   Le [tableau PublishComponent](publishcomponent-table.md) répertorie les fonctionnalités et les composants qui sont publiés pour une utilisation par d’autres applications. Les [composants et les fonctionnalités](components-and-features.md) sont les deux types de publication de fonctionnalités.
-   La [table MsiAssembly](msiassembly-table.md) spécifie Windows Installer paramètres pour .NET Framework assemblys Common Language Runtime et les assemblys Win32.
-   La [table MsiAssemblyName](msiassemblyname-table.md) spécifie le schéma pour les éléments d’un nom de cache d’assembly fort pour un assembly Common Language Runtime ou Win32.
-   La [table ComPlus](complus-table.md) contient les informations nécessaires pour installer les applications com+.
-   La [table IsolatedComponent](isolatedcomponent-table.md) associe le composant spécifié dans la \_ colonne application du composant (généralement un fichier. exe) au composant spécifié dans la \_ colonne partagé du composant (généralement une DLL partagée).
-   La [table de mise à niveau](upgrade-table.md) contient les informations requises lors des [mises à niveau majeures](major-upgrades.md).

 

 



