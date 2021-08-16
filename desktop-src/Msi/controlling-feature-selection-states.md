---
description: Vous pouvez contrôler les options d’installation de fonctionnalité disponibles pour les utilisateurs et les applications en créant la table des fonctionnalités et la table des composants.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Contrôle des États de sélection des fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd269e5b7b0c810df6f7f0909d56b98cdd1c54c9b51eacc40656fe48fc32f8e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379904"
---
# <a name="controlling-feature-selection-states"></a>Contrôle des États de sélection des fonctionnalités

Vous pouvez contrôler les options d’installation de fonctionnalité disponibles pour les utilisateurs et les applications en créant la table des [fonctionnalités](feature-table.md) et la [table des composants](component-table.md).

-   Pour empêcher la sélection de l’état de publication pour une fonctionnalité, incluez **msidbFeatureAttributesDisallowAdvertise** dans le champ attributs de la fonctionnalité dans le [tableau des fonctionnalités](feature-table.md).
-   Pour empêcher la sélection des États d’exécution à partir de la source ou d’exécution à partir du réseau pour une fonctionnalité, incluez **msidbComponentAttributesLocalOnly** dans les champs attributs de la [table des composants](component-table.md) pour chaque composant appartenant à la fonctionnalité. Si une fonctionnalité n’a pas de composants, les options exécuter à partir de la source et exécuter à partir de mon ordinateur sont toujours disponibles.
-   Pour empêcher la sélection de l’État exécuter à partir de mon ordinateur pour une fonctionnalité, incluez **msidbComponentAttributesSourceOnly** dans les champs attributs de la [table des composants](component-table.md) pour chaque composant appartenant à la fonctionnalité. Si une fonctionnalité n’a pas de composants, les options exécuter à partir de la source et exécuter à partir de mon ordinateur sont toujours disponibles.
-   Les nouvelles fonctionnalités enfants peuvent être créées en incluant **msidbFeatureAttributesFollowParent** et **msidbFeatureAttributesUIDisallowAbsent** dans le champ attributs du [tableau des fonctionnalités](feature-table.md).

 

 



