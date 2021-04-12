---
description: La séquence de l’interface utilisateur est importée dans l’exemple de base de données.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importation du InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203775"
---
# <a name="importing-the-installuisequence"></a>Importation du InstallUISequence

La [table InstallUISequence](installuisequence-table.md) répertorie les actions qui sont exécutées lorsque l' [action d’installation](install-action.md) de niveau supérieur est exécutée et que le niveau d’interface utilisateur interne est défini sur interface utilisateur complète ou réduite. Le programme d’installation ignore les actions dans ce tableau si le niveau de l’interface utilisateur est défini sur interface utilisateur de base ou sur aucune interface utilisateur. Consultez l' [interface utilisateur](user-interface.md) et les [niveaux d’interface utilisateur](user-interface-levels.md). Consultez le [groupe tables de procédures d’installation](installation-procedure-tables-group.md), [à l’aide d’une table de séquences](using-a-sequence-table.md)et de l' [exemple de table de séquence détaillé](sequence-table-detailed-example.md).

Si, dans la section, vous avez [importé une base de données vide](importing-a-blank-database.md) que vous avez utilisée uisample.msi du kit de développement logiciel (SDK) Windows Installer, les tables de séquence de votre copie de MNP2000.msi contiennent déjà les séquences d’action suggérées décrites dans [utilisation d’une table de séquences](using-a-sequence-table.md). Aucune modification de ces séquences ne doit être nécessaire pour créer le package d’installation du bloc-notes.

Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table InstallUISequence.

[Table InstallUISequence](installuisequence-table.md)



| Action                | Condition                                    | Séquence |
|-----------------------|----------------------------------------------|----------|
| AppSearch             |                                              | 400      |
| CCPSearch             | NON installé                                | 500      |
| CostFinalize          |                                              | 1 000     |
| CostInitialize        |                                              | 800      |
| ExecuteAction         |                                              | 1 300     |
| ExitDlg               |                                              | -1       |
| FatalErrorDlg         |                                              | -3       |
| FileCost              |                                              | 900      |
| LaunchConditions      |                                              | 100      |
| MaintenanceWelcomeDlg | Installé et ne reprend pas et n’est pas présélectionné | 1250     |
| PrepareDlg            |                                              | 140      |
| ProgressDlg           |                                              | 1 280     |
| ResumeDlg             | Installé et (reprise ou présélection)        | 1240     |
| RMCCPSearch           | NON installé                                | 600      |
| UserExitDlg           |                                              | -2       |
| WelcomeDlg            | NON installé                                | 1230     |
| MigrateFeatureStates  |                                              | 1200     |
| FindRelatedProducts   |                                              | 200      |



 

[Continuer](importing-the-adminexecutesequence.md)

 

 



