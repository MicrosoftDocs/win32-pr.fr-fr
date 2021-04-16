---
title: Version de format
description: La valeur de la version de format est un type de données WORD qui est utilisé pour indiquer la version de format de ce flux.
ms.assetid: 38362a45-4f49-4a85-aabe-452ff32c2812
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503019a3bfe3224e4137ac3bfd43fadbe1e15a3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507985"
---
# <a name="format-version"></a>Version de format

La valeur de la version de format est un type de données **Word** qui est utilisé pour indiquer la version de format de ce flux. Il peut s’agir de zéro ou d’un. L’indicateur format-version doit être vérifié lors de la lecture du jeu de propriétés. S’il ne s’agit pas de zéro ou d’un, le flux a été écrit dans une spécification différente et ne peut pas être lu par du code développé conformément à cette spécification.

Les jeux de propriétés avec le format version 1 sont équivalents à la version 0, avec les ajouts suivants :

-   **Noms des propriétés sensibles** à la casse. Les noms de propriété sont stockés dans la propriété dictionnaire réservé, [ID de propriété 0](/windows/desktop/Stg/reserved-property-identifiers). Dans les jeux de propriétés de la version 1, ces noms peuvent respecter la casse. Le respect de la casse est déterminé par la propriété comportement réservé, [ID de propriété 0x80000003](/windows/desktop/Stg/reserved-property-identifiers).
-   **Noms de propriétés de type long**. Les jeux de propriétés de la version 1, contrairement aux jeux de propriétés de la version 0, ne sont pas limités dans la longueur des noms de propriété. Pour plus d’informations sur les noms de propriété, consultez [ID de propriété 0](/windows/desktop/Stg/reserved-property-identifiers) .
-   **Types de propriété**. Les jeux de propriétés de la version 1 peuvent contenir tous les types de propriété qui peuvent être contenus dans un jeu de propriétés de la version 0 plus certains types supplémentaires. Pour plus d’informations sur ces types, consultez la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

 

 