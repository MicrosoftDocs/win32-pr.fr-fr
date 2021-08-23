---
description: La table MsiPatchSequence contient toutes les informations requises par le programme d’installation pour déterminer la séquence d’application d’un correctif logiciel de petite mise à jour par rapport à tous les autres correctifs.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Table MsiPatchSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc529c0f7d1a4cdd1bab568f64507922d6e28f539636600f88dea603c4fe1a52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519799"
---
# <a name="msipatchsequence-table"></a>Table MsiPatchSequence

La table MsiPatchSequence contient toutes les informations requises par le programme d’installation pour déterminer la séquence d’application d’un correctif logiciel de [petite mise à jour](small-updates.md) par rapport à tous les autres correctifs. La table doit se trouver dans la base de données du fichier correctif et non dans une transformation dans le correctif. Le programme d’installation ignore cette table lorsque vous appliquez un correctif de [mise à niveau majeure](major-upgrades.md) . Lors de l’application d’un correctif de [mise à niveau mineure](minor-upgrades.md) , le programme d’installation utilise uniquement cette table pour identifier les correctifs remplacés qui ne doivent pas être séquencés.

La **table MsiPatchSequence** contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| PatchFamily | [Identificateur](identifier.md) | O   | N        |
| ProductCode | [GUID](guid.md)             | O   | O        |
| Séquence    | [Version](version.md)       | N   | N        |
| Attributs  | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

Spécifie que le correctif est membre de la famille de correctifs nommée dans ce champ. Les correctifs de la même famille de correctifs qui ciblent la même version du produit sont triés selon les valeurs de la colonne séquence. Les correctifs au sein de la famille de correctifs sont appliqués au produit cible dans l’ordre de la plus grande séquence. Le PatchFamily est également utilisé pour déterminer les correctifs à remplacer. Un correctif peut figurer dans plusieurs lignes et appartenir à plusieurs familles de correctifs s’il s’applique à plusieurs produits ou comprend plusieurs correctifs.

la Windows Installer n’interprète pas la valeur PatchFamily de quelque manière que ce soit par comparaison avec d’autres valeurs PatchFamily. Une valeur PatchFamily doit être unique dans le ProductCode ciblé par l’ensemble de correctifs. Dans les scénarios complexes de mise à jour corrective, l’identificateur PatchFamily peut avoir besoin d’être globalement unique.

</dd> <dt>

<span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode
</dt> <dd>

Une valeur dans ce champ est facultative. Si un GUID de [Code de produit](product-codes.md) est entré dans ce champ et que le correctif est appliqué au produit spécifié, le correctif est trié et appliqué en tant que membre du PatchFamily spécifié. Si un GUID de code de produit est entré dans ce champ et que le correctif n’est pas appliqué au produit spécifié par ProductCode, cette ligne est ignorée. Si la valeur de ProductCode est NULL, le correctif est trié et appliqué en tant que membre de PatchFamily pour toutes les cibles du correctif, quel que soit le code du produit.

Un correctif peut avoir plusieurs lignes dans le même PatchFamily et une autre ProductCode pour chaque produit ciblé par le correctif. Une ligne pour le PatchFamily peut spécifier la valeur NULL pour ProductCode. Si le produit cible correspond à une ligne avec une valeur ProductCode non NULL, le programme d’installation utilise la ligne correspondante et ignore la ligne avec la valeur ProductCode NULL. Si aucun des codes de produit spécifiés ne correspond à la cible, le correctif est trié et appliqué en tant que membre de PatchFamily pour toutes les cibles du correctif, quel que soit le code du produit.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence
</dt> <dd>

La valeur dans la colonne Sequence spécifie la séquence de ce correctif dans le PatchFamily spécifié. La valeur de la séquence est exprimée au format des données de [version](version.md) . La valeur contient entre 1 et 4 champs et chaque champ a une plage comprise entre 0 et 65535. Les membres de PatchFamily sont triés et appliqués au produit cible dans l’ordre des valeurs de séquence de plus en plus nombreuses. Par exemple, les six valeurs suivantes sont en constante évolution : 1, 1,1, 1,2, 2,01, 2.01.1, 2.01.1.1.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs
</dt> <dd>

La présence de l’attribut **msidbPatchSequenceSupersedeEarlier** dans une ligne indique que le correctif de [mise à jour de petite taille](small-updates.md) remplace les mises à jour fournies par tous les correctifs ayant des valeurs de séquence moindres dans le même PatchFamily. Ce correctif contient tous les correctifs fournis par les correctifs antérieurs dans le PatchFamily spécifié. Cet attribut ne signifie pas que ce correctif remplace les correctifs antérieurs dans tous les cas, car les correctifs précédents peuvent appartenir à plusieurs familles de correctifs.

Un correctif de [petite mise à jour](small-updates.md) ne peut pas remplacer une [mise à niveau mineure](minor-upgrades.md) ou une [mise à niveau majeure](major-upgrades.md) en tout cas, même si **msidbPatchSequenceSupersedeEarlier** est défini. 

| Name                                   | Valeur | Signification                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | 0x00  | Indique une valeur de séquencement simple.                              |
| **msidbPatchSequenceSupersedeEarlier** | 0x01  | Indique un correctif qui remplace les correctifs antérieurs dans cette famille. |



 

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



