---
description: Les propriétés publiques peuvent être créées dans la base de données d’installation de la même façon que les propriétés privées.
ms.assetid: 032aa55f-d97a-4455-bd32-571b0e05763b
title: Propri&#233;t&#233;s publiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822dfc55e0ab659e5580580edd04eb156540cb61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009732"
---
# <a name="public-properties"></a>Propri&#233;t&#233;s publiques

Les propriétés publiques peuvent être créées dans la base de données d’installation de la même façon que les [propriétés privées](private-properties.md). En outre, les valeurs des propriétés publiques peuvent être modifiées par un utilisateur ou un administrateur système en définissant la propriété sur la ligne de commande, en appliquant une transformation ou en interagissant avec une interface utilisateur créée. Les noms de propriétés publiques ne peuvent pas contenir de lettres minuscules. Consultez [restrictions sur les noms de propriété](restrictions-on-property-names.md).

Les propriétés publiques sont généralement définies par les utilisateurs lors de l’installation. Par exemple, la propriété publique [**INSTALLLEVEL**](installlevel.md) peut être spécifiée sur la ligne de commande utilisée pour lancer l’installation ou choisie à l’aide d’une interface utilisateur créée.

Les valeurs de propriété publiques peuvent être substituées soit sur une ligne de commande, soit à l’aide d’une action [standard](standard-actions.md) ou [personnalisée](custom-actions.md) , en appliquant une transformation, soit en demandant à l’utilisateur d’interagir avec une interface utilisateur créée. Pour effacer une propriété publique dans la table de propriétés, laissez-la hors de la table. Les propriétés qui doivent être définies par l’interface utilisateur pendant l’installation, puis transmises à la phase d’exécution de l’installation doivent être publiques.

Pour obtenir la liste des propriétés publiques standard utilisées par le programme d’installation, consultez Référence de la [propriété](property-reference.md). Un auteur peut également définir une propriété publique personnalisée en entrant le nom de la propriété et une valeur initiale dans la [table des propriétés](property-table.md). Toutes les propriétés publiques peuvent être remplacées par tous les utilisateurs si l’une des conditions suivantes est remplie.

-   L’utilisateur est un administrateur système.
-   La stratégie de EnableUserControl par ordinateur est définie sur 1. Consultez [stratégie système](system-policy.md).
-   La propriété [**EnableUserControl**](-enableusercontrol.md) a la valeur 1.
-   Il s’agit d’une installation non gérée qui n’est pas effectuée avec des privilèges élevés.

Si aucune des conditions ci-dessus n’est vraie, le programme d’installation limite par défaut les propriétés publiques qui peuvent être remplacées par un utilisateur qui n’est pas un administrateur système. Consultez [**propriétés publiques restreintes**](restricted-public-properties.md).

 

 



