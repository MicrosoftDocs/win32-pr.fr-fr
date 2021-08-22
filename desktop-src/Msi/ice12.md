---
description: ICE12 valide les tables CustomAction, Directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence et InstallUISequence de la base de données Windows Installer.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef427ca1567680aa9a9f2a598f5a94cb8dee545487afcf3eb1fbb8d1f350fd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262259"
---
# <a name="ice12"></a>ICE12

ICE12 interroge les tables [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md)et [InstallUISequence](installuisequence-table.md) pour valider les éléments suivants :

-   Que l' [action CostFinalize](costfinalize-action.md) se produit dans n’importe quelle table de séquences contenant des actions de type [action personnalisée 35](custom-action-type-35.md) ou [type d’action personnalisé 51](custom-action-type-51.md).
-   Que chaque [type d’action personnalisé 35](custom-action-type-35.md) vient après l' [action CostFinalize](costfinalize-action.md). dans les tables de séquence.
-   Chaque [type d’action personnalisé 51](custom-action-type-51.md) qui a une clé étrangère dans la table de répertoires de la colonne source de la table CustomAction vient avant l' [action CostFinalize](costfinalize-action.md) dans les tables de séquence.

Notez que ICE12 ne valide pas le texte mis en forme dans la colonne cible de la table CustomAction.

## <a name="result"></a>Résultat

ICE12 publie un message d’erreur si la validation des actions personnalisées qui définissent une propriété de répertoire échoue.

## <a name="example"></a> Exemple

ICE12 publie trois erreurs pour l’exemple indiqué.

-   Pour CA1, le dossier’mondossier’est introuvable dans la table de répertoire
-   Pour CA2, la séquence « 80 » est antérieure à CostFinalize dans la table InstallExecuteSequence. Il doit venir après ( CF@100 )
-   Pour CA3, la séquence « 125 » vient après CostFinalize dans la table InstallExecuteSequence. Il doit précéder ( CF@100 )

[Table CustomAction](customaction-table.md) (partielle)



| Action | Type | Source        |
|--------|------|---------------|
| AC1    | 35   | Mondossier      |
| CA2    | 35   | WindowsFolder |
| CA3    | 51   | WindowsFolder |



 

[Table de répertoire](directory-table.md)



| Répertoire     | Répertoire \_ parent | DefaultDir    |
|---------------|-------------------|---------------|
| TARGETDIR     |                   | SourceDir     |
| WindowsFolder | TARGETDIR         | WindowsFolder |



 

[Table InstallExecuteSequence](installexecutesequence-table.md) (partielle)



| Action       | Séquence |
|--------------|----------|
| CostFinalize | 100      |
| CA2          | 80       |
| CA3          | 125      |



 

Pour corriger l’erreur pour CA1, remplacez son entrée dans la colonne source de la table CustomAction par une entrée existante dans la table Directory ou ajoutez la valeur mondossier à la table Directory.

Pour corriger l’erreur pour CA2, modifiez sa séquence dans la table InstallExecuteSequence de sorte qu’elle figure après l’action CostFinalize.

Pour corriger l’erreur pour CA3, modifiez sa séquence dans la table InstallExecuteSequence de sorte qu’elle précède l’action CostFinalize.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



