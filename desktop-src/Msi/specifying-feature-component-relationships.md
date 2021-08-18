---
description: chaque fonctionnalité de Windows Installer utilise un ou plusieurs composants Windows Installer, et les fonctionnalités peuvent partager des composants.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Spécification des relations Feature-Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1d7a79e35822d5a0ad67f43297ec461eb3c2fd766c946cc414a571c148de5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627869"
---
# <a name="specifying-feature-component-relationships"></a>Spécification des relations Feature-Component

chaque [fonctionnalité de Windows Installer](windows-installer-features.md) utilise un ou plusieurs [composants Windows Installer](windows-installer-components.md), et les fonctionnalités peuvent partager des composants. La [table FeatureComponents](featurecomponents-table.md) définit la relation entre les fonctionnalités et les composants. pour plus d’Windows Installer vue d’ensemble, consultez le groupe et les [composants et fonctionnalités](components-and-features.md) [principaux des Tables](core-tables-group.md) . dans cette section, vous allez ajouter des informations dans la table FeatureComponents de l’exemple Bloc-notes.

Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table FeatureComponents vide.

[Table FeatureComponents](featurecomponents-table.md)



| Fonctionnalité\_ | Composant\_ |
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

 

 



