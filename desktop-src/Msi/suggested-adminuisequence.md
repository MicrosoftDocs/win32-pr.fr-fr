---
description: Séquences d’actions suggérées pour une table AdminUISequence de base dans une base de données Windows Installer.
ms.assetid: a5371133-7d55-4041-8e1f-ecc8245c8d3a
title: AdminUISequence suggéré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af34c0662d19070b1d97b88e8942b2276cc64a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755397"
---
# <a name="suggested-adminuisequence"></a>AdminUISequence suggéré



| Action                                      | Condition | Séquence |
|---------------------------------------------|-----------|----------|
| FatalErrorDlg                               |           | -3       |
| UserExitDlg                                 |           | -2       |
| ExitDlg                                     |           | -1       |
| PrepareDlg                                  |           | 140      |
| [CostInitialize](costinitialize-action.md) |           | 800      |
| [FileCost](filecost-action.md)             |           | 900      |
| [CostFinalize](costfinalize-action.md)     |           | 1 000     |
| AdminWelcomeDlg                             |           | 1230     |
| ProgressDlg                                 |           | 1 280     |
| [ExecuteAction](executeaction-action.md)   |           | 1 300     |



 

 

 



