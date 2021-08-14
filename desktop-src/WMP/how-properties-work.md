---
title: Fonctionnement des propriétés
description: Fonctionnement des propriétés
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Lecteur Windows Media les plug-ins, exemples de propriétés Echo
- plug-ins, exemples de propriétés d’écho
- plug-ins de traitement de signal numérique, exemples de propriétés Echo
- Plug-ins DSP, exemples de propriétés Echo
- Echo DSP, exemple de plug-in, propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdefea3fce39b70d20d2f100d36cc4aeb8770bd15cd5cd0bf0978cd08f2259f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339133"
---
# <a name="how-properties-work"></a>Fonctionnement des propriétés

Les valeurs de propriété sont stockées dans des variables membres.

Les propriétés sont rendues accessibles par les paires de méthodes. Une méthode fournit l’implémentation pour spécifier la valeur de la propriété ; son nom commence par put \_ . L’autre méthode fournit l’implémentation pour récupérer la valeur de la propriété ; son nom commence par la fonction obtient \_ . La définition de l’interface se trouve dans Echo. idl. Les prototypes de méthode de propriété se trouvent dans Echo. h. Elles sont implémentées dans Echo. cpp.

Les trois sections suivantes vous montrent comment modifier les méthodes de propriété existantes en fonction de vos besoins et comment ajouter les méthodes pour une propriété supplémentaire.

-   [Variables pour stocker les propriétés](variables-to-store-properties.md)
-   [Modification de la propriété Scale](modifying-the-scale-property.md)
-   [Ajout de la propriété de combinaison humide](adding-the-wet-mix-property.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemples de propriétés Echo**](echo-sample-properties.md)
</dt> </dl>

 

 




