---
description: Vous pouvez contrôler les options d’installation de fonctionnalité disponibles pour les utilisateurs et les applications en créant la table des fonctionnalités et la table des composants.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Contrôle des États de sélection des fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadedf4b6038f8257d06671e0774afc258391898
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210452"
---
# <a name="controlling-feature-selection-states"></a><span data-ttu-id="a4876-103">Contrôle des États de sélection des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="a4876-103">Controlling Feature Selection States</span></span>

<span data-ttu-id="a4876-104">Vous pouvez contrôler les options d’installation de fonctionnalité disponibles pour les utilisateurs et les applications en créant la table des [fonctionnalités](feature-table.md) et la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a4876-104">You can control which feature installation options are available for users and applications to select by authoring the [Feature table](feature-table.md) and [Component table](component-table.md).</span></span>

-   <span data-ttu-id="a4876-105">Pour empêcher la sélection de l’état de publication pour une fonctionnalité, incluez **msidbFeatureAttributesDisallowAdvertise** dans le champ attributs de la fonctionnalité dans le [tableau des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="a4876-105">To prevent selection of the advertise state for a feature, include **msidbFeatureAttributesDisallowAdvertise** in the feature's Attributes field in the [Feature table](feature-table.md).</span></span>
-   <span data-ttu-id="a4876-106">Pour empêcher la sélection des États d’exécution à partir de la source ou d’exécution à partir du réseau pour une fonctionnalité, incluez **msidbComponentAttributesLocalOnly** dans les champs attributs de la [table des composants](component-table.md) pour chaque composant appartenant à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a4876-106">To prevent selection of the run-from-source or run-from-network states for a feature, include **msidbComponentAttributesLocalOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="a4876-107">Si une fonctionnalité n’a pas de composants, les options exécuter à partir de la source et exécuter à partir de mon ordinateur sont toujours disponibles.</span><span class="sxs-lookup"><span data-stu-id="a4876-107">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="a4876-108">Pour empêcher la sélection de l’État exécuter à partir de mon ordinateur pour une fonctionnalité, incluez **msidbComponentAttributesSourceOnly** dans les champs attributs de la [table des composants](component-table.md) pour chaque composant appartenant à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a4876-108">To prevent selection of the run-from-my-computer state for a feature, include **msidbComponentAttributesSourceOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="a4876-109">Si une fonctionnalité n’a pas de composants, les options exécuter à partir de la source et exécuter à partir de mon ordinateur sont toujours disponibles.</span><span class="sxs-lookup"><span data-stu-id="a4876-109">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="a4876-110">Les nouvelles fonctionnalités enfants peuvent être créées en incluant **msidbFeatureAttributesFollowParent** et **msidbFeatureAttributesUIDisallowAbsent** dans le champ attributs du [tableau des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="a4876-110">New child features can be authored by including **msidbFeatureAttributesFollowParent** and **msidbFeatureAttributesUIDisallowAbsent** in the Attributes field of the [Feature table](feature-table.md).</span></span>

 

 



