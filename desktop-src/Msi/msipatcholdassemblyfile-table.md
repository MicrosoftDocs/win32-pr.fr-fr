---
description: La table MsiPatchOldAssemblyFile lie un fichier de la table file à un nom d’assembly dans la table MsiPatchOldAssemblyName. Plusieurs anciens noms d’assembly peuvent être associés à un seul fichier.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Table MsiPatchOldAssemblyFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518938"
---
# <a name="msipatcholdassemblyfile-table"></a>Table MsiPatchOldAssemblyFile

La table MsiPatchOldAssemblyFile lie un fichier de la [table file](file-table.md) à un nom d’assembly dans la [table MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md). Plusieurs anciens noms d’assembly peuvent être associés à un seul fichier.

La table MsiPatchOldAssemblyFile contient les colonnes suivantes.



| Colonne     | Type                         | Clé | Nullable |
|------------|------------------------------|-----|----------|
| fichier\_     | [Identificateur](identifier.md) | O   | N        |
| Chargeur\_ | [Identificateur](identifier.md) | O   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_
</dt> <dd>

Clé étrangère vers la [table de fichiers](file-table.md) qui spécifie l’assembly à corriger. Cette colonne fait partie de la clé primaire.

</dd> <dt>

<span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Chargeur\_
</dt> <dd>

Clé étrangère vers la [table MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) qui identifie l’un des anciens noms d’assembly pour l’assembly. Cette colonne fait partie de la clé primaire.

</dd> </dl>

## <a name="remarks"></a>Notes

Windows Installer utilise la table MsiPatchOldAssemblyFile et la [table MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) lors de la mise à jour corrective des assemblys installés dans le global assembly cache (GAC). Lors de la publication d’une version plus récente d’un assembly, le nom fort de l’assembly est modifié. Les deux tables identifient ensemble l’ancien nom d’assembly pour un assembly mis à jour. Cela permet au programme d’installation d’utiliser l’ancien nom d’assembly pour rechercher le fichier d’origine dans le GAC et d’appliquer un correctif binaire. Sans ces informations, le programme d’installation devra peut-être accéder à la source d’installation d’origine afin de corriger un assembly installé dans le GAC.

La table MsiPatchOldAssemblyFile et la [table MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) ne sont pas générées automatiquement par [PatchWiz](patchwiz-dll.md). Le package de mise à jour spécifié dans la [table UpgradedImages](upgradedimages-table-patchwiz-dll-.md) doit contenir ces tables pour que le correctif dispose de ces informations.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



