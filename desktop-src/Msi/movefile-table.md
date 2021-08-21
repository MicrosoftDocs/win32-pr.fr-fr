---
description: Cette table contient la liste des fichiers à déplacer ou à copier à partir d’un répertoire source spécifié vers un répertoire de destination spécifié.
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: Table MoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d90afe8a5fb950f2e6fdb96ba0f8af4f8969226a5dc219bc9cd0598481beb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945094"
---
# <a name="movefile-table"></a>Table MoveFile

Cette table contient la liste des fichiers à déplacer ou à copier à partir d’un répertoire source spécifié vers un répertoire de destination spécifié.

La table MoveFile contient les colonnes suivantes.



| Colonne       | Type                         | Clé | Nullable |
|--------------|------------------------------|-----|----------|
| FileKey      | [Identificateur](identifier.md) | O   | N        |
| Composant\_  | [Identificateur](identifier.md) | N   | N        |
| SourceName   | [Text](text.md)             | N   | O        |
| DestName     | [Nom du fichier](filename.md)     | N   | O        |
| SourceFolder | [Identificateur](identifier.md) | N   | O        |
| DestFolder   | [Identificateur](identifier.md) | N   | N        |
| Options      | [Integer](integer.md)       | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Clé primaire qui identifie de façon unique un enregistrement MoveFile particulier.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la [table des composants](component-table.md). Si le composant référencé par cette clé n’est pas sélectionné pour l’installation ou la suppression, aucune action n’est effectuée sur cette entrée MoveFile.

</dd> <dt>

<span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName
</dt> <dd>

Cette colonne contient le nom localisable des fichiers sources à déplacer ou copier. Cette colonne peut être laissée vide. Consultez la description de la colonne SourceFolder. Ce champ doit contenir un nom de fichier long et peut contenir des caractères génériques ( \* et ?).

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName
</dt> <dd>

Cette colonne contient le nom localisable à attribuer au fichier d’origine après qu’il a été déplacé ou copié. Si ce champ est vide, le nom du fichier de destination est le même que celui du fichier source.

</dd> <dt>

<span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder
</dt> <dd>

Cette colonne contient le nom d’une propriété ayant une valeur qui correspond au chemin d’accès complet au répertoire source. Si la colonne SourceName est laissée vide, la propriété nommée dans la colonne SourceFolder est supposée contenir le chemin d’accès complet au fichier source lui-même (y compris le nom du fichier).

</dd> <dt>

<span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder
</dt> <dd>

Nom d’une propriété dont la valeur correspond au chemin d’accès complet au répertoire de destination.

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options
</dt> <dd>

Valeur entière spécifiant le mode d’opération.



| Constante                     | Valeur hexadécimale | Decimal | Signification               |
|------------------------------|-------------|---------|-----------------------|
| (aucun)                       | 0x000       | 0       | Copiez le fichier source. |
| **msidbMoveFileOptionsMove** | 0x001       | 1       | Déplacez le fichier source. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Si un \* caractère générique «» est entré dans la colonne SourceName de la table MoveFile et qu’un nom de fichier de destination est spécifié dans la colonne DestName, tous les fichiers déplacés ou copiés conservent les noms dans les sources.

Cette table est traitée par l' [action MoveFiles](movefiles-action.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE85](ice85.md)  
</dl>

 

 



