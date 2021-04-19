---
description: ICE68 vérifie que tous les types d’action personnalisés nécessaires pour une installation sont valides.
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532160"
---
# <a name="ice68"></a>ICE68

ICE68 vérifie que tous les types d’action personnalisés nécessaires pour une installation sont valides. L’échec de la résolution de l’erreur signalée par ICE68 provoque l’échec d’une installation qui tente d’exécuter l’action. ICE68 émet un avertissement si l’attribut **msidbCustomActionTypeNoImpersonate** est défini sans définir également l’attribut **msidbCustomActionTypeInScript** .

## <a name="result"></a>Résultats

ICE68 retourne une erreur si un type d’action requis pour une installation n’est pas valide.

## <a name="example"></a>Exemple

ICE68 publie l’avertissement suivant si une action personnalisée a le bit **msidbCustomActionTypeNoImpersonate** défini dans le champ type de la table CustomAction sans que le **msidbCustomActionTypeInScript** soit également défini.

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

Pour résoudre cet avertissement, incluez **msidbCustomActionTypeInScript** (0x400) si l’action personnalisée inclut **msidbCustomActionTypeNoImpersonate** (0x800). Dans le cas contraire, le programme d’installation ignore l’attribut **msidbCustomActionTypeNoImpersonate** . Pour plus d’informations, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).

ICE68 signale l’erreur suivante pour l’exemple ci-dessous :

``` syntax
Invalid custom action type for action 'Action1'.
```

1027 n’est pas un type d’action valide.

Pour corriger cette erreur, choisissez un type d’action personnalisé valide.

[Table CustomAction](customaction-table.md) (partielle)



| Action  | Type | Source   | Cible     |
|---------|------|----------|------------|
| Action1 | 1027 | Argument | Composant1 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



