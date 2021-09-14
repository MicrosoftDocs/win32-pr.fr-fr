---
description: La table AdvtExecuteSequence répertorie les actions que le programme d’installation appelle lorsqu’il exécute l’action de publication de niveau supérieur. Consultez le groupe tables de procédures d’installation, à l’aide d’une table de séquences et de l’exemple de table de séquence détaillé.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importation du AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021382"
---
# <a name="importing-the-advtexecutesequence"></a>Importation du AdvtExecuteSequence

La [table AdvtExecuteSequence](advtexecutesequence-table.md) répertorie les actions que le programme d’installation appelle lorsqu’il exécute l' [action de publication](advertise-action.md)de niveau supérieur. Consultez le [groupe tables de procédures d’installation](installation-procedure-tables-group.md), [à l’aide d’une table de séquences](using-a-sequence-table.md)et de l' [exemple de table de séquence détaillé](sequence-table-detailed-example.md).

si, dans la section, vous avez [importé une base de données vide](importing-a-blank-database.md) que vous avez utilisée uisample.msi du kit de développement logiciel (SDK) Windows Installer, les tables de séquence de votre copie de MNP2000.msi contiennent déjà les séquences d’action suggérées décrites dans [utilisation d’une table de séquences](using-a-sequence-table.md). aucune modification de ces séquences ne doit être nécessaire pour créer l’exemple de package d’installation de Bloc-notes.

Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la [table AdvtExecuteSequence](advtexecutesequence-table.md).

[Table AdvtExecuteSequence](advtexecutesequence-table.md)



| Action                | Condition | Séquence |
|-----------------------|-----------|----------|
| CostFinalize          |           | 1 000     |
| CostInitialize        |           | 800      |
| CreateShortcuts       |           | 4500     |
| InstallFinalize       |           | 6600     |
| InstallInitialize     |           | 1500     |
| InstallValidate       |           | 1400     |
| PublishComponents     |           | 6200     |
| PublishFeatures       |           | 6300     |
| PublishProduct        |           | 6 400     |
| RegisterClassInfo     |           | 4600     |
| RegisterExtensionInfo |           | 4700     |
| RegisterMIMEInfo      |           | 4900     |
| RegisterProgIdInfo    |           | 4 800     |



 

La [table AdvtUISequence](advtuisequence-table.md) n’est pas utilisée par le programme d’installation. Cette table ne doit pas exister ou rester vide dans la base de données d’installation.

[Continuer](adding-summary-information.md)

 

 



