---
description: Le tableau InstallExecuteSequence répertorie les actions qui sont exécutées lorsque le programme d’installation exécute l’action d’installation de niveau supérieur. Consultez le groupe tables de procédures d’installation, à l’aide d’une table de séquences et de l’exemple de table de séquence détaillé.
ms.assetid: cdd4f02a-cfe6-4a23-9fc2-f4cb810379aa
title: Importation du InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586557130c6aa9af197d5d28f6bd750f4de736feb6982f3b7f12ce73ccf41c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430769"
---
# <a name="importing-the-installexecutesequence"></a>Importation du InstallExecuteSequence

Le [tableau InstallExecuteSequence](installexecutesequence-table.md) répertorie les actions qui sont exécutées lorsque le programme d’installation exécute l' [action d’installation](install-action.md)de niveau supérieur. Consultez le [groupe tables de procédures d’installation](installation-procedure-tables-group.md), [à l’aide d’une table de séquences](using-a-sequence-table.md)et de l' [exemple de table de séquence détaillé](sequence-table-detailed-example.md).

si, dans la section, vous avez [importé une base de données vide](importing-a-blank-database.md) que vous avez utilisée uisample.msi du kit de développement logiciel (SDK) Windows Installer, les tables de séquence de votre copie de MNP2000.msi contiennent déjà les séquences d’action suggérées décrites dans [utilisation d’une Table de séquences](using-a-sequence-table.md). aucune modification de ces séquences n’est nécessaire pour créer le package d’installation Bloc-notes.

Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table InstallExecuteSequence.

[Table InstallExecuteSequence](installexecutesequence-table.md)



| Action                   | Condition     | Séquence |
|--------------------------|---------------|----------|
| AllocateRegistrySpace    | NON installé | 1550     |
| AppSearch                |               | 400      |
| BindImage                |               | 4300     |
| CCPSearch                | NON installé | 500      |
| CostFinalize             |               | 1 000     |
| CostInitialize           |               | 800      |
| CreateFolders            |               | 3700     |
| CreateShortcuts          |               | 4500     |
| DeleteServices           | VersionNT     | 2000     |
| DuplicateFiles           |               | 4210     |
| FileCost                 |               | 900      |
| FindRelatedProducts      |               | 200      |
| InstallFiles             |               | 4000     |
| InstallFinalize          |               | 6600     |
| InstallInitialize        |               | 1500     |
| InstallODBC              |               | 5400     |
| InstallServices          | VersionNT     | 5800     |
| InstallValidate          |               | 1400     |
| LaunchConditions         |               | 100      |
| MigrateFeatureStates     |               | 1200     |
| MoveFiles                |               | 3 800     |
| PatchFiles               |               | 4090     |
| ProcessComponents        |               | 1 600     |
| PublishComponents        |               | 6200     |
| PublishFeatures          |               | 6300     |
| PublishProduct           |               | 6 400     |
| RegisterClassInfo        |               | 4600     |
| RegisterComPlus          |               | 5700     |
| RegisterExtensionInfo    |               | 4700     |
| RegisterFonts            |               | 5300     |
| RegisterMIMEInfo         |               | 4900     |
| RegisterProduct          |               | 6100     |
| RegisterProgIdInfo       |               | 4 800     |
| RegisterTypeLibraries    |               | 5500     |
| RegisterUser             |               | 6000     |
| RemoveDuplicateFiles     |               | 3400     |
| RemoveEnvironmentStrings |               | 3300     |
| RemoveExistingProducts   |               | 6700     |
| RemoveFiles              |               | 3 500     |
| RemoveFolders            |               | 3600     |
| RemoveIniValues          |               | 3100     |
| RemoveODBC               |               | 2 400     |
| RemoveRegistryValues     |               | 2600     |
| RemoveShortcuts          |               | 3200     |
| RMCCPSearch              | NON installé | 600      |
| SelfRegModules           |               | 5600     |
| SelfUnregModules         |               | 2 200     |
| SetODBCFolders           |               | 1100     |
| StartServices            | VersionNT     | 5900     |
| StopServices             | VersionNT     | 1900     |
| UnpublishComponents      |               | 1 700     |
| UnpublishFeatures        |               | 1800     |
| UnregisterClassInfo      |               | 2700     |
| UnregisterComPlus        |               | 2100     |
| UnregisterExtensionInfo  |               | 2 800     |
| UnregisterFonts          |               | 2 500     |
| UnregisterMIMEInfo       |               | 3000     |
| UnregisterProgIdInfo     |               | 2900     |
| UnregisterTypeLibraries  |               | 2300     |
| ValidateProductID        |               | 700      |
| WriteEnvironmentStrings  |               | 5200     |
| WriteIniValues           |               | 5100     |
| WriteRegistryValues      |               | 5 000     |



 

[Continuer](importing-the-installuisequence.md)

 

 



