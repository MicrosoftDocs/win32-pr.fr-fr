---
description: Séquences d’actions suggérées pour une table InstalUISequence de base dans une base de données Windows Installer.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: InstallUISequence suggéré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523252"
---
# <a name="suggested-installuisequence"></a>InstallUISequence suggéré



| Action                                          | Condition                                                                                                  | Séquence |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| FatalErrorDlg                                   |                                                                                                            | -3       |
| UserExitDlg                                     |                                                                                                            | -2       |
| ExitDlg                                         |                                                                                                            | -1       |
| [LaunchConditions](launchconditions-action.md) |                                                                                                            | 100      |
| PrepareDlg                                      |                                                                                                            | 140      |
| [AppSearch](appsearch-action.md)               |                                                                                                            | 400      |
| [CCPSearch](ccpsearch-action.md)               | NON [ **installé**](installed.md)                                                                         | 500      |
| [RMCCPSearch](rmccpsearch-action.md)           | NON [ **installé**](installed.md)                                                                         | 600      |
| [CostInitialize](costinitialize-action.md)     |                                                                                                            | 800      |
| [FileCost](filecost-action.md)                 |                                                                                                            | 900      |
| [CostFinalize](costfinalize-action.md)         |                                                                                                            | 1 000     |
| WelcomeDlg                                      | NON [ **installé**](installed.md)                                                                         | 1230     |
| ResumeDlg                                       | [**Installé**](installed.md) ET ( [**reprendre**](resume.md) ou [**présélectionner**](preselected.md))       | 1240     |
| MaintenanceWelcomeDlg                           | [**Installé**](installed.md) ET ne pas [**reprendre**](resume.md) et ne pas [**présélectionner**](preselected.md) | 1250     |
| ProgressDlg                                     |                                                                                                            | 1 280     |
| [ExecuteAction](executeaction-action.md)       |                                                                                                            | 1 300     |



 

 

 



