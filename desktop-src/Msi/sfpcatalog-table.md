---
description: la table SFPCatalog contient les catalogues utilisés par Windows Me.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: Table SFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe887644faf6cf0a5cda626bbf757e9f448ef1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238578"
---
# <a name="sfpcatalog-table"></a>Table SFPCatalog

la table SFPCatalog contient les catalogues utilisés par Windows Me.

La table SFPCatalog contient les colonnes suivantes.



| Colonne     | Type                       | Clé : | Nullable |
|------------|----------------------------|-----|----------|
| SFPCatalog | [Nom du fichier](filename.md)   | O   | N        |
| Catalogue    | [Binaire](binary.md)       | N   | N        |
| Dépendance | [Correct](formatted.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog
</dt> <dd>

Nom de fichier abrégé du catalogue. Étant donné que les catalogues n’ont pas de version, le catalogue spécifié dans cette colonne peut remplacer un catalogue qui porte le même nom et qui est déjà installé sur le système local. Consultez la rubrique contrôle de version des fichiers, mais [aucun fichier n’a une version](neither-file-has-a-version.md).

</dd> <dt>

<span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogue
</dt> <dd>

Données binaires du catalogue.

</dd> <dt>

<span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dépendance
</dt> <dd>

Le catalogue spécifié dans ce champ est le parent du catalogue dépendant spécifié dans le champ SFPCatalog. Entrez le nom de fichier abrégé du catalogue parent dans le champ dépendance. Ce champ est une clé de retour dans la colonne SFPCatalog. La correspondance de dépendance est sensible à la casse.

Si le champ de dépendance fait référence à un autre enregistrement dans cette table SFPCatalog, le catalogue parent est installé avant le catalogue dépendant.

Si le champ de dépendance fait référence à un catalogue parent qui n’est pas présent dans le champ SFPCatalog de cette table, et si le catalogue parent n’est pas déjà installé, l’installation échoue.

</dd> </dl>

## <a name="remarks"></a>Remarques

L' [action InstallSFPCatalogFile](installsfpcatalogfile-action.md) interroge la table de [composants](component-table.md), la [table de fichiers](file-table.md), la [table FileSFPCatalog](filesfpcatalog-table.md) et la table SFPCatalog.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
</dl>

 

 



