---
description: séquences d’actions suggérées pour une table AdminExecuteSequence de base dans une base de données Windows Installer.
ms.assetid: c54181d3-a16a-4007-a9ac-03ace98b637e
title: AdminExecuteSequence suggéré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5513dbd120422a9fca2c291401c0e4ba8ed8f376f8a0e080a66f25024b11a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627219"
---
# <a name="suggested-adminexecutesequence"></a>AdminExecuteSequence suggéré



| Action                                                | Condition | Séquence |
|-------------------------------------------------------|-----------|----------|
| [CostInitialize](costinitialize-action.md)           |           | 800      |
| [FileCost](filecost-action.md)                       |           | 900      |
| [CostFinalize](costfinalize-action.md)               |           | 1 000     |
| [InstallValidate](installvalidate-action.md)         |           | 1400     |
| [InstallInitialize](installinitialize-action.md)     |           | 1500     |
| [InstallAdminPackage](installadminpackage-action.md) |           | 3900     |
| [InstallFiles](installfiles-action.md)               |           | 4000     |
| [InstallFinalize](installfinalize-action.md)         |           | 6600     |



 

 

 



