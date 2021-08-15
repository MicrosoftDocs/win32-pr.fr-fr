---
description: La table DrLocator contient les informations nécessaires pour trouver un fichier ou un répertoire en recherchant dans l’arborescence de répertoires.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Table DrLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1765c7b8f5c38d5701c4c401eb333c7db6a7c403689b8c3100d55b5e51e28e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378323"
---
# <a name="drlocator-table"></a>Table DrLocator

La table DrLocator contient les informations nécessaires pour trouver un fichier ou un répertoire en recherchant dans l’arborescence de répertoires.

La table DrLocator contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Signature\_ | [Identificateur](identifier.md) | O   | N        |
| Parent      | [Identificateur](identifier.md) | O   | O        |
| Chemin        | [AnyPath](anypath.md)       | O   | O        |
| Profondeur       | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_
</dt> <dd>

La \_ colonne signature est une clé externe de la première colonne de la [table de signature](signature-table.md). Ce champ peut représenter une signature de fichier unique figurant dans la table de signatures. Si la valeur de cette colonne est absente de la table de signature, la recherche est supposée être pour un répertoire désigné par la table DrLocator.

</dd> <dt>

<span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Parent
</dt> <dd>

Cette colonne est la signature du répertoire parent du fichier ou du répertoire dans la colonne signature \_ . Si ce champ a la valeur null et que la colonne de chemin d’accès ne se développe pas en chemin d’accès complet, tous les lecteurs fixes du système de l’utilisateur sont recherchés à l’aide du chemin d’accès.

Ce champ est une clé dans l’une des tables suivantes : [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)ou DrLocator.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>D
</dt> <dd>

La colonne Path contient le chemin d’accès sur le système de l’utilisateur. Il s’agit d’un chemin d’accès complet ou d’un sous-chemin d’accès relatif sous le répertoire spécifié dans la colonne parente. Consultez les restrictions sur le type de données [AnyPath](anypath.md) .

</dd> <dt>

<span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Profondeur
</dt> <dd>

Profondeur en dessous du chemin d’accès que le programme d’installation recherche pour le fichier ou le répertoire spécifié dans la \_ colonne signature. La valeur utilisée dans le champ profondeur est basée sur zéro. Par exemple, si le champ path est c:/Program Files/bin, la colonne Depth doit avoir la valeur 0 ou une valeur supérieure pour détecter un fichier situé dans le dossier bin. Si le champ profondeur est vide, la profondeur est supposée être égale à zéro.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette table est utilisée avec la [table AppSearch](appsearch-table.md).

Les colonnes de cette table ne sont généralement pas localisées. Si un auteur décide de rechercher des produits dans plusieurs langues, il doit y avoir une entrée distincte incluse dans le tableau pour chaque langue.

Consultez [recherche d’applications, de fichiers, d’entrées de registre ou de .ini d’entrées de fichier existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



