---
description: La table MsiPatchOldAssemblyName spécifie l’ancien nom d’un assembly.
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: Table MsiPatchOldAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319914"
---
# <a name="msipatcholdassemblyname-table"></a>Table MsiPatchOldAssemblyName

La table MsiPatchOldAssemblyName spécifie l’ancien nom d’un assembly.

La table MsiPatchOldAssemblyName contient les colonnes suivantes.



| Colonne   | Type                         | Clé | Nullable |
|----------|------------------------------|-----|----------|
| Assembly | [Identificateur](identifier.md) | O   | N        |
| Nom     | [Text](text.md)             | O   | N        |
| Valeur    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Chargeur
</dt> <dd>

Identificateur unique de l’ancien nom de l’assembly. Cette clé est utilisée comme mappage entre cette table et la [table MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md).

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Nom de l’attribut associé à la valeur spécifiée dans la colonne valeur.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Valeur associée au nom spécifié dans la colonne nom.

</dd> </dl>

## <a name="remarks"></a>Notes

Windows Installer utilise la table [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) et la table MsiPatchOldAssemblyName lors de la mise à jour corrective des assemblys installés dans le global assembly cache (GAC). Lors de la publication d’une version plus récente d’un assembly, le nom fort de l’assembly est modifié. Les deux tables identifient ensemble l’ancien nom d’assembly pour un assembly mis à jour. Cela permet au programme d’installation d’utiliser l’ancien nom d’assembly pour rechercher le fichier d’origine dans le GAC et d’appliquer un correctif binaire. Sans ces informations, le programme d’installation devra peut-être accéder à la source d’installation d’origine afin de corriger un assembly installé dans le GAC.

La table [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) et la table MsiPatchOldAssemblyName ne sont pas générées automatiquement par [PatchWiz](patchwiz-dll.md). Le package de mise à jour spécifié dans la [table UpgradedImages](upgradedimages-table-patchwiz-dll-.md) doit contenir ces tables pour que le correctif dispose de ces informations.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



