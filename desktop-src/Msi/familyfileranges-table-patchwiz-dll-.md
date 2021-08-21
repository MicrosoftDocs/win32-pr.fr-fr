---
description: La table FamilyFileRanges contient des informations sur des fichiers particuliers d’une image mise à niveau avec des plages qui ne doivent jamais être remplacées.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: Table FamilyFileRanges (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0559f4cea1061f9cf0c1438140e7abba8b00908233a1a1d608ae5dbd8b79ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636896"
---
# <a name="familyfileranges-table-patchwizdll"></a>Table FamilyFileRanges (Patchwiz.dll)

La table FamilyFileRanges contient des informations sur des fichiers particuliers d’une image mise à niveau avec des plages qui ne doivent jamais être remplacées. Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La table FamilyFileRanges contient les colonnes suivantes.



| Colonne        | Type | Clé | Nullable |
|---------------|------|-----|----------|
| Famille        | text | O   | N        |
| TCTI           | text | O   | N        |
| RetainOffsets | text |     | N        |
| RetainLengths | text |     | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famille
</dt> <dd>

Clé étrangère vers la colonne Family de la [table ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>TCTI
</dt> <dd>

Clé étrangère dans les [tables de fichiers](file-table.md) de toutes les images mises à niveau dans la famille d’images.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

Décalage des plages qui ne peuvent pas être remplacées. La valeur de ce champ est une liste de valeurs de décalage de plage pour les plages qui ne sont pas remplacées dans les fichiers cibles. L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne RetainLengths.

Les valeurs peuvent être décimales ou hexadécimales. [Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ». Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.

</dd> <dt>

<span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths
</dt> <dd>

Longueur, en octets, des plages qui ne peuvent pas être remplacées. La valeur de ce champ est une liste de valeurs de longueur de plage à conserver dans les fichiers cibles. L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne RetainOffsets.

Les valeurs peuvent être décimales ou hexadécimales. [Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ». Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les décalages et les longueurs entrés dans RetainOffsets et RetainLengths ne doivent pas spécifier des plages qui se chevauchent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mise à jour corrective des régions sélectionnées d’un fichier](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



