---
description: Chaque fonctionnalité de Windows Installer utilise un ou plusieurs composants Windows Installer, et les fonctionnalités peuvent partager des composants.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Spécification des relations Feature-Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05ff15f4c735ac7d081c16f49f1aafe555a96db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517542"
---
# <a name="specifying-feature-component-relationships"></a>Spécification des relations Feature-Component

Chaque [fonctionnalité de Windows Installer](windows-installer-features.md) utilise un ou plusieurs [composants Windows Installer](windows-installer-components.md), et les fonctionnalités peuvent partager des composants. La [table FeatureComponents](featurecomponents-table.md) définit la relation entre les fonctionnalités et les composants. Pour plus d’Windows Installer vue d’ensemble, consultez le groupe et les [composants et fonctionnalités](components-and-features.md) [principaux des tables](core-tables-group.md) . Dans cette section, vous allez ajouter des informations dans la table FeatureComponents de l’exemple du bloc-notes.

Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table FeatureComponents vide.

[Table FeatureComponents](featurecomponents-table.md)



| Fonctionnalité\_ | -\_ |
|-----------|-------------|
| Chaussures  | Chaussures    |
| Concert   | Concert     |
| Jongl     | Jongl       |
| Terrain  | Terrain    |
| Aide      | Aide        |
| Janvier   | Janvier     |
| NewYears  | NewYears    |
| Bloc-notes   | Bloc-notes     |
| Fichier Lisezmoi    | Bloc-notes     |



 

[Continuer](adding-registry-information.md)

 

 



