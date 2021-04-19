---
description: La table AdminUISequence répertorie les actions que le programme d’installation appelle lorsqu’il exécute l’action d’administration de niveau supérieur et que le niveau d’interface utilisateur interne a la valeur interface utilisateur complète ou interface utilisateur réduite.
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: Importation du AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541862"
---
# <a name="importing-the-adminuisequence"></a>Importation du AdminUISequence

La [table AdminUISequence](adminuisequence-table.md) répertorie les actions que le programme d’installation appelle lorsqu’il exécute l' [action d’administration](admin-action.md) de niveau supérieur et que le niveau d’interface utilisateur interne a la valeur interface utilisateur complète ou interface utilisateur réduite. Le programme d’installation ignore les actions dans ce tableau si le niveau de l’interface utilisateur est défini sur interface utilisateur de base ou aucune interface utilisateur. Consultez l' [interface utilisateur](user-interface.md) et les [niveaux d’interface utilisateur](user-interface-levels.md). Consultez le [groupe tables de procédures d’installation](installation-procedure-tables-group.md), [à l’aide d’une table de séquences](using-a-sequence-table.md)et de l' [exemple de table de séquence détaillé](sequence-table-detailed-example.md).

Si, dans la section, vous avez [importé une base de données vide](importing-a-blank-database.md) que vous avez utilisée uisample.msi du kit de développement logiciel (SDK) Windows Installer, les tables de séquence de votre copie de MNP2000.msi contiennent déjà les séquences d’action suggérées décrites dans [utilisation d’une table de séquences](using-a-sequence-table.md). Aucune modification de ces séquences ne doit être nécessaire pour installer l’exemple du bloc-notes.

Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table AdminExecuteSequence.

[Table AdminUISequence](adminuisequence-table.md)



| Action          | Condition | Séquence |
|-----------------|-----------|----------|
| AdminWelcomeDlg |           | 1230     |
| CostFinalize    |           | 1 000     |
| CostInitialize  |           | 800      |
| ExecuteAction   |           | 1 300     |
| ExitDlg         |           | -1       |
| FatalErrorDlg   |           | -3       |
| FileCost        |           | 900      |
| PrepareDlg      |           | 140      |
| ProgressDlg     |           | 1 280     |
| UserExitDlg     |           | -2       |



 

[Continuer](importing-the-advtexecutesequence.md)

 

 



