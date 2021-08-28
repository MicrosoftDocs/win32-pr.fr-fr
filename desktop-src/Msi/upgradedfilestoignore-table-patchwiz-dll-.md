---
description: La table UpgradedFilesToIgnore empêche la mise à jour de fichiers spécifiques qui sont en fait modifiés dans l’image mise à niveau par rapport aux images cibles.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: Table UpgradedFilesToIgnore (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3af0a4a8c3385c2d028cdb66ad276d3f480ca8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884493"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a>Table UpgradedFilesToIgnore (Patchwiz.dll)

La table UpgradedFilesToIgnore empêche la mise à jour de fichiers spécifiques qui sont en fait modifiés dans l’image mise à niveau par rapport aux images cibles. Il peut être utile de le faire dans certains cas. Par exemple, un package de correctifs destiné uniquement à être utilisé avec des installations non administratives n’a pas besoin d’inclure des fichiers de mise à jour corrective qui font uniquement partie des images administratives. L’exclusion de fichiers utilisés uniquement dans les images d’administration peut réduire la taille du package de correctifs. Toutefois, les administrateurs doivent être informés de la mise à jour de ces fichiers séparément. Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La table UpgradedFilesToIgnore contient les colonnes suivantes.



| Colonne   | Type | Clé : | Nullable |
|----------|------|-----|----------|
| Upgraded | texte | O   | N        |
| TCTI      | texte | O   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Mis à niveau
</dt> <dd>

Clé étrangère vers la colonne mise à niveau de la [table UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md). L’outil de création de correctifs exclut la mise à jour du fichier spécifié dans la colonne TCTI de la table UpgradedFilesToIgnore lors de la mise à niveau d’une cible vers l’image spécifiée dans le champ mis à niveau. Entrez la valeur « \* » dans le champ mis à niveau pour exclure la mise à jour du fichier pour toutes les images mises à niveau.

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>TCTI
</dt> <dd>

Clé étrangère dans la [table de fichiers](file-table.md) de l’image mise à niveau. Une valeur de la forme « &lt; préfixe &gt; \* » correspond à toutes les clés de table de fichiers de la table de fichiers qui commencent par ce préfixe. Aucun texte ne peut suivre l’astérisque.

</dd> </dl>

 

 



