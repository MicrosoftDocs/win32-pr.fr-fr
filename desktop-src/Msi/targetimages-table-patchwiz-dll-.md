---
description: La table TargetImages contient des informations sur les images cibles du produit. Un package de correctifs Windows Installer met à jour une image cible en une image mise à niveau.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: Table TargetImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbb8e7bae92fbc25b217808aaae709f079d65dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868450"
---
# <a name="targetimages-table-patchwizdll"></a>Table TargetImages (Patchwiz.dll)

La table TargetImages contient des informations sur les images cibles du produit. Un package de correctifs Windows Installer met à jour une image cible en une image mise à niveau.

Une table TargetImages contenant au moins un enregistrement est requise dans chaque base de données de création de correctif (fichier. PCP). Cette table est utilisée par la fonction [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) .

La table TargetImages contient les colonnes suivantes.



| Colonne                | Type    | Clé | Nullable |
|-----------------------|---------|-----|----------|
| Cible                | text    | O   | N        |
| MsiPath               | text    |     | N        |
| SymbolPaths           | text    |     | O        |
| Upgraded              | text    |     | N        |
| Commande                 | entier |     | N        |
| ProductValidateFlags  | text    |     | O        |
| IgnoreMissingSrcFiles | entier |     | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Indicatif
</dt> <dd>

Identificateur d’une image cible. Le package de correctifs met à jour l’image cible spécifiée dans cette colonne avec l’image mise à niveau spécifiée dans la colonne mise à niveau. Il existe une ou plusieurs images cibles pour chaque image mise à niveau. L’image cible doit être une image d’installation entièrement décompressée du produit, telle qu’une image administrative ou une image d’installation non compressée sur un CD-ROM. Notez que la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) ne génère pas de correctifs binaires pour les fichiers dans les armoires. La valeur de ce champ est utilisée avec la valeur dans le champ mis à niveau pour générer les noms des transformations que le programme d’installation ajoute au package de correctifs.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath
</dt> <dd>

Ce champ spécifie le chemin d’accès complet, y compris le nom de fichier, à l’emplacement du fichier. msi de l’image cible. Il s’agit de l’emplacement des fichiers sources de l’image cible.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Liste délimitée par des points-virgules des dossiers dans lesquels rechercher les fichiers de symboles qui peuvent être utilisés pour optimiser la génération du correctif binaire. Notez que les sous-répertoires des dossiers spécifiés dans ce champ ne sont pas recherchés. Un correctif binaire optimisé peut être plus petit. Microsoft Visual C++ doit être installé sur l’ordinateur générant le correctif et utilisé pour créer les fichiers de symboles. Ce champ est facultatif et le programme d’installation crée un correctif binaire même si aucun fichier de symboles n’est spécifié ou si les fichiers de symboles ne sont pas disponibles pour Patchwiz.dll.

</dd> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Mis à niveau
</dt> <dd>

Clé étrangère vers la colonne mise à niveau de la [table UpgradedImages](upgradedimages-table-patchwiz-dll-.md). La fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) ignore toutes les images mises à niveau qui ne sont pas référencées par au moins un enregistrement de la table TargetImages.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordre
</dt> <dd>

Ordre relatif de l’image cible. Étant donné que plusieurs cibles peuvent être corrigées vers une image mise à niveau, le champ order fournit un moyen de séquencer les transformations dans la liste des transformations de correctifs. En règle générale, l’ordre passe de l’image la plus ancienne à la plus récente.

</dd> <dt>

<span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags
</dt> <dd>

Le champ ProductValidateFlags est utilisé pour spécifier la vérification du produit afin d’éviter d’appliquer des transformations non pertinentes. La valeur entrée dans ce champ doit être un entier hexadécimal à 8 chiffres et l’une des valeurs valides pour le paramètre *iValidation* de la fonction [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) . La valeur par défaut est 0x00000922, ce qui équivaut à **MSITRANSFORM \_ Validate \_ UPDATEVERSION**  +  **MSITRANSFORM \_ Validate \_ NEWEQUALBASEVERSION**  +  **MSITRANSFORM \_ Validate \_ UPGRADECODE**  +  **MSITRANSFORM \_ Validate \_ Product**.

</dd> <dt>

<span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles
</dt> <dd>

Si ce champ est défini sur une valeur différente de zéro, les fichiers absents de l’image cible sont ignorés par le programme d’installation et restent inchangés lors de la mise à jour corrective. Cela permet d’effectuer des correctifs sans avoir besoin de l’intégralité de l’image. Seuls les fichiers modifiés du produit et le fichier. msi sont requis. Cela peut réduire le temps nécessaire pour générer le correctif.

> [!Note]  
> N’utilisez pas la valeur IgnoreMissingSrcFiles avec TrustMsi défini sur 1 dans le [tableau des propriétés](properties-table-patchwiz-dll-.md).

 

</dd> </dl>

## <a name="remarks"></a>Notes

Cette table accepte les variables d’environnement en tant que chemins d’accès commençant par la version 4,0 de Patchwiz.dll.

 

 



