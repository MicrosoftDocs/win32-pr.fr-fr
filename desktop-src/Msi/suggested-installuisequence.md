---
description: séquences d’actions suggérées pour une table InstalUISequence de base dans une base de données Windows Installer.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: InstallUISequence suggéré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab5c65ed594cf86f86555de235d0ceb0530b9f3e233bfdf5c38d094ca9719a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624331"
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



 

 

 



