---
description: La table RemoveIniFile contient les informations qu’une application doit supprimer d’un fichier. ini.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Table RemoveIniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57b4ba6f2c42ee636f1b9e21e798e27665f102a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542013"
---
# <a name="removeinifile-table"></a>Table RemoveIniFile

La table RemoveIniFile contient les informations qu’une application doit supprimer d’un fichier. ini.

La table RemoveIniFile contient les colonnes suivantes.



| Colonne        | Type                         | Clé | Nullable |
|---------------|------------------------------|-----|----------|
| RemoveIniFile | [Identificateur](identifier.md) | O   | N        |
| FileName      | [FileName](text.md)         | N   | N        |
| DirProperty   | [Identificateur](identifier.md) | N   | O        |
| Section       | [Correct](formatted.md)   | N   | N        |
| Clé           | [Correct](formatted.md)   | N   | N        |
| Valeur         | [Correct](formatted.md)   | N   | O        |
| Action        | [Integer](integer.md)       | N   | N        |
| -\_   | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile
</dt> <dd>

Clé de cette table.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extension
</dt> <dd>

Nom du fichier. ini dans lequel supprimer les informations.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nom d’une propriété dont la valeur est supposée correspondre au chemin d’accès complet au dossier du fichier. ini à supprimer. La propriété peut être le nom d’un répertoire dans la [table de répertoires](directory-table.md), une propriété définie par la [table AppSearch](appsearch-table.md), ou toute autre propriété qui représente un chemin d’accès complet.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section
</dt> <dd>

Section du fichier. ini localisable.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel
</dt> <dd>

La clé du fichier. ini localisable sous la section.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Valeur localisable à supprimer. La valeur est obligatoire lorsque action a la valeur 4.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel
</dt> <dd>

Type de modification à effectuer.



| Constante                         | Valeur hexadécimale | Decimal | Signification                          |
|----------------------------------|-------------|---------|----------------------------------|
| **msidbIniFileActionRemoveLine** | 0x002       | 2       | Supprime l’entrée. ini.              |
| **msidbIniFileActionRemoveTag**  | 0x004       | 4       | Supprime une balise d’une entrée. ini. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la première colonne de la [table de composants](component-table.md) référençant le composant qui contrôle la suppression de la valeur. ini.

</dd> </dl>

## <a name="remarks"></a>Notes

Les informations du fichier. ini sont supprimées lorsque le composant correspondant a été sélectionné pour être installé, localement ou exécuté à partir de la source.

Cette table est référencée lorsque l' [action RemoveIniValues](removeinivalues-action.md) est exécutée.

Si la colonne de répertoire \_ est spécifiée comme étant null, l’emplacement du fichier ini est l’emplacement du fichier ini Windows standard qui est le répertoire Windows par défaut.

La suppression de la dernière valeur d’une section supprime cette section. Il n’existe aucune autre façon de supprimer toute une section autre que la suppression de toutes ses valeurs.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



