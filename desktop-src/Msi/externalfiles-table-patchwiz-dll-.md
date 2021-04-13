---
description: La table ExternalFiles contient des informations sur des fichiers spécifiques qui ne font pas partie d’une image cible normale.
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: Table ExternalFiles (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f0002961408be9f43685ef40cd2ccff729e48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528197"
---
# <a name="externalfiles-table-patchwizdll"></a>Table ExternalFiles (Patchwiz.dll)

La table ExternalFiles contient des informations sur des fichiers spécifiques qui ne font pas partie d’une image cible normale. Ces fichiers peuvent exister dans des produits qui ont été mis à jour par un autre produit, une mise à niveau ou un correctif. Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La table ExternalFiles contient les colonnes suivantes.



| Colonne        | Type    | Clé | Nullable |
|---------------|---------|-----|----------|
| Famille        | text    | O   | N        |
| TCTI           | text    | O   | N        |
| FilePath      | text    | O   | N        |
| SymbolPaths   | text    |     | O        |
| IgnoreOffsets | text    |     | O        |
| IgnoreLengths | text    |     | O        |
| RetainOffsets | text    |     | N        |
| Commande         | entier |     | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famille
</dt> <dd>

Clé étrangère vers la colonne Family de la [table ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>TCTI
</dt> <dd>

Clé étrangère dans la [table de fichiers](file-table.md) du fichier. msi de l’image mise à niveau.

</dd> <dt>

<span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>Cheminfichier
</dt> <dd>

Chemin d’accès complet du fichier externe, y compris le nom du fichier. Le champ FilePath est utilisé pour localiser le fichier spécifié dans la colonne TCTI.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Chemin d’accès complet dans lequel les fichiers de symboles du fichier spécifiés dans la colonne TCTI sont recherchés.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

La valeur de ce champ est une liste délimitée par des virgules de nombres de décalages de plage pour les plages à ignorer dans le fichier externe. L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne IgnoreLengths. Cette colonne est facultative.

Les valeurs peuvent être décimales ou hexadécimales. [Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ». Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

La valeur de ce champ est une liste délimitée par des virgules de longueurs de plage, en octets, pour les plages à ignorer dans le fichier externe. L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne IgnoreOffsets. Cette colonne est facultative.

Les valeurs peuvent être décimales ou hexadécimales. [Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ». Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

La valeur de ce champ est une liste délimitée par des virgules de nombres de décalages de plage pour les plages à conserver dans le fichier externe. L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne RetainOffsets de l’enregistrement correspondant dans la [table FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).

Les valeurs peuvent être décimales ou hexadécimales. [Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ». Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordre
</dt> <dd>

Si deux versions ou plus sont spécifiées pour le même fichier externe, la table peut contenir plusieurs enregistrements avec des valeurs correspondantes dans les champs TCTI et Family. Dans ce cas, le champ order peut spécifier l’ordre des fichiers externes à utiliser lors de la création du correctif. L’ordre passe de la version la plus ancienne à la plus récente.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette table accepte les variables d’environnement en tant que chemins d’accès commençant par la version 4,0 de Patchwiz.dll.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mise à jour corrective des régions sélectionnées d’un fichier](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



