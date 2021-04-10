---
description: La table PatchSequence est utilisée pour générer la table MsiPatchSequence dans un correctif. La table requiert la version de PATCHWIZ.DLL disponible avec Windows Installer&\# 160 ; 3.0.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: Table PatchSequence (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382e940d3c0cb6c7be2c8360ab98f2afaf13c799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868846"
---
# <a name="patchsequence-table-patchwizdll"></a>Table PatchSequence (PATCHWIZ.DLL)

La table PatchSequence est utilisée pour générer la [table MsiPatchSequence](msipatchsequence-table.md) dans un correctif. La table requiert la version de [PATCHWIZ.DLL](patchwiz-dll.md) disponible avec Windows Installer 3,0.

Le tableau suivant identifie les colonnes de la table PatchSequence.



| Colonne      | Type       | Clé | Nullable |
|-------------|------------|-----|----------|
| PatchFamily | Identificateur | O   | N        |
| Cible      | Texte       | O   | O        |
| Séquence    | Version    |     | O        |
| Remplacent   | Integer    |     | O        |



 

### <a name="columns"></a>Colonnes

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

Identificateur qui indique les familles de séquence auxquelles ce correctif appartient.

Les valeurs des colonnes Target et PatchFamily définissent ensemble la clé primaire de la table. Un correctif qui appartient à plusieurs familles de séquences, ou qui a des séquences différentes en fonction du code de produit de la cible, peut avoir une ligne pour chaque jumelage. Cette valeur est utilisée pour remplir la colonne PatchFamily de la [table MsiPatchSequence](msipatchsequence-table.md) qui appartient au correctif.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Indicatif
</dt> <dd>

La colonne cible est utilisée pour filtrer les PatchFamily par code de produit.

Une valeur NULL dans cette colonne indique que ce PatchFamily s’applique à toutes les cibles du correctif. Si cette colonne contient une clé étrangère à la [table TargetImages](targetimages-table-patchwiz-dll-.md), le code de produit de l’image spécifiée est récupéré et utilisé pour remplir la valeur de code du produit dans la ligne du nouveau correctif de la [table MsiPatchSequence](msipatchsequence-table.md). Si cette colonne contient un GUID, le GUID est utilisé pour remplir la valeur de code de produit de la ligne dans la table MsiPatchSequence.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence
</dt> <dd>

La valeur dans la colonne séquence est utilisée pour remplir la colonne de séquence de la [table MsiPatchSequence](msipatchsequence-table.md) du nouveau fichier correctif.

Si la valeur est NULL, un numéro de séquence est généré automatiquement.

</dd> <dt>

<span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Remplacent
</dt> <dd>

La valeur **msidbPatchSequenceSupersedeEarlier** ou 1 dans ce champ indique que ce correctif remplace les [petites mises à jour](small-updates.md) antérieures dans les familles de séquence auxquelles ce correctif appartient.

La valeur de cette colonne est utilisée pour définir la colonne d’attributs de la ligne du nouveau correctif dans la [table MsiPatchSequence](msipatchsequence-table.md) .

</dd> </dl>

### <a name="remarks"></a>Notes

Disponible à partir de Windows Installer 3,0.

 

 



