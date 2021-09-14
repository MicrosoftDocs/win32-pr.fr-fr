---
description: ICEM03 vérifie que toutes les actions du module sont des actions de base ou qu’elles dérivent d’une action de base valide.
ms.assetid: 8e2b5921-32cf-45e8-9906-30002574a712
title: ICEM03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f368fa50a71153c41eebaa9ee5084449cf824993
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021444"
---
# <a name="icem03"></a>ICEM03

ICEM03 vérifie que toutes les actions du module sont des actions de base ou qu’elles dérivent d’une action de base valide.

Le module de fusion CIEM est stocké dans un fichier de module de fusion. CUB appelé Mergemod. CUB et non dans le fichier. CUB contenant le CIEM utilisé pour la validation du package.

## <a name="result"></a>Résultats

ICEM03 publie les messages d’erreur pour un module contenant des actions dans une table de séquences qui n’est pas une action de base ou qui est dérivée d’une action de base valide.

## <a name="example"></a>Exemple

ICEM03 publie les messages d’erreur suivants pour un module contenant les entrées de base de données présentées ci-dessous.

``` syntax
The action 'Action1' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
The action 'Action2' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
```

[Table ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Action  | Séquence | BaseAction | Après | Condition |
|---------|----------|------------|-------|-----------|
| Action1 |          | Action2    | 0     |           |
| Action2 |          | Action1    | 0     |           |



 

ICEM03 publie des erreurs pour ces deux actions, car elles font référence les unes aux autres comme des actions de base dans la table ModuleInstallExecuteSequence. Toutes les actions dans les tables [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md)et [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) doivent être des actions de base ou dériver leur position de la combinaison d’une autre action et d’un indicateur Before et after.

Pour corriger cette erreur, déterminez les actions de base pour les deux actions. Ajoutez un enregistrement pour les actions de base avec un numéro de séquence par défaut. Pour action1 et action2, entrez les noms des actions de base dans la colonne BaseAction et 0 ou 1 dans la colonne après.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE du module de fusion](merge-module-ice-reference.md)
</dt> </dl>

 

 



