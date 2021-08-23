---
description: La table AdminExecuteSequence répertorie les actions exécutées par le programme d’installation lorsqu’il appelle l’action d’administration de niveau supérieur. Consultez le groupe tables de procédures d’installation, à l’aide d’une table de séquences et de l’exemple de table de séquence détaillé.
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Importation du AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de646049fed05f881b61c4b635af3bc9d2caed09512a1ec89853066b0ba99c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787379"
---
# <a name="importing-the-adminexecutesequence"></a>Importation du AdminExecuteSequence

La [table AdminExecuteSequence](adminexecutesequence-table.md) répertorie les actions exécutées par le programme d’installation lorsqu’il appelle l' [action d’administration](admin-action.md)de niveau supérieur. Consultez le [groupe tables de procédures d’installation](installation-procedure-tables-group.md), [à l’aide d’une table de séquences](using-a-sequence-table.md)et de l' [exemple de table de séquence détaillé](sequence-table-detailed-example.md).

si, dans la section, vous avez [importé une base de données vide](importing-a-blank-database.md) que vous avez utilisée uisample.msi du kit de développement logiciel (SDK) Windows Installer, les tables de séquence de votre copie de MNP2000.msi contiennent déjà les séquences d’action suggérées décrites dans [utilisation d’une Table de séquences](using-a-sequence-table.md). aucune modification de ces séquences ne doit être nécessaire pour créer l’exemple de package d’installation de Bloc-notes.

Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table AdminExecuteSequence.

[Table AdminExecuteSequence](adminexecutesequence-table.md)



| Action              | Condition | Séquence |
|---------------------|-----------|----------|
| CostFinalize        |           | 1 000     |
| CostInitialize      |           | 800      |
| FileCost            |           | 900      |
| InstallAdminPackage |           | 3900     |
| InstallFiles        |           | 4000     |
| InstallFinalize     |           | 6600     |
| InstallInitialize   |           | 1500     |
| InstallValidate     |           | 1400     |



 

[Continuer](importing-the-adminuisequence.md)

 

 



