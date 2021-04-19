---
description: Voici un exemple de table de séquences.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Exemple de table de séquence détaillé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4698d5270f2f246fe6e676799ea239e47a950c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518937"
---
# <a name="sequence-table-detailed-example"></a>Exemple de table de séquence détaillé

Voici un exemple de table de séquences.



| Action                                          | Condition                                                       | Séquence |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [LaunchConditions](launchconditions-action.md) |                                                                 |          |
| [AppSearch](appsearch-action.md)               |                                                                 | 200      |
| [CCPSearch](ccpsearch-action.md)               | \_test CCP                                                       | 300      |
| CCPDialog                                       | PAS \_ de \_ réussite CCP                                               | 400      |
| MyCustomConfig                                  | NON [ **installé**](installed.md)                              | 500      |
| [CostInitialize](costinitialize-action.md)     |                                                                 | 600      |
| [FileCost](filecost-action.md)                 |                                                                 | 700      |
| [CostFinalize](costfinalize-action.md)         |                                                                 | 800      |
| InstallDialog                                   | NON [ **installé**](installed.md)                              | 900      |
| MaintenanceDialog                               | [**Installé**](installed.md) ET ne pas [ **reprendre**](resume.md) | 1 000     |
| ActionDialog                                    |                                                                 | 1100     |
| [RegisterProduct](registerproduct-action.md)   |                                                                 | 1200     |
| [InstallValidate](installvalidate-action.md)   |                                                                 | 1 300     |
| [InstallFiles](installfiles-action.md)         |                                                                 | 1400     |
| MyCustomAction                                  | $MyComponent > 2                                             | 1500     |
| [InstallFinalize](installfinalize-action.md)   |                                                                 | 1 600     |



 

Les actions suivantes dans cette table de séquences sont définies par le programme d’installation et sont des exemples d’actions standard :

[LaunchConditions](launchconditions-action.md)

 

[AppSearch](appsearch-action.md)

 

[CCPSearch](ccpsearch-action.md)

 

[CostInitialize](costinitialize-action.md)

 

[FileCost](filecost-action.md)

 

[CostFinalize](costfinalize-action.md)

 

[RegisterProduct](registerproduct-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallValidate](installvalidate-action.md)

Les actions suivantes ont été définies par l’auteur de la table et sont des exemples d' [actions personnalisées](custom-actions.md) et doivent être répertoriées dans la [table CustomAction](customaction-table.md):

MyCustomConfig

 

MyCustomAction

Les entrées restantes du champ action sont des clés étrangères dans la [table Dialog](dialog-table.md). Ils spécifient les noms des boîtes de dialogue qui s’affichent si le champ condition prend la valeur true.

CCPDialog

 

InstallDialog

 

MaintenanceDialog

 

ActionDialog

Dans la colonne condition, le programme d’installation ignore l’action si la propriété ou l’expression dans ce champ a la valeur false. La propriété [**installed**](installed.md) et la propriété [**Resume**](resume.md) sont des exemples de propriétés définies par le programme d’installation. La propriété [**installed**](installed.md) a la valeur true si le produit est déjà installé et que la propriété [**Resume**](resume.md) est définie si la reprise d’une installation a été interrompue. Le \_ test CCP et les \_ Propriétés de réussite non CCP \_ sont des exemples de propriétés qui peuvent être définies sur la ligne de commande par l’utilisateur qui installe l’application.

Toutes les actions s’exécutent en séquence avec les étapes conditionnelles suivantes :

-   Le CPPSearch est exécuté uniquement si le \_ test CCP est défini.
-   CCPDialog est exécuté uniquement si la \_ réussite du CCP n' \_ est pas définie.
-   MaintenanceDialog est exécuté uniquement si ce produit est déjà installé et s’il ne s’agit pas d’une installation qui est reprise après avoir été suspendue.
-   MyCustomAction est exécuté uniquement si l’expression dans la colonne condition a la valeur true. L’expression $MyComponent > 2 fait référence à l’état d’action du composant appelé MyComponent. Cette condition indique que MyCustomAction doit être exécuté uniquement si MonComposant est configuré pour être installé. Pour plus d’informations sur les États d’action et les États de sélection, consultez la propriété [**FeatureRequestState**](session-featurerequeststate.md) , la [table de fonctionnalités](feature-table.md)et l' [action InstallFiles](installfiles-action.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de propriétés](using-properties.md)
</dt> <dt>

[Syntaxe d’instruction conditionnelle](conditional-statement-syntax.md)
</dt> </dl>

 

 



