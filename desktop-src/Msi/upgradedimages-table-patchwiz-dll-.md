---
description: La table UpgradedImages contient des informations sur les images mises à niveau du produit.
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: Table UpgradedImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a50a172511966922186bd91ff387ce4437deca64a704f65fd1ecdff8153192
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809519"
---
# <a name="upgradedimages-table-patchwizdll"></a>Table UpgradedImages (Patchwiz.dll)

La table UpgradedImages contient des informations sur les images mises à niveau du produit. L’image mise à niveau doit être une image d’installation entièrement décompressée de la version la plus récente du produit, par exemple, une image administrative ou une image d’installation non compressée à partir d’un CD-ROM. un package de correctifs Windows Installer met à jour une image cible en une image mise à niveau. La table UpgradedImages est requise dans la base de données de création de correctifs (fichier. PCP) et est utilisée par [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).

Une table UpgradedImages contenant au moins un enregistrement est requise dans chaque base de données de création de correctif (fichier. PCP). Cette table est utilisée par [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).

La table UpgradedImages contient les colonnes suivantes.



| Colonne       | Type | Clé | Nullable |
|--------------|------|-----|----------|
| Upgraded     | text | O   | N        |
| MsiPath      | text |     | N        |
| PatchMsiPath | text |     | O        |
| SymbolPaths  | text |     | O        |
| Famille       | text |     | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Mis à niveau
</dt> <dd>

Le champ mis à niveau est un identificateur arbitraire permettant de connecter les images cibles à une image mise à niveau du produit.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath
</dt> <dd>

Ce champ spécifie le chemin d’accès complet, y compris le nom de fichier, à l’emplacement du fichier .msi de l’image mise à niveau. Il s’agit de l’emplacement des fichiers sources de l’image mise à niveau.

</dd> <dt>

<span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath
</dt> <dd>

Le patchMsiPath facultatif pointe vers une copie modifiée de la base de données d’installation mise à niveau qui contient des créations supplémentaires spécifiques au processus d’installation des correctifs. Par exemple, des boîtes de dialogue supplémentaires ou des actions personnalisées sont conditionnées sur la propriété [**patch**](patch.md) .

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Liste délimitée par des points-virgules des dossiers dans lesquels rechercher les fichiers de symboles qui peuvent être utilisés pour optimiser la génération du correctif binaire. Notez que les sous-répertoires des dossiers spécifiés dans ce champ ne sont pas recherchés. Un correctif binaire optimisé peut être plus petit. Visual C++ doit être installé sur l’ordinateur générant le correctif et utilisé pour créer les fichiers de symboles. Ce champ est facultatif et le programme d’installation crée un correctif binaire même si aucun fichier de symboles n’est spécifié ou si les fichiers de symboles ne sont pas disponibles pour Patchwiz.dll.

</dd> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famille
</dt> <dd>

Clé étrangère dans la [table ImageFamilies](imagefamilies-table-patchwiz-dll-.md). Chaque image mise à niveau ne doit appartenir qu’à une seule famille.

</dd> </dl>

## <a name="remarks"></a>Remarques

Bien que chaque image mise à niveau puisse être regroupée dans une famille d’images distincte, le regroupement d’images mises à niveau qui partagent des fichiers peut rendre le fichier. msp plus petit.

Cette table accepte les variables d’environnement en tant que chemins d’accès commençant par la version 4,0 de Patchwiz.dll.

 

 



