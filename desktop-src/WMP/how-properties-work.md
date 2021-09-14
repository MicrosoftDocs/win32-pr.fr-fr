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
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416238"
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

 

 




