---
description: La \_ table TargetFiles OptionalData contient des informations sur des fichiers spécifiques dans une image cible. Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction UiCreatePatchPackageEx.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: Table TargetFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5664e2e21968cb3fee5ce3d606dd07008f2436c4b649a7bcefeebd77df9cf6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623734"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a>TargetFiles \_ OptionalData, table (Patchwiz.dll)

La \_ table TargetFiles OptionalData contient des informations sur des fichiers spécifiques dans une image cible. Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La \_ table TargetFiles OptionalData contient les colonnes suivantes.



| Colonne        | Type | Clé | Nullable |
|---------------|------|-----|----------|
| Cible        | text | O   | N        |
| TCTI           | text | O   | N        |
| SymbolPaths   | text |     | O        |
| IgnoreOffsets | text |     | O        |
| IgnoreLengths | text |     | O        |
| RetainOffsets | text |     | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Indicatif
</dt> <dd>

Clé étrangère vers la colonne cible de la [table TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>TCTI
</dt> <dd>

Clé étrangère dans la [table de fichiers](file-table.md) de l’image cible.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

La valeur de ce champ est ajoutée à la liste de dossiers délimités par des points-virgules dans la colonne SymbolPaths de la [table TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) lorsque le correctif est généré et peut être utilisé pour ajouter des fichiers de symboles pour un fichier spécifique.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

La valeur de ce champ est une liste délimitée par des virgules de nombres de décalages de plage pour les plages à ignorer dans le fichier cible. L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne IgnoreLengths. Cette colonne est facultative.

Les valeurs peuvent être décimales ou hexadécimales. [Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ». Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

La valeur de ce champ est une liste délimitée par des virgules de longueurs de plage, en octets, pour les plages à ignorer dans le fichier cible. L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne IgnoreOffsets. Cette colonne est facultative.

Les valeurs peuvent être décimales ou hexadécimales. [Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ». Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

La valeur de ce champ est une liste délimitée par des virgules de nombres de décalages de plage pour les plages à conserver dans le fichier cible. L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne RetainOffsets de l’enregistrement correspondant dans la [table FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)

Les valeurs peuvent être décimales ou hexadécimales. [Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ». Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mise à jour corrective des régions sélectionnées d’un fichier](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



