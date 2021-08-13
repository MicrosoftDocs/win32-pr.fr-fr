---
description: Windows Le programme d’installation peut optimiser la mise à jour corrective pour réduire le temps nécessaire à l’application des correctifs pour les applications installées.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Optimisation des correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee37ba48764f6249410a6dfc2512245aa6ca6dfca68cff09ec15e06a42f9156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627642"
---
# <a name="patch-optimization"></a>Optimisation des correctifs

Windows Le programme d’installation peut optimiser la mise à jour corrective pour réduire le temps nécessaire à l’application des correctifs pour les applications installées.

**Windows Installer 2,0 :** Non pris en charge. pour les versions de Windows Installer publiées avant Windows Installer 3,0, la mise à jour corrective exécute une installation de réparation complète de l’application, ce qui peut prendre beaucoup plus de temps.

**Windows Installer 3,0 et versions ultérieures :** Le processus de mise à jour corrective modifie uniquement les parties d’une application qui sont modifiées par un correctif.

**Windows Installer 3,1 et versions ultérieures :** à partir de Windows Installer 3,1, l’optimisation des correctifs exige que la propriété OptimizedInstallMode de tous les correctifs de la transaction soit définie sur 1 (un) dans la [Table MsiPatchMetadata](msipatchmetadata-table.md).

si un correctif modifie uniquement les tables suivantes, Windows Installer 3,0 ou une version ultérieure ignore les actions associées à toutes les autres tables, même si ces actions sont répertoriées dans les tables de séquence du package d’installation d’application d’origine (fichier .msi).

-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [Condition](condition-table.md)
-   [CustomAction](customaction-table.md)
-   [File](file-table.md)
-   [FileSFPCatalog](filesfpcatalog-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [Média](media-table.md)
-   [MoveFile](movefile-table.md)
-   [MsiAssembly](msiassembly-table.md)
-   [MsiDigitalCertificate](msidigitalcertificate-table.md)
-   [MsiDigitalSignature](msidigitalsignature-table.md)
-   [MsiFileHash](msifilehash-table.md)
-   [MsiPatchHeaders](msipatchheaders-table.md)
-   [Patch](patch-table.md)
-   [PatchPackage](patchpackage-table.md)
-   [Propriété](property-table.md)
-   [Registre](registry-table.md)
-   [SFPCatalog](sfpcatalog-table.md)
-   [Exportation](typelib-table.md)
-   [\_Colonnes](-columns-table.md)
-   [\_Stockages](-storages-table.md)
-   [\_Flux](-streams-table.md)
-   [\_Tables](-tables-table.md)
-   [\_Table TransformView](-transformview-table.md)
-   [\_Validation](-validation-table.md)

Pour désactiver l’option d’optimisation des correctifs, utilisez la stratégie [DisableFlyWeightPatching](disableflyweightpatching.md) .

 

 



