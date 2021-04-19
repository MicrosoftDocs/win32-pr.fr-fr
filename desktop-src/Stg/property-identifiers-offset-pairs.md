---
title: Identificateurs de propriété/paires d’offsets
description: La valeur définie pour la propriété nombre de propriétés est un tableau d’identificateurs de propriété/valeurs de jeu de propriétés de paires d’offsets.
ms.assetid: 341608a1-3ab1-4fa9-ab9a-4124c63c78a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b55ed20aef2c76dc97fcb3f4acfe981b9800308
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106533547"
---
# <a name="property-identifiersoffset-pairs"></a>Identificateurs de propriété/paires d’offsets

La valeur définie pour la propriété nombre de propriétés est un tableau d’identificateurs de propriété/valeurs de jeu de propriétés de paires d’offsets. Les identificateurs de propriété sont des valeurs 32 bits qui identifient de façon unique une propriété dans une section. Les paires décalage indiquent la distance entre le début de la section et le début de la paire type/valeur de la propriété. Étant donné que les décalages sont relatifs à la section, les sections peuvent être copiées sous la forme d’un tableau d’octets.

Les identificateurs de propriété ne sont pas triés dans un ordre particulier. Les propriétés peuvent être omises dans le jeu de propriétés stocké. les lecteurs ne doivent pas compter sur un ordre ou une plage spécifique d’identificateurs de propriété.

 

 




